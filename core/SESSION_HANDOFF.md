# SETS 1.3.1 — Persistencia entre conversaciones y /close

## Qué debe conseguir este protocolo
Permitir reanudar sin narrar toda la conversación; mantener **tres artefactos** en la disciplina: `LEARNING_STATE.md` = foto vigente y prioridades; `EVIDENCE_LOG.md` = historial append-only verificable; `LAST_HANDOFF.md` = último cierre para reanudar. El protocolo `SESSION_HANDOFF.md` vive en el framework y no es el archivo a reemplazar. ChatGPT Projects no implica sincronización automática de archivos. La edición manual o descarga/reemplazo es parte explícita del proceso.

## Contrato obligatorio de formato
Antes de generar un `LAST_HANDOFF.md` en cualquier disciplina, consulta
**`sets-framework/templates/LAST_HANDOFF.template.md`**, adjunto al Proyecto de ChatGPT
como **`LAST_HANDOFF.template.md`**. Ese archivo es la **plantilla oficial** y
contiene las secciones, campos obligatorios y comprobaciones de cierre.

- Si está disponible, utiliza sus encabezados y orden; sustituye todos los marcadores y no
  presentes una plantilla sin completar como si fuera un cierre real.
- Si no puedes leer el archivo, dilo y solicita adjuntarlo; no inventes que lo has consultado.
  Se puede ofrecer un resumen provisional, pero un `/close` completo requiere la plantilla.
- La plantilla vive en el **framework**; el resultado `state/LAST_HANDOFF.md` vive en la
  **disciplina**. No adjuntes al proyecto un `LAST_HANDOFF.md` vacío como si fuera historial.
- La plantilla **no sustituye** `LEARNING_STATE.md` ni `EVIDENCE_LOG.md`; los tres resultados
  de `/close` siguen siendo obligatorios.

## Al ejecutar /close (protocolo obligatorio)
1. Asignar `session_id = SETS-AAAAMMDD-NN` **único dentro del repositorio de la disciplina**, después de comparar `LEARNING_STATE.md`, `EVIDENCE_LOG.md` y `LAST_HANDOFF.md`. Si no hay historial previo, empezar por `01`. Si no puedes comprobar que el ID esté libre, pedir confirmación en vez de inventarlo. Si se migra desde SALS, conservar los IDs históricos `SALS-*` ya registrados; los nuevos usan `SETS-*`.
2. Resumir objetivo, temas realmente practicados, máximo 3 aprendizajes y riesgos, próximos pasos, y preparar el **contenido íntegro de `LAST_HANDOFF.md` siguiendo exactamente la plantilla oficial**, listo para reemplazar el cierre anterior.
3. Emitir **solo evidencias que realmente hayan ocurrido**, IDs EV únicos; si no hay intento real: «sin evidencia evaluable».
4. Preparar **actualización completa de `LEARNING_STATE.md`** lista para reemplazar el archivo anterior, preservando módulos no modificados y anotando el último `session_id` integrado; si se puede generar un archivo descargable, preferirlo sobre texto interminable.
5. Preparar **entradas nuevas para añadir a `EVIDENCE_LOG.md`**, sin duplicar existentes.
6. Dejar una pregunta de recuperación y, si procede, una fecha orientativa para repaso (no evento/reminder programado).
7. Señalar literalmente estado de persistencia: **«Cambios propuestos; no guardados todavía en archivos del Proyecto/GitHub»**, salvo que una acción de escritura real haya ocurrido y sido verificada.

## Salida breve primero
```text
SETS HANDOFF | session_id: SETS-AAAAMMDD-NN
Track / competencia: ...
Realizado: ...
Evidencias nuevas: ... (o ninguna)
Aprendizaje principal y error a reforzar: ...
Decisión/artefacto: ...
Próxima revisión: ...
Siguiente reto: ...
Estado de escritura: [propuesto / archivo descargable creado / actualizado realmente]
```

Después del resumen, ofrecer los **tres artefactos**: `LAST_HANDOFF.md` íntegro, `LEARNING_STATE.md` íntegro y delta append-only de `EVIDENCE_LOG.md`, o enlaces de descarga cuando realmente se hayan creado los archivos. No generar un archivo enorme en la respuesta por defecto si se puede proporcionar como artefacto; permitir `/close brief` como **resumen provisional sin persistencia completa**, avisando que para sincronizar archivos se requiere `/close` completo.

## Ruta práctica de guardado
1. Usuario ejecuta `/close` y recibe nuevo `LAST_HANDOFF.md`, nuevo `LEARNING_STATE.md` y entradas nuevas de evidencia.
2. Reemplaza las copias locales de `LAST_HANDOFF.md` y `LEARNING_STATE.md`; añade solo las nuevas entradas a `EVIDENCE_LOG.md`.
3. Versiona los tres en Git (opcional) y reemplaza las copias adjuntas del Proyecto de ChatGPT según las opciones disponibles allí.
4. Al cambiar de chat, el proyecto usa las copias nuevas. Si aún no se reemplazaron, pegar el último handoff manualmente.

**No confundir:** ofrecer texto o descarga ≠ haber modificado automáticamente el repositorio o los archivos del Proyecto.

## /resume en chat nuevo
«Usa `PROJECT_CONFIG.yaml`, `LEARNING_STATE.md`, `EVIDENCE_LOG.md` y, si lo adjunto, el handoff más reciente. Interpreta `LAST_HANDOFF.md` conforme a `LAST_HANDOFF.template.md`. Compara `session_id` antes de integrar una sesión. Muestra en dos frases dónde vamos, plantea una sola pregunta de recuperación si hay repaso pendiente, luego continúa con el siguiente desafío. Si hay conflictos, pregunta por la versión correcta y no inventes historial».

## Política anti-duplicación y corrección
La clave de sesión es `session_id` y la de evidencia `EV-ID`, únicas dentro del repositorio de la disciplina. No sumar dos veces una sesión reproducida por handoff y archivo actualizado. Verificar IDs en el log antes de proponer el siguiente sufijo; si la continuidad está incompleta, solicitar confirmación. Cuando se detecta corrección, conservar el registro previo y crear una nota referenciada. Preservar privacidad: no guardar transcripciones extensas, secretos, datos productivos ni información confidencial de empleadores.
