# SETS — LAST_HANDOFF (plantilla oficial)

> **Plantilla, no una sesión real.** Este archivo pertenece a `sets-framework/templates/`.
> No lo confundas con `state/LAST_HANDOFF.md`: este último pertenece a cada disciplina y solo
> debe sustituirse por un cierre real producido mediante `/close`. Sustituye los marcadores
> entre `[...]`; elimina instrucciones y ejemplos antes de guardar un handoff real.

## 1. Identificación
- **session_id:** `[SETS-AAAAMMDD-NN]`
- **Fecha de cierre:** `[AAAA-MM-DD]`
- **Disciplina / repositorio:** `[identificador]`
- **Track y módulo:** `[inmediato/permanente, módulo o competencia]`
- **Versión del framework:** `[versión realmente utilizada]`

## 2. Objetivo y trabajo realmente realizado
- **Objetivo de la sesión:** `[objetivo explícito]`
- **Realizado:** `[actividad, reto o tema realmente tratado]`
- **Pendiente o no ejecutado:** `[elementos que NO se hicieron; o «Ninguno»]`

## 3. Resultado del aprendizaje
- **Aprendizajes principales (máximo 3):** `[solo conclusiones respaldadas por la sesión]`
- **Fortalezas observadas:** `[hechos observables, o «Sin evidencia suficiente»]`
- **Vacíos / errores relevantes (máximo 2):** `[o «No evaluados»]`
- **Ayuda requerida:** `[H0–H4, por reto si corresponde; o «No evaluado»]`
- **Riesgos / incertidumbres:** `[aspectos no verificados o «Ninguno identificado»]`

## 4. Evidencias de competencia

| EV-ID | Competencia / reto | Evidencia observable | Ayuda (H0–H4) | Evaluación / límite |
|---|---|---|---|---|
| `[EV-AAAAMMDD-NN]` | `[competencia]` | `[qué hizo efectivamente el estudiante]` | `[H#]` | `[resultado, condición o limitación]` |

> Si no hubo intento evaluable, sustituir la tabla de ejemplo por:
> **Sin evidencia evaluable en esta sesión.** No crear IDs de evidencia en ese caso.
> Incluir solo EV-ID nuevos, contrastados con `state/EVIDENCE_LOG.md`. No copiar evidencias
> anteriores como nuevas. Si no se pueden verificar IDs, indicar el conflicto y solicitar validación.

## 5. Decisiones y artefactos
- **Decisiones tomadas:** `[decisión + argumento esencial, o «Ninguna»]`
- **Artefactos reales:** `[rutas de ADR, código, diagrama, laboratorio, etc., o «Ninguno»]`
- **Estado de verificación:** `[ejecutado / revisado / propuesto / no ejecutado]`

## 6. Continuidad y próxima sesión
- **Último `session_id` que debe quedar integrado en `LEARNING_STATE.md`:** `[session_id de esta sesión, una vez persistido]`
- **Tema o competencia para continuar:** `[prioridad]`
- **Siguiente acción concreta:** `[un ejercicio/desafío específico]`
- **Pregunta de recuperación:** `[una pregunta sin responder para el próximo inicio, o «No aplica»]`
- **Repaso sugerido:** `[fecha orientativa o «Por determinar»; no constituye recordatorio programado]`
- **Bloqueos o datos a confirmar:** `[o «Ninguno»]`

## 7. Persistencia verificada
- **`state/LAST_HANDOFF.md`:** `[propuesto / guardado y verificado / desconocido]`
- **`state/LEARNING_STATE.md`:** `[propuesto / guardado y verificado / desconocido]`
- **`state/EVIDENCE_LOG.md`:** `[sin cambios / delta propuesto / guardado y verificado / desconocido]`
- **GitHub:** `[no actualizado / commit verificado: <hash> / desconocido]`
- **Archivos del Proyecto de ChatGPT:** `[no actualizados / actualización verificada / desconocido]`

**Declaración de persistencia:** **Cambios propuestos; no guardados todavía en archivos del Proyecto/GitHub.**

> Conservar esa declaración por defecto. Solo cambiarla después de comprobar las operaciones
> reales de escritura en cada destino. Generar texto o archivos descargables no equivale a haber
> actualizado GitHub ni los archivos adjuntos del Proyecto de ChatGPT.

---

### Comprobaciones antes de emitir un `LAST_HANDOFF.md` real

1. `session_id` único respecto a historial accesible; si no puede verificarse, pedir confirmación.
2. Todas las evidencias pertenecen a esta sesión y son observables; no inventar evaluaciones.
3. `LEARNING_STATE.md` y el delta de `EVIDENCE_LOG.md` coinciden con este handoff y no duplican IDs.
4. Identificar claramente ejercicios no realizados y artefactos no ejecutados.
5. Conservar explícito qué está **propuesto** y qué realmente fue **guardado y verificado**.
6. Al iniciar `/resume`, contrastar el `session_id` con `LEARNING_STATE.md`; si ya está integrado,
   **no volver a aplicar** sus evidencias. Ante discrepancias, preguntar antes de fusionar.
