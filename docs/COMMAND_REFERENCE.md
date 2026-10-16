# SETS — Referencia de comandos

**Framework:** SETS — Software Engineering Training System  
**Base:** v1.3.1  
**Alcance:** transversal a las disciplinas (Java, Kafka, Arquitectura de Software, etc.).

> Los comandos son **convenciones escritas en el chat**, interpretadas por las instrucciones de SETS. No son comandos nativos de ChatGPT ni ejecutables instalados. Se puede pedir lo mismo en lenguaje natural.

## 1. Sintaxis y convenciones

- `/<comando> <argumento>`: argumento necesario para enfocar la actividad; si falta, SETS solicita el dato mínimo imprescindible o propone un contexto razonable cuando sea seguro hacerlo.
- `[argumento]`: argumento opcional; SETS elige un tema a partir de la disciplina y el estado conocido cuando no se indique.
- **Una interacción significativa por turno:** en evaluaciones, retos y entrevistas, formular una pregunta o decisión y esperar respuesta antes de avanzar.
- **Tutoría, no teatro:** ofrecer explicaciones cuando se pidan; no convertir todo en evaluación.
- **Evidencia ≠ exposición:** completar una lectura o recibir la solución no demuestra dominio. Registrar ayuda H0–H4 y solo evaluaciones sustentadas en respuestas observadas.

## 2. Inicio, progreso y continuidad

| Comando | ¿Para qué sirve? | Ejemplo | Qué esperar |
|---|---|---|---|
| `/start` | Inicia un diagnóstico breve de la **disciplina configurada**. | `/start` | Una primera tarea o pregunta relevante, no un cuestionario completo; espera tu respuesta. |
| `/status` | Muestra progreso, evidencias, brechas y próximo objetivo, sin inventar calificaciones. | `/status` | Resumen del estado disponible; señala datos no evaluados o desactualizados. |
| `/close` | Cierra una sesión **con persistencia propuesta**. | `/close` | Resumen, `LAST_HANDOFF.md` completo según su plantilla, `LEARNING_STATE.md` completo actualizado y **nuevas entradas** para `EVIDENCE_LOG.md`. |
| `/close brief` | Obtiene un resumen provisional cuando no quieres preparar todos los archivos. | `/close brief` | Cierre ligero; **no** equivale a haber guardado el estado y **no** reemplaza `/close`. |
| `/resume` | Reanuda desde el estado y último handoff disponibles. | `/resume` | Verifica coherencia de sesiones/evidencias y propone el siguiente paso; indica ausencias o discrepancias en vez de inventar continuidad. |

**Flujo recomendado:** primera conversación `/start` → entrenamiento → `/close` → revisar y guardar archivos en GitHub y actualizar fuentes del Proyecto de ChatGPT → nueva conversación `/resume`.

**Alcance real de `/close`:** SETS **prepara** los resultados. No escribe automáticamente en GitHub ni sustituye las fuentes del Proyecto salvo que se utilice y compruebe una integración de escritura. Evita añadir dos veces una evidencia con el mismo ID. `EVIDENCE_LOG.md` es acumulativo: se agregan solo las nuevas entradas, sin borrar el historial.

## 3. Aprender, practicar y comprobar

| Comando | ¿Para qué sirve? | Ejemplo | Qué esperar |
|---|---|---|---|
| `/learn <tema>` | Aprender un concepto desde sus fundamentos, con ejemplos y práctica adaptada. | `/learn inyección de dependencias` | Modelo mental útil, explicación clara y una actividad de comprobación. |
| `/deep <tema>` | Profundizar en mecanismos internos, límites, casos límite y modos de fallo. | `/deep JVM Garbage Collection` | Análisis de funcionamiento, supuestos, comportamiento y trade-offs técnicos. |
| `/lab <tema>` | Entrenar implementando, probando o diagnosticando una solución. | `/lab retries e idempotencia con Spring` | Enunciado, criterios de éxito, entregables y retroalimentación; no solución anticipada. |
| `/quiz <tema>` | Comprobar recuperación de conocimiento y aplicación a casos nuevos. | `/quiz patrones de diseño` | Preguntas adaptativas **una por turno**, evaluación después de cada intento. |
| `/explain` | Solicitar una explicación directa del problema o concepto en curso. | `/explain` o `/explain idempotencia` | Explicación comprensible sin obligarte a adivinar mediante preguntas; luego puede ofrecer una comprobación opcional. |
| `/hint` | Solicitar **una** pista gradual durante un reto. | `/hint` | La ayuda mínima útil; registra nivel H1–H4 si afecta la evidencia. |
| `/challenge` | Elevar la dificultad del problema en curso. | `/challenge` | Nueva restricción, contraejemplo, fallo o caso de transferencia; no dificultad arbitraria. |
| `/reflect` | Revisar críticamente el propio razonamiento y las decisiones tomadas. | `/reflect` | Preguntas concretas de autocrítica, supuestos y aprendizaje, sin atribuirte decisiones que no hiciste. |

