# 🔍 Actividad 1: Análisis del Proceso Actual (AS-IS) y Puntos de Fricción

## 1. 📌 Contexto Diagnóstico
El centro de fisioterapia **GABO'S Readaptación y Movimiento** cuenta con cinco fisioterapeutas. Actualmente, la gestión de la información se encuentra fragmentada: las historias clínicas se almacenan en documentos de Google Drive, mientras que las citas se coordinan de forma manual mediante mensajes no estructurados en **WhatsApp** y una **agenda física**. Esta desorganización dificulta la visibilidad de horarios disponibles, sobrecarga al personal y genera reprocesos constantes.

---

## 2. 🔄 Flujo de Trabajo Actual (AS-IS) y Puntos de Fricción

| Paso | Acción Actual (Flujo AS-IS) | Medio Utilizado | Punto de Fricción Identificado / Riesgo de Error |
| :---: | :--- | :---: | :--- |
| **1** | 📩 El paciente solicita una cita. | WhatsApp | **Incertidumbre visual:** El usuario no conoce los horarios libres, operando "a ciegas". |
| **2** | 🔎 El personal revisa mensajes y consulta disponibilidad. | WhatsApp y Agenda Física | **Sobrecarga de atención:** Búsqueda manual en mensajes no estructurados y en la agenda física. |
| **3** | 🤝 Se coordina el horario con el fisioterapeuta. | Conversación / Revisión manual | **Espera prolongada:** Si el fisioterapeuta está en consulta, la respuesta al paciente se paraliza. |
| **4** | 📝 La cita se registra y se confirma al paciente. | Agenda Física y WhatsApp | **Acciones duplicadas:** Transcripción manual propensa a errores ortográficos o cruces de nombres. |
| **5** | ❌ Los cambios o cancelaciones se procesan manualmente. | WhatsApp y Agenda Física | **Trampa de consistencia:** Tachar o borrar la agenda física deteriora el registro analógico. |

---

## 3. ⚠️ Factores Determinantes de la Fricción Operativa

### 🧠 Factores Humanos (Limitaciones Cognitivas)
* 🧩 **Memoria de Trabajo del Administrador:** La recepción debe retener mentalmente solicitudes de varios pacientes mientras hojea la agenda física. Este sobreesfuerzo excede el límite cognitivo de la memoria de corto plazo (*Número de Miller: 7±2 elementos*), propiciando olvidos o errores de agendamiento.
* 🔋 **Fatiga Mental y Carga de Atención:** Atender llamadas, responder mensajes en WhatsApp y atender pacientes presenciales de forma simultánea eleva la carga mental, incrementando la probabilidad de cometer errores de digitación.

### 🛠️ Factores Tecnológicos (Brechas de Ingeniería)
* 🗄️ **Silos de Información Desconectados:** La separación entre la base de datos de historias clínicas (Google Drive) y el control de citas (agenda física) impide validar de forma automática restricciones médicas previas.
* 🚨 **Falta de Retroalimentación de Estado:** La agenda en papel carece de alertas lógicas que adviertan sobre sobreposiciones o límites de carga horaria de los fisioterapeutas, violando el principio interactivo de *Prevención de Errores* (Nielsen #5).

---

# 👥 Actividad 2: Identificación de Usuarios y Matriz de Necesidades

El rediseño del sistema interactivo de agendamiento para **GABO'S Readaptación y Movimiento** requiere caracterizar los perfiles de usuarios que interactúan con el proceso para mitigar sus brechas de uso:

---

## 📋 Matriz de Necesidades de Usuarios

| Usuario | Objetivo Principal | Necesidad en la Interfaz (IHC) | Dificultad Actual (Silos / Papel) |
| :--- | :--- | :--- | :--- |
| **🩺 Paciente**<br>*(Estudiantes y ciudadanos)* | Reservar sesiones de terapia física de forma ágil y autónoma. | Flujo de pasos sencillo, visibilidad real de horarios disponibles y confirmación inmediata por SMS/WhatsApp. | Dependencia de la respuesta humana por WhatsApp; esperas prolongadas para conocer cupos. |
| **👨‍⚕️ Fisioterapeuta**<br>*(5 especialistas)* | Visualizar su cronograma diario de pacientes y registrar evoluciones clínicas. | Acceso rápido desde dispositivos móviles, interfaz limpia sin información redundante y control de carga. | Falta de sincronización; debe revisar la agenda en recepción para enterarse de cambios de último minuto. |
| **👩‍💼 Personal Administrativo**<br>*(Recepción / Gaby)* | Coordinar recursos del centro, evitar cruces de horarios y confirmar citas. | Herramienta unificada que prevenga sobreposiciones y registre datos automáticamente sin duplicar pasos. | Estrés y saturación operacional por atender llamadas, chats de WhatsApp y la agenda física al mismo tiempo. |
| **📊 Administrador del Centro**<br>*(Gabo / Gerencia)* | Monitorear la productividad, analizar asistencias y optimizar la capacidad instalada. | Tablero de control (dashboard) consolidado con métricas de eficiencia e historial inmutable de citas. | Inexistencia de datos históricos o estadísticas centralizadas en el soporte analógico de papel. |