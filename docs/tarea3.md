## 1. Matriz de Mapeo de Metáforas de Interfaz

| Metáfora / Dominio Fuente (Mundo Real) | Elemento Digital (UI/HCI) | Etiqueta / Mensaje en Pantalla | Comportamiento del Sistema | Riesgo |
| :--- | :--- | :--- | :--- | :--- |
| **1. El Semáforo de Tránsito**<br>| Grid / Matriz interactiva de disponibilidad de horarios por cada uno de los 5 fisioterapeutas. | • "Horario Disponible"<br>• "Reserva Temporal, 5 min"<br>• "Turno Ocupado" | Al hacer clic en una celda verde, el sistema cambia a amarillo y bloquea el cupo en el servidor por 5 minutos para evitar citas duplicadas mientras el usuario llena sus datos. | **Daltonismo / Deuteranopia:** Los usuarios con deficiencia cromática no distinguen verde de rojo.<br>*Mitigación:* Añadir iconos de estado (check, candado, reloj) y etiquetas de texto explícitas. |
| **2. El Camino del Paciente**<br>| Stepper / Barra de progreso lineal interactiva de 4 pasos para el agendamiento. | "Paso 2 de 4: Seleccione su Fisioterapeuta y Horario" | Muestra el progreso visual. Permite la navegación bidireccional (avanzar y retroceder) sin borrar los datos previamente ingresados en los pasos anteriores. | **Direccionalidad de lectura:** Asume lectura occidental, izquierda a derecha.<br>*Mitigación:* Mantener numeración clara, "Paso 1 de 4" y flechas de navegación universales. |
| **3. La Ficha Médica de Papel**<br> | Tarjeta contenedora de datos del paciente con mecanismo de autoguardado pasivo. | "Borrador guardado automáticamente a las 10:45 AM" | Detecta inactividad en el teclado (debounce 2s) y guarda los datos en segundo plano. Si la página se cierra o se navega atrás, los datos se recuperan automáticamente. | **Resistencia al modelo invisible:** Usuarios tradicionales buscan un botón físico explícito de "Guardar".<br>*Mitigación:* Incluir el aviso de autoguardado pasivo junto con un botón claro de "Confirmar Cita". |

---

## 2. Análisis por Perspectiva Lingüística y Computacional

### 2.1 Metáfora 1: El Semáforo de Tránsito

* **Perspectiva Lingüística (Lenguaje del Sistema):**  
  Elimina por completo la jerga técnica de base de datos, como `"Slot_ID_404"` o `"Status Code 200"` y utiliza un vocabulario cotidiano orientado al dominio del paciente y de la secretaria Gaby: *"Horario Libre a las 15:00"*, *"Fisioterapeuta en Consulta"*, *"Turno Reservado"*. La interfaz habla el lenguaje del usuario de forma amigable y transparente.

* **Perspectiva Computacional (Reglas de Negocio y Persistencia):**  
  Implementa un control de concurrencia en la región crítica del backend. Al presionar una celda verde, se emite una petición transaccional que cambia el estado del cupo a `PENDING_LOCK` con un tiempo de vida (TTL) de 300 segundos en memoria (Redis/Cache). Si el usuario no confirma la cita dentro del tiempo límite, el evento `RELEASE_SLOT` libera automáticamente el cupo devolviéndolo al estado `AVAILABLE` (Verde).

---

### 2.2 Metáfora 2: El Camino del Paciente

* **Perspectiva Lingüística (Lenguaje del Sistema):**  
  Establece un diálogo instruccional claro e informativo que guía al usuario durante todo el flujo (*"Paso 2 de 4: Selecciona tu especialista y hora"*). Los botones evitan términos ambiguos como *"Submit"* o *"Process"*, empleando verbos de acción claros como *"Continuar a Datos del Paciente"* o *"Volver a Selección"*.

* **Perspectiva Computacional (Reglas de Negocio y Persistencia):**  
  Maneja un estado global de navegación en el cliente (`AppointmentFormState`). La navegación bidireccional mediante `nextStep()` y `prevStep()` mantiene la persistencia en memoria local (`sessionStorage`), permitiendo que el usuario retroceda para cambiar de fisioterapeuta sin que el formulario dispare validaciones de error destructivas ni borre el nombre o teléfono ya digitados.

---

### 2.3 Metáfora 3: La Ficha Médica de Papel

* **Perspectiva Lingüística (Lenguaje del Sistema):**  
  Utiliza mensajes tranquilizadores que disipan el miedo a perder la información: *"Borrador guardado automáticamente"*, *"Tus datos están a salvo"*, *"Última sincronización hace un momento"*.

* **Perspectiva Computacional (Reglas de Negocio y Persistencia):**  
  Aplica un patrón de diseño *Debounce* de 2000 ms en los eventos del formulario. Cuando el usuario deja de teclear, el sistema persiste automáticamente los campos en la memoria local (`localStorage`). En caso de una desconexión de red durante el registro, activa el estado `OFFLINE_DRAFT` almacenando los datos en una cola de peticiones (*Request Queue*) que se sincroniza automáticamente (`SYNC_ON_RECONNECT`) al detectar nuevamente acceso a internet.
