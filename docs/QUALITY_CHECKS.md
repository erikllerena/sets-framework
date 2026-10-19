# SETS — Acceptance checks del propio framework

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
| Q18 Enseñar antes de producir | `/start`, responder diagnóstico y continuar | Explica concepto según brecha: mecanismo, ejemplo y límite; no propone `/lab` como paso obligatorio |
| Q19 Mecanismo causal | `/deep concurrencia` | Sigue estados o flujo, expresa invariantes y permite predecir una consecuencia; no solo definiciones |
| Q20 No convertir en examen | «Quiero entender primero por qué» | Explica de forma suficiente; pregunta de verificación solo cuando aporta y se pueda posponer |
| Q21 Diferenciar modelos | «Explícame Kafka como una oficina de correos» | Advierte dónde falla la analogía frente a semántica de entrega/consumo |
| Q22 Comparación sin dependencia | «Explícalo en Java y TypeScript» | Señala principio invariante y detalles específicos; no fuerza dominar ambos stacks ni otra disciplina |
| Q23 Razonamiento sin código | «No quiero lab, solo entender consistencia» | Utiliza caso de estados o predicción, no considera lectura como dominio probado |
| Q24 Teach-back con precisión | «Voy a explicárselo a un CTO» | Evalúa impacto, riesgos y claridad, no exige detalles internos innecesarios |
| Q25 Mapa opcional | `/close` sin CONCEPT_MAP | Genera solo los tres artefactos obligatorios; no inventa mapa ni cuarta salida |
| Q26 Respeto a dominios aislados | Proyecto frontend y analogía con backend | Enseña lo necesario en contexto, no importa progreso de otro proyecto |

## Señales de que debemos cambiar SETS
- El tutor escribe mucho y pregunta poco o pregunta sin enseñar.
- Siempre favorece las mismas tecnologías o un diagrama largo.
- Convierte cualquier tema (por ejemplo, JVM o algoritmos) en preguntas de arquitectura sin necesidad.
- Califica «dominio» con una respuesta a un problema ya revelado.
- Pide más documentación de la que la práctica justifica.
- Reporta avances inventados o imposible verificar el estado entre chats.
- La entrevista se siente como trivia y no entrena decisiones.
- El usuario no puede explicar **por qué** la opción elegida vencería a la rival.

## Criterios de calidad para probar el motor conceptual
Para Q18–Q26, el evaluador debe registrar: `OK / Falla / Sin probar`, evidencia textual breve y **una sola hipótesis de mejora** cuando falle. No confundir que una conversación suene agradable con un desempeño pedagógico medido. No afirmar que los checks ya pasaron por haberlos escrito.

## Iteración de producto
Recoger 2 problemas observados → formular hipótesis de mejora → modificar uno o dos archivos relevantes → repetir mismo test en una sesión futura. Evitar cambiar todo el sistema por un caso aislado.
