# 🩺 Sistema Interactivo de Agendamiento de Citas
## GABO'S Readaptación y Movimiento

Este repositorio contiene la especificación técnica, el análisis de usabilidad e Interacción Humano-Computador (IHC) y los prototipos de alta fidelidad para el rediseño del proceso de gestión de citas del centro de fisioterapia **GABO'S Readaptación y Movimiento**.

---

## 👥 Integrantes y Roles

* **Sebastián Santana:** Frontend Developer
* **Alex Guachi:** Backend Developer
* **Wilson Pillapa:** Tester
* **Viviana Sarco:** QA (Quality Assurance)

---

## 📌 1. Diagnóstico del Proceso Actual (AS-IS)

Actualmente, la gestión de la información opera de forma fragmentada: las historias clínicas se almacenan en documentos de Google Drive, mientras que las citas se coordinan manualmente mediante mensajes no estructurados en **WhatsApp** y una **agenda física de papel**.

### 🔄 Flujo AS-IS y Puntos de Fricción

| Paso | Acción Actual (Flujo AS-IS) | Medio | Punto de Fricción / Riesgo Identificado |
| :---: | :--- | :---: | :--- |
| **1** | El paciente solicita una cita por WhatsApp. | WhatsApp | **Incertidumbre visual:** Ausencia de visibilidad sobre horarios libres; opera "a ciegas". |
| **2** | El personal revisa mensajes y consulta disponibilidad. | WhatsApp / Agenda | **Sobrecarga de atención:** Búsqueda manual no estructurada en mensajes y papel. |
| **3** | Se coordina el horario con el fisioterapeuta de turno. | Conversación manual | **Espera prolongada:** Respuesta paralizada si el terapeuta está en consulta. |
| **4** | La cita se registra y se confirma manualmente. | Agenda física / WhatsApp | **Acciones duplicadas:** Transcripción propensa a errores ortográficos o cruces de nombres. |
| **5** | Los cambios o cancelaciones se procesan manualmente. | Agenda física / WhatsApp | **Trampa de consistencia:** Tachar o borrar con corrector deteriora el soporte analógico. |

