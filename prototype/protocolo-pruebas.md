# Actividad 7: Protocolo de Validación de Usabilidad y Evaluación Cuantitativa

## 1. Diseño de la Prueba de Usabilidad

### 1.1 Perfil de los Participantes
La evaluación se realizó con una muestra representativa de 3 usuarios asignados al rol de operadores/agentes de agendamiento:
* **Usuario 1:** Wilson Pillapa
* **Usuario 2:** Viviana Sarco
* **Usuario 3:** Alex Guachi

### 1.2 Tarea Evaluada (Benchmark Task)
* **Objetivo:** Registrar una cita médica completa para un paciente en la especialidad de Pediatría, verificar disponibilidad en el semáforo visual, completar los datos del paciente y confirmar la emisión del ticket.

---

## 2. Resultados de las Métricas de Usabilidad

### 2.1 Tasa de Éxito ($\text{TE}$)
* **Fórmula:** $\text{TE} = \left( \frac{\text{Tareas exitosas}}{\text{Total de tareas}} \right) \times 100$
* **Sustitución:** $\text{TE} = \left( \frac{3}{3} \right) \times 100 = 100\%$
* **Resultado:** **100% de efectividad**. Todos los participantes completaron la tarea sin bloqueos.

---

### 2.2 Reducción del Tiempo de Ejecución ($\Delta T$)
* **Tiempo Promedio Sistema Legacy ($T_{anterior}$):** 120 segundos.
* **Tiempo Promedio Nuevo Prototipo ($T_{nuevo}$):** 30 segundos.
* **Fórmula:** $\Delta T = \left( \frac{T_{anterior} - T_{nuevo}}{T_{anterior}} \right) \times 100$
* **Sustitución:** $\Delta T = \left( \frac{120 - 30}{120} \right) \times 100 = 75\%$
* **Resultado:** **75% de reducción** en el tiempo promedio de atención por cita.

---

### 2.3 Clics fuera del Flujo Crítico ($COC$)
* **Fórmula:** $COC = \text{Clics Totales Realizados} - \text{Clics Mínimos Óptimos}$
* **Promedio Mínimo Óptimo:** 8 clics.
* **Promedio Registrado:** 8 clics.
* **Sustitución:** $COC = 8 - 8 = 0$
* **Resultado:** **0 clics de desviación**. El flujo navegable guía al usuario sin desvíos.

---

### 2.4 Tasa de Error de Tarea ($TER$)
* **Fórmula:** $TER = \left( \frac{\text{Campos o pasos erróneos}}{\text{Total de campos interactuados}} \right) \times 100$
* **Sustitución:** $TER = \left( \frac{0}{36} \right) \times 100 = 0\%$
* **Resultado:** **0% de tasa de error**. La presencia de validaciones y el stepper previno datos erróneos.

---

### 2.5 Índice de Intervención Manual ($IH$)
* **Fórmula:** $IH = \left( \frac{\text{Acciones manuales de corrección}}{\text{Pasos totales}} \right) \times 100$
* **Sustitución:** $IH = \left( \frac{0}{15} \right) \times 100 = 0\%$
* **Resultado:** **0% de intervención manual externa**. El proceso fue 100% asistido por la interfaz digital.

---

## 3. Resumen Consolidado de Indicadores

| Indicador | Meta Esperada | Resultado Obtenido | Estado |
| :--- | :---: | :---: | :---: |
| **Tasa de Éxito ($\text{TE}$)** | $100\%$ | $100\%$ | 🟢 Cumplido |
| **Reducción de Tiempo ($\Delta T$)** | $\ge 50\%$ | $75\%$ | 🟢 Excedido |
| **Clics Fuera de Flujo ($COC$)** | $\le 2$ | $0$ | 🟢 Cumplido |
| **Tasa de Error ($TER$)** | $\le 5\%$ | $0\%$ | 🟢 Cumplido |
| **Intervención Manual ($IH$)** | $\le 10\%$ | $0\%$ | 🟢 Cumplido |