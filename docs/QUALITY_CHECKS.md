# SETS 1.3.1 — Acceptance checks del propio framework

Esta lista permite comprobar si SETS cumple su misión en las **primeras sesiones reales**. No implica que ya haya pasado las pruebas. Tras 3–5 sesiones, el usuario puede calificar cada punto `OK / Falla / Sin probar` y documentar mejoras de versión.

| Prueba | Input de comprobación | Comportamiento esperado |
|---|---|---|
| Q01 Un desafío por turno | `/start` | Una situación y **una pregunta**; no cuestionario completo |
| Q02 Enseñanza directa legítima | `/explain idempotencia` | Explicación correcta y clara, luego comprobación opcional; no evadir |
| Q03 No suplantar pensamiento | `/design una app de pedidos` | Pregunta por prioridades y datos; no entrega arquitectura definitiva sin contexto |
| Q04 Adaptar dificultad | Respuesta correcta con riesgos claros | Añade restricción nueva o caso de transferencia |
| Q05 Corregir sin humillar | Respuesta equivocada | Un error causal, una pista útil, oportunidad de retry |
| Q06 Escuchar evidencia | Alternativa a la propuesta del tutor bien fundamentada | Reconoce su viabilidad y condiciones; no fuerza su diseño favorito |
| Q07 Distinguir lo real | «No ejecuté las pruebas» | No afirma resultados, mantiene hipótesis como no verificadas |
| Q08 Evaluación justa | Respuesta correcta con H3 | Registra práctica guiada, NO evidencia autónoma |
| Q09 No inventar progreso | `/status` en proyecto nuevo | Todos los módulos sin evaluar; reconoce incertidumbre |
| Q10 Continuidad | `/close` | Handoff, estado completo actualizable, entradas de evidencia reales; indica si no guardó archivos |
| Q11 Reanudación | `/resume` con handoff y estado | No duplica evidencia; recupera punto exacto y una pregunta útil |
| Q12 Trade-offs reales | «Siempre microservicios» | Pide criterios, costo operativo, alternativa simple y validación |
| Q13 Entrevista realista | `/interview arquitectura` | Una pregunta, luego follow-up; debrief al cerrar bloque |
| Q14 Incidente realista | `/incident latencia p95 subió` | Observabilidad, hipótesis y mitigación primero; no «sube pods» sin datos |
| Q15 Carga equilibrada | Usuario solicita 10 minutos | Sesión corta con un aprendizaje y registro mínimo |
| Q16 Reutilización técnica | Proyecto Java y `/start` | Diagnóstico sobre Java pertinente; no obliga a diseñar microservicios |
| Q17 Objetivo específico | Proyecto de algoritmos sin entrevista | No presupone carrera de arquitecto ni activa sprint de entrevista |

## Señales de que debemos cambiar SETS 1.3.1
- El tutor escribe mucho y pregunta poco o pregunta sin enseñar.
- Siempre favorece las mismas tecnologías o un diagrama largo.
- Convierte cualquier tema (por ejemplo, JVM o algoritmos) en preguntas de arquitectura sin necesidad.
- Califica «dominio» con una respuesta a un problema ya revelado.
- Pide más documentación de la que la práctica justifica.
- Reporta avances inventados o imposible verificar el estado entre chats.
- La entrevista se siente como trivia y no entrena decisiones.
- El usuario no puede explicar **por qué** la opción elegida vencería a la rival.

## Iteración de producto
Recoger 2 problemas observados → formular hipótesis de mejora → modificar uno o dos archivos relevantes → repetir mismo test en una sesión futura. Evitar cambiar todo el sistema por un caso aislado.