### ⚠️ Factores de Fricción Operativa
* **Limitaciones Cognitivas (Humano):** Sobreesfuerzo en la memoria de trabajo de la secretaria (*Número de Miller: $7 \pm 2$*) al retener solicitudes mientras hojea la agenda, sumado a la fatiga mental por multicanalidad.
* **Brechas Tecnológicas (Técnico):** Silos desconectados entre historias clínicas y citas, además de la falta de alertas lógicas en papel para evitar sobreposiciones o sobrecargas de horas (*Nielsen #5*).

---

## 👥 2. Matriz de Necesidades de Usuarios

| Usuario | Objetivo Principal | Necesidad en la Interfaz (IHC) | Dificultad Actual (Silos / Papel) |
| :--- | :--- | :--- | :--- |
| **🩺 Paciente** *(Estudiantes y ciudadanos)* | Reservar sesiones de terapia de forma ágil y autónoma. | Flujo de pasos sencillo, visibilidad real de horarios y confirmación inmediata por SMS/WhatsApp. | Dependencia de la respuesta humana; esperas prolongadas para conocer cupos. |
| **👨‍⚕️ Fisioterapeuta** *(5 especialistas)* | Visualizar su cronograma diario y registrar evoluciones clínicas. | Acceso rápido móvil, interfaz limpia sin información redundante y control de carga. | Falta de sincronización; debe revisar la agenda en recepción para enterarse de cambios. |
| **👩‍💼 Personal Administrativo** *(Recepción / Gaby)* | Coordinar recursos, evitar sobreposiciones y confirmar citas. | Herramienta unificada que prevenga reservas cruzadas y guarde datos automáticamente. | Estrés y saturación operacional por atender llamadas, WhatsApp y la agenda física. |
| **📊 Administrador del Centro** *(Gabo / Gerencia)* | Monitorear productividad, analizar asistencias y optimizar la capacidad. | Tablero de control consolidado con métricas de eficiencia e historial inmutable. | Inexistencia de datos históricos o estadísticas centralizadas en soporte analógico. |

---

## 🛠️ 3. Propuesta de Solución: Mecanismo Híbrido

Tras evaluar cuatro alternativas mediante una matriz de selección paramétrica (Agenda Digital Interna, Solicitud con Confirmación, Autoagendamiento Directo y Mecanismo Híbrido), se seleccionó el **Mecanismo Híbrido (Automatizado con Gestión Asistida por Excepción)**.

* **Autonomía:** Automatización del autoagendamiento directo para el 80% de las citas rutinarias y estándares.
* **Control Asistido:** Validación y control por recepción para casos complejos, reagendamientos críticos o asignaciones por subespecialidad clínica.
* **Impacto Operativo:** Ahorro directo de 135 segundos por cita (75% de optimización de tiempo) y reducción del porcentaje de intervención administrativa manual al 0% en citas estándar.

---

## 📊 4. Indicadores de Eficiencia y Metáforas de Interfaz (IHC)

### 📈 Indicadores Operacionalizados
* **Tiempo de Ciclo Operativo ($T_c$):** Registro y guardado exitoso con validación de datos en $\le 90$ segundos.
* **Carga de Clics ($COC$):** Reducción de la interacción a un camino óptimo de $\le 3$ clics para consultar disponibilidad.
* **Tasa de Errores ($TER$):** Validación en tiempo real para lograr un $0.0\%$ de margen de error en la entrada de datos.

### 🎨 Metáforas Visuales Integradas
1. **El Semáforo de Tránsito:** Matriz interactiva de disponibilidad (🟢 Verde: Disponible, 🟡 Amarillo: Pendiente, 🔴 Rojo: Reservado) con iconos explícitos para usuarios con daltonismo.
2. **El Sendero del Paciente:** Barra de progreso lineal (*Stepper*) interactiva de 4 pasos con navegación bidireccional sin pérdida de campos.
3. **La Ficha Médica de Papel:** Contenedor de datos con autoguardado pasivo (*Debounce 2s*) y persistencia local para prevenir pérdidas ante desconexiones.

---

## 🎨 5. Prototipo Navegable de Alta Fidelidad

* **Herramienta:** Figma (High-Fidelity Interactive Prototype)
* **Enlace de Acceso:** [Ver Prototipo Interactivo en Figma](https://www.figma.com/design/e5eBbcsee8QaGX1c4mOiXh/Untitled?t=ZJRGDeKQND5tZx8U-1)

### 📱 Pantallas Principales e Interacciones

#### 1. Dashboard Principal y Buscador (Semáforo de Carga)
Proporciona visibilidad del estado del sistema (*Nielsen #1*), resumen de citas y matriz de disponibilidad en tiempo real.

![Dashboard Principal](prototype/image/image.png)

---

#### 2. Selección de Especialista y Horario
Grilla de bloques horarios clicables con tarjetas informativas del profesional de la salud.

![Buscador de Disponibilidad](prototype/image/image-1.png)
![Especialistas y Horarios](prototype/image/image-2.png)

---

#### 3. Formulario por Pasos (Stepper Wizard)
Captura de datos estructurada en fases secuenciales para evitar el desbordamiento de la memoria de trabajo.

![Formulario Stepper](prototype/image/image-3.png)

---

#### 4. Expediente de Cita y Confirmación Automática
Resumen del registro con historial de estado, detalles del tratamiento y opciones de gestión.

![Expediente de Cita](prototype/image/image-4.png)

---

#### 5. Flujo de Cancelación y Reagendamiento
Diálogo de confirmación explícito con ventana modal de advertencia para prevenir acciones accidentales y permitir la recuperación rápida.

![Flujo de Cancelación y Reagendamiento](prototype/image/image-5.png)

---

## 📁 6. Estructura de Documentación y Asignación de Tareas

Toda la documentación detallada del proyecto, análisis metodológicos y el desarrollo de la prueba práctica se encuentran distribuidos dentro del directorio `/docs` del repositorio:

* **`/docs/tarea1.md`**: Modelado de flujo AS-IS, puntos de fricción cognitivos/tecnológicos y Matriz de Usuarios (*Asignado a Viviana Sarco - QA*).
* **`/docs/indicadores.md y mecanicos.md`**: Comparación técnica de mecanismos de agendamiento, justificación del mecanismo híbrido e indicadores de eficiencia IHC (*Asignado a Alex Guachi - Backend Developer*).
* **`/docs/tarea3.md`**: Creación de metáforas de interfaz, análisis lingüístico y computacional (*Asignado a Wilson Pillapa - Tester*).
* **`/prototype`**: Especificación del prototipo navegable, protocolo de validaciones cruzadas y métricas consolidadas (*Asignado a Sebastián Santana - Frontend Developer*).