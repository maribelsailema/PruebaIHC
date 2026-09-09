# Actividad 8: Recomendación Final y Conclusiones del Diagnóstico e Intervención HCI

## 1. Dictamen de la Intervención
Con base en los análisis comparativos entre el sistema AS-IS (mecanismo tradicional) y la propuesta TO-BE (prototipo interactivo basado en estándares HCI), se emite un **dictamen favorable** para la adopción e implementación del nuevo sistema de agendamiento digital.

---

## 2. Argumentación Técnica y Justificación

1. **Eficiencia Operativa:**
   La reducción del tiempo de atención en un **75%** (de 120s a 30s) descongestiona significativamente los canales de atención del centro médico y optimiza la productividad del personal.

2. **Mitigación del Error Humano:**
   Las validaciones sintácticas en tiempo real y el diseño en forma de *Stepper Wizard* eliminaron por completo las inconsistencias en la captura de datos ($TER = 0\%$).

3. **Inclusividad y Accesibilidad:**
   La incorporación de contrastes adecuados, tipografía legible y soporte de navegación por teclado garantiza el cumplimiento de los lineamientos **WCAG 2.1 nivel AA**, permitiendo que personas con limitaciones visuales o motoras operen la interfaz de forma autónoma.

4. **Adopción de Metáforas Visuales:**
   El uso del semáforo visual para mostrar la disponibilidad de citas redujo la carga cognitiva de los operadores, permitiéndoles interpretar estados de ocupación de forma instantánea.

---

## 3. Recomendaciones de Implementación Futura

* **Fase 1 (Corto Plazo):** Integrar el prototipo validado con la base de datos central de historias clínicas (EHR) mediante APIs RESTful.
* **Fase 2 (Mediano Plazo):** Habilitar un canal omnicanal de autoagendamiento para pacientes vía aplicación web/móvil, manteniendo los mismos principios HCI evaluados.
* **Fase 3 (Largo Plazo):** Implementar un módulo de notificaciones push y recordatorios automáticos por SMS/WhatsApp 24 horas antes de la cita para reducir el ausentismo.

---

## 4. Conclusión
La rediseño centrado en el usuario transforma una tarea administrativamente costosa en un proceso automatizado, intuitivo y altamente confiable, cumpliendo rigurosamente con los objetivos de usabilidad, accesibilidad y eficiencia exigidos en el ámbito de la Interacción Humano-Computador.