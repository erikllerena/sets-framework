# Actualización del framework — SETS 1.3.2 → 1.4.0

## Cambios técnicos

**Nuevos**: `core/CONCEPTUAL_ENGINE.md`, `templates/CONCEPT_MAP.template.md`, este documento.

**Modificados**: `core/PROJECT_INSTRUCTIONS.md`, `core/INTERACTION_ENGINE.md`, `core/PRACTICE_ENGINE.md`, `core/ASSESSMENT_ENGINE.md`, `core/DECISION_ENGINE.md`, `templates/PROJECT_CONFIG.template.yaml`, `docs/QUALITY_CHECKS.md`, `docs/COMMAND_REFERENCE.md`, `docs/LEARNING_SCIENCE.md`, `core/SESSION_HANDOFF.md` (solo encabezado), `docs/EXAMPLE_SESSION.md` (solo encabezado), `README.md`, `CHANGELOG.md`.

**Sin cambio en contrato**: `core/SESSION_HANDOFF.md`, `templates/LAST_HANDOFF.template.md`, `templates/EVIDENCE_LOG.template.md`, `templates/LEARNING_STATE.template.md`, `docs/REFERENCE_POLICY.md`, nombres y semántica de comandos. **No hay que reiniciar progreso para actualizar el framework.**

## Orden recomendado para cuatro repositorios

1. Actualiza **`sets-framework`** con este paquete; conserva su historial de Git.
2. Después actualiza **`sets-software-architecture`**, su `CHATGPT_PROJECT_INSTRUCTIONS.md` y su `SETUP_CHATGPT.md` para referenciar `CONCEPTUAL_ENGINE.md`. Carga el nuevo motor como **fuente del Proyecto de ChatGPT** y reemplaza las fuentes de motores modificados.
3. Repite con **`sets-backend-architecture`** y luego **`sets-frontend-architecture`**, cada uno con su propia configuración, memoria, preferencias de ejemplos y currículo, sin copiar estados académicos entre ellos.
4. Si decides mantener un mapa conceptual, crea `state/CONCEPT_MAP.md` **dentro de ese repositorio de disciplina** desde la plantilla; no lo crees en `sets-framework` con información del estudiante.

> **Nota:** actualizar GitHub no actualiza automáticamente las fuentes ni las instrucciones activas en ChatGPT. Hasta completar los pasos 2–3, el proyecto puede comportarse con la versión anterior del motor.

## Contratos que no deben romperse

- El sistema de evaluación 0–4, H0–H4 y las evidencias acumulativas siguen siendo los mismos. Las cinco lentes conceptuales **NO** crean otra escala.
- `/close` continúa entregando SOLO los tres artefactos obligatorios (`LAST_HANDOFF.md`, `LEARNING_STATE.md`, delta de `EVIDENCE_LOG.md`). El mapa de conceptos es opcional y no forma parte del cierre estándar.
- No asumir que el usuario conoce Angular, React, Java, Go u otra tecnología; elegir demostraciones por su utilidad dentro de cada proyecto.
- Ante `/learn`: enseñanza conceptual primero; ante `/lab` explícito: ejecutar laboratorio con la ayuda necesaria; ante `/interview`: no revelar respuestas antes del intento.

## Comprobación sugerida

Desde una conversación de prueba dentro del proyecto, pedir: «Enséñame por qué existe la idempotencia, qué mecanismo la hace posible, qué no garantiza y cómo diferenciarías ese principio entre Java y otro stack. Sin laboratorio». Debería explicar conceptualmente, mostrar un límite real y **no** fabricar evidencia de ejecución.
