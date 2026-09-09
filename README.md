# 🩺 Sistema Interactivo de Agendamiento de Citas
## GABO'S Readaptación y Movimiento

Este repositorio contiene la especificación, el diseño de interacción humano-computador (IHC) y los prototipos de alta fidelidad para el rediseño del proceso de agendamiento de citas del centro de fisioterapia **GABO'S Readaptación y Movimiento**.

---

## 📌 1. Diagnóstico del Proceso Actual (AS-IS)

Actualmente, la gestión de citas y el control de historias clínicas operan de forma fragmentada mediante mensajes no estructurados en **WhatsApp**, **Google Drive** y una **agenda física de papel**.

### 🔄 Flujo AS-IS y Puntos de Fricción

| Paso | Acción Actual | Medio | Punto de Fricción / Riesgo |
| :---: | :--- | :---: | :--- |
| **1** | Solicitud de cita | WhatsApp | **Incertidumbre visual:** El paciente no conoce los horarios libres. |
| **2** | Consulta de disponibilidad | WhatsApp / Agenda | **Sobrecarga de atención:** Búsqueda manual no estructurada. |
| **3** | Coordinación con especialista | Conversación manual | **Espera prolongada:** Respuesta paralizada si el terapeuta está en consulta. |
| **4** | Registro y confirmación | Agenda física / WhatsApp | **Acciones duplicadas:** Transcripción manual propensa a errores. |
| **5** | Cambios o cancelaciones | Agenda física / WhatsApp | **Deterioro de consistencia:** Tachar o borrar sobre papel. |

### ⚠️ Factores de Fricción Operativa
* **Límite Cognitivo (Humano):** Sobreesfuerzo en memoria de trabajo (*Número de Miller: 7±2*) y fatiga mental por multicanalidad.
* **Silos Tecnológicos (Técnico):** Desconexión entre historial clínico y agendamiento; ausencia de alertas automáticas ante sobreposiciones (*Nielsen #5*).

---

## 🛠️ 2. Propuesta de Solución: Mecanismo Híbrido

Tras analizar cuatro alternativas mediante una matriz paramétrica de decisión, se seleccionó el **Mecanismo Híbrido (Automatizado con Gestión Asistida por Excepción)** con una calificación de **4.75 / 5.00**.

* **Autonomía:** Autoagendamiento directo para citas rutinarias/estándar.
* **Control Asistido:** Validación y gestión por recepción para casos complejos, reagendamientos críticos o asignaciones por subespecialidad.
* **Beneficio:** Reduce en más de un 60% las tareas repetitivas de digitación y elimina las citas dobles mediante bloqueos en tiempo real.

---

## 📊 3. Indicadores de Eficiencia y Metáforas de Interfaz (IHC)

### 📈 Indicadores Mapeados
1. **Tiempo de Ciclo Operativo ($T_c$):** Reducción de tiempos de registro a $\le 90$ segundos.
2. **Tiempo de Intervención Administrativa ($T_a$):** Liberación de carga en recepción.
3. **Número de Transacciones ($N_a$):** Máximo 3 clics para consultar disponibilidad.
4. **Tasa de Automatización ($I_h$):** Medición del porcentaje de autoservicio alcanzado.
5. **Tasa de Errores ($E_r$):** Prevención de fallos de digitación y cruces de agenda.

### 🎨 Metáforas Visuales Integradas
* **El Semáforo de Tránsito:** Matriz interactiva de disponibilidad (🟢 Disponible, 🟡 Reserva Temporal, 🔴 Ocupado) con soporte para acromatopsia mediante simbología.
* **El Camino del Paciente:** Formulario secuencial por pasos (*Stepper*) con navegación bidireccional sin pérdida de datos.
* **La Ficha Médica de Papel:** Autoguardado pasivo (*Debounce 2s*) y soporte de borrador *offline*.

---

## 🎨 4. Prototipo Navegable de Alta Fidelidad

* **Herramienta:** Figma (High-Fidelity Prototype)
* **Enlace de Acceso:** [Ver Prototipo Interactivo en Figma](https://www.figma.com/design/e5eBbcsee8QaGX1c4mOiXh/Untitled?t=ZJRGDeKQND5tZx8U-1)

### 📱 Pantallas Principales

#### 1. Dashboard Principal y Buscador (Semáforo de Carga)
Permite identificar la disponibilidad por especialidad y rango horario sin realizar consultas profundas.

![Dashboard Principal](prototype/image/image.png)

---

#### 2. Selección de Especialista y Horario
Grilla de bloques horarios clicables organizados cronológicamente con tarjetas informativas del profesional.

![Selección de Especialista](prototype/image/image-1.png)
![Selección de Horario](prototype/image/image-2.png)

---

#### 3. Formulario por Pasos (Stepper Wizard)
Captura de datos estructurada en 3 fases para prevenir la fatiga cognitiva del usuario.

![Formulario Stepper](prototype/image/image-3.png)

---

#### 4. Expediente y Confirmación Automática
Resumen de la reserva con generación inmediata de comprobante en PDF y reenvío por WhatsApp/Correo.

![Confirmación de Cita](prototype/image/image-4.png)

---

#### 5. Flujo de Cancelación y Reagendamiento
Ventana modal de confirmación para evitar cierres accidentales y permitir la reprogramación ágil.

![Cancelación y Reagendamiento](prototype/image/image-5.png)

---

## 📁 5. Documentación y Asignación de Tareas

Toda la documentación detallada del proyecto, informes técnicos y desglose del trabajo colaborativo se encuentran organizados dentro de la carpeta `/docs` del repositorio:

* **`/docs`**: Contiene los archivos Markdown individuales con el desarrollo exhaustivo de cada una de las actividades asignadas a los integrantes del equipo.

| Actividad / Módulo | Descripción | Ubicación |
| :--- | :--- | :--- |
| **Actividades 1 y 2** | Análisis AS-IS, Puntos de Fricción y Matriz de Necesidades de Usuarios. | `/docs/tarea1.md` |
| **Actividades 3 y 4** | Selección de Mecanismo de Agendamiento, Matriz Paramétrica e Indicadores de Eficiencia IHC. | `/docs/indicadores.md y mecanicos.md` |
| **Actividad 5** | Especificación de Metáforas de Interfaz (Perspectiva Lingüística y Computacional). | `/docs/tarea3.md` |
| **Actividad 6** | Prototipado de Alta Fidelidad en Figma y Arquitectura de Interacción. | `/prototype/` |