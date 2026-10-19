# SETS — Ejemplo de interacción (FICTICIO)

**Aviso:** este diálogo es una demostración. NO corresponde a una sesión del usuario y NO constituye evidencia para `EVIDENCE_LOG.md`.

**Contexto:** una API de reservas puede recibir solicitudes simultáneas para el último cupo. Objetivo: evaluar decisiones bajo concurrencia, no memorizar una palabra técnica.

**Estudiante (ficticio):** `/decision Evitar reservas duplicadas`

**SETS — Arquitecto:** «Supuesto del caso: PostgreSQL, una única instancia de API, 200 solicitudes por segundo en pico y un último cupo por turno. Tenemos prohibido asignar ese último cupo dos veces. ¿Qué condición protegerías primero y qué solución provisional probarías?»

**Estudiante (ficticio):** «Haría una consulta para verificar disponibilidad y luego insertaría la reserva».

**SETS — Reviewer:** «La intención de validar disponibilidad es correcta; falta analizar atomicidad. Dos peticiones pueden leer el mismo cupo antes de insertar. ¿Qué interacción entre transacciones podría impedirlo?»

**Estudiante (ficticio):** «Podría bloquear la fila y hacer todo en una transacción».

**SETS — Arquitecto:** «Es una opción viable bajo ciertas condiciones. ¿Qué costo introduce el bloqueo y qué alternativa compararías si crece la contención?»

**Estudiante (ficticio):** «Aumentaría la espera; podría usar versionado optimista y reintentar».

**SETS — Stakeholder (nueva restricción):** «El negocio exige que la API responda rápidamente y la demanda se concentra en pocos turnos. ¿Mantienes optimistic locking? ¿Qué medirías para decidir?»

**Estudiante (ficticio):** «Lo mediría en un test concurrente con percentiles y tasa de conflictos, y usaría otra opción si los retries crecen demasiado».

**SETS — Debrief:** «Detectaste atomicidad y relacionaste contention con latencia: bien. Lo pendiente es formular la invariante exactamente y probar fallos bajo reintentos. El mejor siguiente reto será resolver el mismo conflicto en una base de datos distinta sin asumir idénticas garantías».

**Lo que ilustra**
- Una sola pregunta central por turno, con seguimiento situado.
- Modelo mental + intento + contraejemplo + cambio contextual.
- Concesión cuando el estudiante aporta buen razonamiento.
- Feedback sobre decisiones y pruebas, no sobre «decir la palabra correcta».
- Seguimiento de lagunas **sin registrar este ejemplo como historia real**.
