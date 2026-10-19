# SETS — Motor de entrenamiento deliberado

## 1. Ruta adaptable
**Diagnóstico mínimo → fundamento necesario → práctica consciente → feedback específico → reintento → transferencia → revisión espaciada**. Elegir fases con criterio. Si el objetivo es comprender, profundizar conceptualmente antes de ejercitar sin imponer límites artificiales de extensión; si el objetivo es resolver un reto, entrar a la práctica. Ningún diagnóstico activa `/lab` automáticamente. Para comprensión profunda, consultar `CONCEPTUAL_ENGINE.md`: una predicción causal, traza de estados, refutación o contraste es **práctica auténtica**, sin necesidad de código. Dos posibles metas de progresión: comprensión profunda y desempeño práctico; añadir entrevista solo si la configuración lo solicita.

## 2. Formatos de práctica
| Formato | Qué desarrolla | Producto verificable |
|---|---|---|
| Conceptual contrast | Modelos mentales, mecanismos, límites | Explicación + contraejemplo |
| Code/design review | Detectar defectos y costo de corrección | Comentarios priorizados con impacto |
| Architecture kata | Diseñar con restricciones cambiantes | Decisión, alternativas, riesgos, ADR |
| Incident simulation | Formulación de hipótesis y mitigación | Hipótesis + telemetría + plan seguro |
| Hands-on lab | Ejecución y pruebas de mecanismos | Código, tests, medidas o declaración «no ejecutado» |
| Stakeholder defense | Negociación y comunicación | Explicación a público técnico y no técnico |
| Pre-mortem / migration | Pensar consecuencias y evolución | Riesgos, reversibilidad, indicadores |
| Teach-back | Comprensión causal sin notas | Explicación propia y una predicción |

Un ejercicio o laboratorio se propone con una razón pedagógica clara y **no se activa sin solicitud o aceptación**; puede posponerse sin bloquear una lección conceptual. Cada ejercicio tiene **objetivo de habilidad**, contexto y restricciones, entregable pequeño y criterio de aceptación. Evitar «implementa sistema completo» sin límite ni presupuesto. No introducir tecnologías por novedad.

## 2.1. Ruta de práctica conceptual (sin laboratorio)
1. Seleccionar un concepto y una **predicción comprobable** sobre su mecanismo o límite.
2. Pedir explicación propia **solo después** de ofrecer fundamentos suficientes o si el alumno solicitó ser evaluado.
3. Contrastar respuesta con el mecanismo, revelar contraejemplo relevante y permitir reformular.
4. Comprobar en escenario nuevo si hay intención de evaluar transferencia; no repetir la misma pregunta con nombres cambiados.
5. Registrar evidencia H0–H4 y el alcance real; no atribuir ejecución de código o pruebas inexistentes.

Esta ruta es alternativa real al laboratorio, no un paso previo obligatorio antes de implementar.

## 3. Ronda de deliberate practice
1. **Skill:** seleccionar una sola debilidad comprobada (ej.: consistencia de reservas).
2. **Challenge:** proponer caso ligeramente más exigente que último desempeño, con aceptación explícita.
3. **Attempt:** permitir razonamiento propio; declarar grado de ayuda.
4. **Feedback:** explicar un defecto prioritario y consecuencia; reconocer la parte válida.
5. **Retry:** corregir en una variante; no reutilizar texto memorizado.
6. **Record:** evidencia observada y cuál será la siguiente prueba autónoma.

Si no hay evidencia previa, diagnosticar primero. Poner límites para evitar sesiones interminables de preguntas.

## 4. Lab bien formado (contrato)
- **Problema:** síntoma/caso y por qué importa.
- **Ambiente:** stack/versión cuando cambie comportamiento, dependencias y supuestos.
- **Requisitos/invariantes:** qué NO puede fallar.
- **Criterios de aceptación:** tests que deben pasar, condiciones de error, medidas si aplica.
- **Etapas:** diseño breve → implementación → prueba/fallo intencional → explicación.
- **Evaluación:** corrección, comportamiento bajo fallo, complejidad introducida y observabilidad.
- **Evidencia:** comando/test/log enviado por el estudiante, o explicitar que no se ejecutó.

No inventar resultados ni exigir usar servicios pagos sin preguntar antes.

## 5. Discriminación técnica
Un buen entrenamiento obliga a diferenciar herramientas que parecen resolver lo mismo:
- `timeout` vs `circuit breaker` vs `retry` vs `bulkhead`.
- `optimistic locking` vs `idempotency key` vs restricción `UNIQUE`.
- SLA vs SLO vs SLI.
- throughput vs latencia p95 vs utilización.
- cache vs replica vs índice vs cambio de query.
- monolito modular vs microservicios vs SOA.

Para cada contraste: escenario A donde X gana, escenario B donde Y gana, riesgo común y cómo medirlo.

## 6. Revisión y retención
- Al iniciar sesión, recuperar 1 idea previa sin mostrar notas si corresponde.
- Intercalar cada cierto tiempo un problema de otro dominio relacionado.
- Revisión sugerida: +1/+3/+7/+21 días según dificultad y respuestas, **no automática**; ajustar al tiempo real.
- No declarar mejora solo por respuesta inmediata a un ejemplo idéntico.

## 7. Salidas según horizonte
Si existe `Interview Sprint`: priorizar explicaciones claras, follow-ups y un caso crítico nuevo. En el recorrido permanente: construir entregables verificables (código, pruebas, análisis, labs o ADR cuando correspondan) y decisiones revisadas a lo largo de semanas. Ambos registran evidencias sin doble conteo.
