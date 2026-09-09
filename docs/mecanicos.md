## 1. Introducción y Contexto

El centro de fisioterapia **GABO'S Readaptación y Movimiento** cuenta con cinco fisioterapeutas. Actualmente, la gestión de citas se realiza mediante mecanismos heterogéneos y descentralizados (mensajes no estructurados por WhatsApp y registros en una agenda física de papel). Esta modalidad presenta deficiencias operativas como sobrecarga del personal administrativo, riesgo de sobreposición de horarios, falta de trazabilidad histórica y retrasos significativos en la confirmación de citas para los pacientes.

El objetivo de este documento es evaluar técnicamente diversos mecanismos de agendamiento aplicables al centro y fundamentar la selección de la alternativa óptima mediante una matriz paramétrica de decisión.

---

## 2. Análisis Comparativo de Mecanismos de Agendamiento

Se evalúan cuatro mecanismos de agendamiento considerando las dinámicas clínicas de los 5 fisioterapeutas, las capacidades del personal de recepción y la experiencia del usuario/paciente:

1. **Mecanismo 1: Agenda Digital Interna (Centralizada)**
   * **Descripción:** El paciente solicita la cita por canales externos (WhatsApp, llamada) y el personal administrativo registra, modifica y cancela todas las citas manualmente en un calendario o portal web interno.
   * **Ventajas:** Control absoluto por parte de recepción; previene el autoagendamiento erróneo por parte de pacientes.
   * **Desventajas:** Mantiene el cuello de botella en la recepción; no reduce significativamente el tiempo de intervención administrativa ni la espera del paciente.

2. **Mecanismo 2: Solicitud con Confirmación (Asincrónico Asistido)**
   * **Descripción:** El paciente ingresa a un portal web y solicita un horario preferente. La solicitud queda en estado "Pendiente" hasta que el personal administrativo revisa la disponibilidad y confirma o rechaza la reserva.
   * **Ventajas:** Permite filtrar y revisar las solicitudes antes de la reserva definitiva.
   * **Desventajas:** Genera un estado de incertidumbre en el paciente mientras espera la confirmación; requiere doble interacción para concretar una sola cita.

3. **Mecanismo 3: Autoagendamiento Directo (Autoservicio Completo)**
   * **Descripción:** El paciente selecciona un fisioterapeuta, escoge un horario disponible en tiempo real y confirma la cita de manera autónoma sin mediación humana.
   * **Ventajas:** Maximiza la velocidad de agendamiento y elimina el 100% del trabajo administrativo en citas convencionales.
   * **Desventajas:** Alto riesgo de asignación inadecuada de pacientes con patologías complejas a fisioterapeutas sin la subespecialidad requerida; falta de flexibilidad ante excepciones o emergencias clínicas.

4. **Mecanismo 4: Mecanismo Híbrido (Automatizado con Gestión Asistida por Excepción)**
   * **Descripción:** Combina la autonomía del autoagendamiento para citas rutinarias/estándar con un flujo de validación y control administrativo para casos especiales (primeras evaluaciones complejas, reagendamientos críticos, cancelaciones de última hora o asignaciones por subespecialidad).
   * **Ventajas:** Equilibra la eficiencia operativa y la reducción de carga con la rigurosidad clínica necesaria para la atención en fisioterapia.

---

## 3. Matriz Paramétrica de Decisión

Para seleccionar el mecanismo adecuado, se establece una escala de evaluación de **1 a 5** (donde 1 representa muy bajo cumplimiento/desfavorable y 5 representa máximo cumplimiento/óptimo).

| Criterio de Evaluación | Peso (%) | Agenda Digital Interna | Solicitud con Confirmación | Autoagendamiento Directo | Mecanismo Híbrido (Seleccionado) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Prevención de Conflictos y Solapamiento** | 25% | 3 | 4 | 3 | **5** |
| **Reducción de Esfuerzo Administrativo** | 25% | 2 | 3 | 5 | **4** |
| **Factibilidad Operativa (5 Fisioterapeutas)** | 20% | 4 | 4 | 2 | **5** |
| **Facilidad de Uso y Accesibilidad (Paciente)**| 15% | 3 | 3 | 4 | **5** |
| **Flexibilidad ante Excepciones Clínicas** | 15% | 4 | 3 | 1 | **5** |
| **Puntaje Ponderado Total** | **100%** | **3.05** | **3.45** | **3.20** | **4.75** |

---

## 4. Justificación Científico-Técnica de la Selección

Se selecciona el **Mecanismo Híbrido** (Puntaje Ponderado: **4.75/5.00**) por las siguientes razones sustentadas en los requerimientos del centro:

1. **Optimización de la Carga Cognitiva y Operativa:** Al automatizar el agendamiento recurrente y estándar, la secretaria (recepción) reduce en más de un 60% las tareas repetitivas de digitación y consulta de horarios, focalizando su tiempo de atención en la coordinación de pacientes complejos y en la atención presencial.
2. **Control Clínico y Compatibilidad Multiespecialista:** Los 5 fisioterapeutas del centro poseen cargas de trabajo y especialidades distintas. El enfoque híbrido permite parametrizar reglas lógicas de negocio (ej. tiempo de evaluación inicial vs. sesión de mantenimiento) asegurando que el paciente sea atendido en el bloque y con el profesional correcto.
3. **Reducción de Errores por Doble Validación:** El sistema informático ejerce un bloqueo en tiempo real sobre la base de datos para impedir citas dobles (prevención de errores de software), mientras que el personal administrativo retiene el control de las excepciones (prevención de errores de contexto clínico).