**Nota sobre `/hint` en entrevistas:** una pista puede cambiar el ejercicio de evaluación independiente a ejercicio asistido. SETS debe advertirlo y tratarlo como evidencia diferente; nunca penalizar pedir ayuda como si fuera un defecto personal.

## 4. Diseñar, decidir y revisar

| Comando | ¿Para qué sirve? | Ejemplo | Qué esperar |
|---|---|---|---|
| `/design <sistema>` | Taller de diseño de sistemas o componentes con requisitos y restricciones. | `/design servicio de reservas` | Preguntas de alcance, atributos de calidad, alternativas y validación; no arquitectura definitiva inventada. |
| `/decision <problema>` | Practicar decisiones técnicas, comparando alternativas y trade-offs. | `/decision usar Redis o PostgreSQL para sesiones` | Criterios explícitos, riesgos, objeciones fundamentadas y defensa de la opción. |
| `/review <código/arquitectura>` | Revisar código, diseño, diagrama o propuesta técnica. | `/review este diseño de API` + artefacto | Hallazgos priorizados con impacto, evidencia, riesgos y mejoras justificadas. Si falta el material, solicitarlo. |
| `/incident <escenario>` | Simular un incidente y entrenar diagnóstico por evidencias. | `/incident el p95 de una API se duplicó` | Hipótesis, métricas y mitigación segura antes de conclusiones o cambios irreversibles. |
| `/adr <decisión>` | Documentar una decisión arquitectónica cuando aporte valor. | `/adr persistencia para el catálogo` | ADR con contexto, alternativas, decisión, consecuencias y supuestos; pedir información faltante sin inventarla. |

**Regla:** estos modos también sirven para Java, datos, infraestructura o cloud. No imponer microservicios, diagramas ni ADR en problemas donde no ayudan.

## 5. Preparación profesional

| Comando | ¿Para qué sirve? | Ejemplo | Qué esperar |
|---|---|---|---|
| `/interview [tema]` | Simular una entrevista técnica, con preguntas y repreguntas. | `/interview arquitectura hexagonal` o `/interview` | Una pregunta por turno, sin pistas durante la simulación salvo que se decida salir del modo de evaluación; debrief fundamentado. |
| `/sprint` | Priorizar estudio para una entrevista o meta próxima **cuando la disciplina la tenga configurada**. | `/sprint` | Plan adaptado al plazo real, alcance y brechas demostradas; puede preguntar por fecha si falta. |

## 6. Combinaciones útiles (ejemplos de conversación)

**Aprender una tecnología nueva:**

```text
/learn Apache Kafka
/deep particiones y consumer groups
/lab consumidor idempotente
/quiz idempotencia
/close
```

**Entrenar criterio de arquitectura:**

```text
/design plataforma de comercio electrónico
/decision monolito modular versus microservicios
/challenge
/adr estrategia de despliegue
/close
```

**Prepararte para la entrevista:**

```text
/sprint
/interview system design
/reflect
/close
```

> Estos bloques son **ejemplos de mensajes separados**, no órdenes a ejecutar todas de una vez. Sigue el ritmo de la conversación.

## 7. Qué hacer si falta un archivo o algo no cuadra

- Si no existe `LAST_HANDOFF.md` real, `/start` puede iniciar la primera sesión; `/resume` utiliza el estado disponible y declara la falta de handoff.
- Si `LEARNING_STATE.md`, `EVIDENCE_LOG.md` y `LAST_HANDOFF.md` discrepan, no duplicar registros ni inventar sesiones. Pedir comprobación del estado antes de afirmar continuidad.
- Si el usuario pide `/status` sin evidencias, informar **No evaluado**; no asignar un nivel por la experiencia declarada.
- Si un comando exige un artefacto inexistente (`/review`), pedir lo mínimo necesario; no fingir que se revisó un documento.
- Una petición en lenguaje natural como «ponme un reto más difícil» equivale a `/challenge`; «explícame desde cero» equivale a `/explain` o `/learn`, según el caso.

## 8. Mantenimiento del catálogo

`core/PROJECT_INSTRUCTIONS.md` es el **contrato operativo** que interpreta los comandos; este documento es su **referencia explicativa**. Si se añade, cambia o elimina un comando, actualiza ambos archivos en el mismo cambio y revisa el setup de los proyectos que consumen SETS. No crear comandos adicionales implícitos solo por documentar ejemplos.
