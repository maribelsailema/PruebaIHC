## 1. Marco Metodológico para la Eficiencia en IHC

En la Ingeniería de Interacción Humano-Computador (IHC) y la Evaluación de Usabilidad (ISO 9241-11), la **eficiencia** no se define únicamente a partir del tiempo cronométrico de ejecución. La eficiencia global del proceso comprende la relación entre los recursos consumidos (tiempo, esfuerzo cognitivo, acciones físicas) y la precisión con la que los usuarios alcanzan sus metas (ausencia de errores y reprocesos).

Para el proyecto en **GABO'S Readaptación y Movimiento**, la variable independiente es el **"Mecanismo de gestión de citas"** y la variable dependiente es la **"Eficiencia del proceso de agendamiento"**.

---

## 2. Definición del Multicriterio de Indicadores

Para evaluar de manera integral la variable dependiente, se establece un conjunto multidimensional de 5 indicadores de eficiencia:

1. **Tiempo de Ciclo Operativo ($T_c$):** Duración total desde que se inicia una solicitud hasta que queda registrada de forma persistente en el sistema.
2. **Tiempo de Intervención Administrativa ($T_a$):** Tiempo neto empleado por el personal del centro (secretaría/fisioterapeutas) para validar, procesar o confirmar una operación.
3. **Número de Acciones / Transacciones ($N_a$):** Cantidad de clics, pulsaciones de tecla o interacciones físicas requeridas para completar la tarea.
4. **Porcentaje / Nivel de Intervención Humana ($I_h$):** Proporción de tareas completadas de forma 100% automatizada (autoservicio) frente a las que requieren mediación humana manual.
5. **Tasa de Errores y Reprocesos ($E_r$):** Número de errores de digitación, selecciones incorrectas o intentos fallidos cometidos durante el flujo de interacción.

---

## 3. Operacionalización de las Operaciones de Agendamiento

A continuación se detallan las 5 operaciones fundamentales del módulo de gestión de citas, definiendo sus límites de inicio/fin, criterios de éxito e indicadores observables:

| Operación | Inicio del Flujo | Fin del Flujo | Criterio de Éxito | Indicadores Observables de Eficiencia |
| :--- | :--- | :--- | :--- | :--- |
| **1. Consultar Disponibilidad** | El usuario accede al portal interactivo o módulo de calendario. | Visualización clara de la matriz/grid de horarios libres. | El usuario identifica un horario disponible para un fisioterapeuta específico. | • **$N_a$:** $\le 3$ clics.<br>• **$T_c$:** $\le 15$ segundos.<br>• **Tasa de Retroceso:** 0%. |
| **2. Registrar una Cita** | Selección de un bloque de horario disponible. | Despliegue de pantalla de confirmación con código de reserva. | Registro correcto en base de datos sin duplicaciones ni campos incompletos. | • **$T_c$:** $\le 90$ segundos.<br>• **$E_r$:** $\le 1$ error de digitación.<br>• **$I_h$:** 0% (Automatizado en citas estándar). |
| **3. Modificar una Cita** | Selección de una cita activa en el listado/detalle de reservas. | Recepción de la notificación de actualización de datos. | Actualización exitosa del registro (fecha, hora o terapeuta) manteniendo datos del paciente. | • **$T_a$:** $\le 45$ segundos.<br>• **$N_a$:** $\le 4$ acciones.<br>• **Pérdida de datos:** 0%. |
| **4. Cancelar una Cita** | Activación del botón 'Cancelar Cita' en el detalle de la reserva. | Mensaje de confirmación de anulación y liberación del cupo. | El cupo queda disponible inmediatamente en el calendario sin afectar el historial. | • **$N_a$:** $\le 2$ acciones.<br>• **Confirmación previa:** 100% de los casos (Alerta de prevención).<br>• **Clics accidentales:** 0%. |
| **5. Reagendar una Cita** | Solicitud de reprogramación tras o durante una cancelación. | Emisión del nuevo comprobante de reserva con el nuevo slot. | Reasignación del nuevo slot conservando la historia clínica y datos personales sin reescribir. | • **$T_c$:** $\le 60$ segundos.<br>• **$E_r$:** 0 errores de re-ingreso de datos.<br>• **Eficacia:** 100% de éxito en la transacción. |

---

## 4. Fórmulas de Medición y Procedimiento de Recolección

### Fórmulas Cuantitativas
1. **Reducción de Tiempo de Intervención Administrativa:**
   $$\Delta T_a = \frac{T_{a,\text{AS-IS}} - T_{a,\text{TO-BE}}}{T_{a,\text{AS-IS}}} \times 100\%$$
2. **Tasa de Automatización (Efectividad del Autoservicio):**
   $$I_h (\%) = \left( \frac{\text{Citas procesadas automáticamente}}{\text{Total de citas agendadas}} \right) \times 100\%$$
3. **Tasa de Errores por Operación:**
   $$E_r = \frac{\text{Número total de errores o reprocesos observados}}{\text{Número total de operaciones ejecutadas}}$$

### Procedimiento de Medición
* **Instrumento:** Registro de métricas interactivo mediante sesiones de pruebas de usabilidad guiadas y logs de interacción de la plataforma (telemetría de interfaz).
* **Entorno de Evaluación:** Pruebas de usabilidad con usuarios representativos (pacientes y personal administrativo del centro) ejecutando las 5 operaciones fundamentales sobre el prototipo interactivo.