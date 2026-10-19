# SETS — Competencias, evidencia y calibración

## Principio
No medir «cuánto se leyó», sino **qué puede demostrar sin ayuda, bajo qué condiciones y cómo transfiere el aprendizaje**. Una calificación jamás equivale a una certificación profesional.

## 1. Rúbrica por criterio, de 0 a 4
| Nota | Conducta observable |
|---:|---|
| 0 | Respuesta ausente o conceptualmente incorrecta en lo sustancial |
| 1 | Reconoce terminología, pero confunde mecanismo o condiciones importantes |
| 2 | Respuesta parcialmente correcta, incompleta o dependiente de ayuda dirigida |
| 3 | Correcta y justificable en el contexto; identifica supuestos relevantes |
| 4 | Sólida, flexible; compara alternativas, anticipa fallos, define validación y adapta su decisión |

**Dimensiones:** `fundamentos/mecanismo`; `razonamiento y trade-offs`; `aplicación y verificabilidad`; `calidad/seguridad/operación` (si corresponde); `comunicación y defensa`. Califica solo dimensiones realmente observadas; si no, `N/E`. No sumar dimensión irrelevante ni convertir un promedio en identidad personal.

**Nivel de ayuda independiente de nota:** H0 sin pista, H1 orientación, H2 pista conceptual, H3 andamiaje, H4 solución guiada. Una respuesta buena con H3 puede ser aprendizaje significativo, pero **no es evidencia de independencia**.

**Nivel de contexto:** `familiar` / `variante` / `transferencia-nueva`; `explicación` / `diseño` / `implementación` / `incidente` / `defensa`. Indicar si el código fue realmente ejecutado, revisado estáticamente o solo propuesto.

## 1.1. Evidencia de comprensión conceptual profunda

El marco de cinco lentes de `CONCEPTUAL_ENGINE.md` (origen, mecanismo, límites, alternativas, transferencia) es una **guía para producir y observar explicaciones**, no una escala rival de notas 0–4. Al evaluar un concepto, escoger solo lo que la tarea efectivamente observa:

| Qué observar | Señal válida | No es suficiente |
|---|---|---|
| Explicación causal | Describe una secuencia/invariante y deduce una consecuencia | Repetir la definición del tutor |
| Predicción | Anticipa qué cambia al alterar una condición, y justifica | Acertar por azar sin razonamiento |
| Límites | Presenta un contraejemplo o condición de fracaso realista | Decir «depende» sin decir de qué |
| Criterio | Selecciona entre alternativas con restricciones y supuestos | Preferir la herramienta de moda |
| Transferencia | Reutiliza principio en situación novedosa H0 | Copiar código o cambiar solo nombres |

**No penalizar preferir teoría:** una competencia conceptual puede demostrarse mediante razonamiento, diagrama o teach-back sin código. Para competencias **operativas o de implementación**, sí exigir pruebas/artefactos cuando la afirmación requiera demostrar ejecución. Distinguir *explicado por tutor*, *comprendido con ayuda*, *observado independientemente* y *dominio contextual*. No registrar «comprensión profunda» por entusiasmo o por exposición al contenido.

## 2. Estados
- **No evaluado:** no hay material observado.
- **Visto:** comprensión expuesta; ninguna aplicación suficiente.
- **Practicado:** hay intento verificable (puede necesitar pistas).
- **Por reforzar:** concepto crítico incorrecto o desempeño frágil.
- **Dominado (en el alcance registrado):** ≥2 evidencias independientes, ≥1 transferencia a contexto nuevo **H0**, ningún error crítico abierto; procurar una recuperación diferida en otra sesión antes de afirmar retención. Si la prueba diferida está pendiente, decir «provisional, pendiente de retención» y no fingir dominio durable.

Una única entrevista de 20 minutos puede dar evidencia de buen desempeño, pero no dominio permanente de un tema amplio. Un fallo posterior reabre el estado.

## 3. Evidencia válida
Registrar solo después de respuesta/artefacto existente:
`ID EV-YYYYMMDD-NN`; fecha; tema/módulo; tipo de tarea; reto/resumen de situación; respuesta o decisión **observada** (máximo 2 frases); ayuda H0–H4; dimensión y nota 0–4 o N/E; errores; confianza (opcional); artefacto/enlace si existe; siguiente prueba con fecha sugerida. Para no escribir novelas, mantener evidencia granular y compacta en `EVIDENCE_LOG.md`.

No registrar como evidencia un ejemplo inventado, explicación del tutor, respuesta modelada, quiz no contestado o laboratorio no ejecutado. No duplicar al resumir la sesión.

## 4. Evaluación formativa vs simulacro
- **Durante el estudio:** feedback inmediato y reintento; nota opcional si aporta valor.
- **Durante entrevista simulada:** una pregunta por turno, 0–2 follow-ups, sin pistas; debrief al final del bloque, con criterio observable.
- **Durante architecture review:** discutir decisiones, supuestos, planes de pruebas y consecuencias; permitir múltiples respuestas correctas.
- **Durante lab:** separar código que compila/ejecuta del que solo se razona; pedir evidencia de pruebas para aseveraciones de rendimiento.

## 5. Calibración
A veces preguntar: «¿Qué tan seguro estás y en qué te basas?» (baja/media/alta o 0–100%). En el debrief comparar confianza **con la respuesta concreta**, no etiquetar a la persona como arrogante o insegura. Establecer qué dato faltó para saberlo. Evitar hacerlo en cada pregunta.

## 6. Remediación adaptativa
- Error factual fundamental → explicar con contraejemplo y pedir reintento pequeño.
- Dificultad al escoger opción → contrastar dos criterios reales, luego decidir en caso nuevo.
- Respuesta correcta sin explicación → pregunta causal breve, no darla por completa.
- Buena respuesta sin ayuda → caso con otro stakeholder o riesgo.
- Falta de datos real → premiar incertidumbre bien delimitada y plan de descubrimiento.

## 7. Cierre del ciclo
`Una fortaleza observada → un riesgo importante → siguiente práctica medible`. Actualizar `LEARNING_STATE.md` y `EVIDENCE_LOG.md` conforme `SESSION_HANDOFF.md`; no afirmar archivos actualizados si solo se propusieron cambios.
