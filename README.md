# SETS Framework — v1.4.0

**SETS — Software Engineering Training System** es un framework reutilizable para entrenar competencias en ingeniería de software: comprensión profunda, programación, diseño, resolución de problemas, razonamiento crítico, evaluación con evidencias y continuidad del aprendizaje. No está limitado a arquitectura de software y no depende del framework educativo universal de otras disciplinas.

## División de responsabilidades

- **`sets-framework` (este repositorio):** motores, políticas de referencias y plantillas reutilizables, sin currículo ni progreso de una disciplina.
- **Repositorio de programa:** define su ámbito, `PROJECT_RULES.md`, configuración, currículo y progreso independientes, sin requerir otros programas.

## Estructura

```text
sets-framework/
├── core/
│   ├── PROJECT_INSTRUCTIONS.md
│   ├── CONCEPTUAL_ENGINE.md
│   ├── INTERACTION_ENGINE.md
│   ├── DECISION_ENGINE.md
│   ├── PRACTICE_ENGINE.md
│   ├── ASSESSMENT_ENGINE.md
│   └── SESSION_HANDOFF.md
├── templates/
│   ├── PROJECT_CONFIG.template.yaml
│   ├── CONCEPT_MAP.template.md
│   ├── LEARNING_STATE.template.md
│   ├── EVIDENCE_LOG.template.md
│   ├── LAST_HANDOFF.template.md
│   └── ADR_TEMPLATE.md
├── docs/
│   ├── REFERENCE_POLICY.md
│   ├── LEARNING_SCIENCE.md
│   ├── COMMAND_REFERENCE.md
│   ├── EXAMPLE_SESSION.md
│   └── QUALITY_CHECKS.md
├── CHANGELOG.md
└── README.md
```

## Inicio rápido

1. Crea un repositorio separado para la disciplina, por ejemplo `sets-software-architecture`, usando la plantilla de configuración y estado, o el starter ya preparado.
2. En ChatGPT pega las **instrucciones listas para usar que incluya el programa** (`CHATGPT_PROJECT_INSTRUCTIONS.md`). Ese archivo aplica el motor SETS a su ámbito; `core/PROJECT_INSTRUCTIONS.md` es la especificación transversal de referencia para los programas. Los comandos son convenciones de texto, no software instalable.
3. Carga `core/PROJECT_INSTRUCTIONS.md` como fuente del proyecto junto con **`core/CONCEPTUAL_ENGINE.md`** y los motores relevantes, **`templates/LAST_HANDOFF.template.md`**, y los archivos de configuración, currículo y estado del repositorio de programa. `docs/REFERENCE_POLICY.md` explica cómo seleccionar fuentes; las referencias específicas pertenecen a `learning/REFERENCES.md` de cada disciplina.
4. Realiza `/start`. Para guardar avances, ejecuta `/close`: el handoff seguirá `LAST_HANDOFF.template.md`. Revisa los tres resultados (`LAST_HANDOFF`, `LEARNING_STATE`, delta de `EVIDENCE_LOG`), actualiza `state/` en la disciplina y haz commit.
5. Reemplaza en el Proyecto de ChatGPT los archivos adjuntos modificados: **no hay sincronización automática con GitHub**.

Para cada Proyecto de ChatGPT, sigue el `SETUP_CHATGPT.md` de su propio repositorio.

## Migración SALS → SETS

El nombre anterior, **SALS — Software Architect Learning System**, reflejaba solo la primera disciplina. SETS adopta un ámbito general de ingeniería de software. Los motores principales se conservan; se actualizan la identidad, las rutas y las instrucciones que imponían arquitectura/entrevista como objetivos universales. Los registros históricos con IDs `SALS-*` se conservan y los nuevos usan `SETS-*`.

Si tus repositorios ya existen en GitHub, puedes **renombrarlos** en Settings y cambiar las referencias locales (`git remote set-url origin ...`). No borres commits ni evidencia histórica; el cambio de nombre no borra su contenido.

`main` debe contener una versión funcional. Mejoras del framework se revisan con `docs/QUALITY_CHECKS.md`; `feature/*` es opcional. No versionar secretos, información sensible o material propietario.

> **Estado:** versión preparada para pruebas reales de aprendizaje, no eficacia pedagógica validada mediante sesiones.


## Política de enseñanza y proyectos independientes
- En modo aprendizaje, **conceptualización rigurosa antes de laboratorios por defecto**; el usuario puede solicitar retos directamente.
- Cada proyecto decide su especialidad y su stack ilustrativo mediante su `PROJECT_RULES.md` y `PROJECT_CONFIG.yaml`. No leer ni transferir estados de otros proyectos.
- Referencia de comandos: `docs/COMMAND_REFERENCE.md`. La fuente de verdad del avance está en los archivos del proyecto y su repositorio; no hay sincronización automática.

## Cambios de la v1.4.0 — Conceptual Mastery

- Motor nuevo: `core/CONCEPTUAL_ENGINE.md`. Prioriza origen del problema, mecanismos, invariantes, límites, alternativas y transferencia. **No añade un curso, un stack por defecto ni un laboratorio obligatorio**.
- Plantilla opcional: `templates/CONCEPT_MAP.template.md`. Se usa solo si una disciplina decide mantener un mapa propio de relaciones valiosas; **no hay cuarto archivo obligatorio al cerrar**.
- Cambios en `INTERACTION_ENGINE.md`, `PRACTICE_ENGINE.md`, `ASSESSMENT_ENGINE.md` y `DECISION_ENGINE.md` para alinear explicación, razonamiento, evaluación y práctica conceptual.
- Misma sintaxis de comandos y mismos tres artefactos obligatorios de `/close`.

**Importante para proyectos existentes:** este repositorio no sincroniza archivos ni edita las instrucciones activas de tus Proyectos de ChatGPT. Al actualizar las especialidades, añade `CONCEPTUAL_ENGINE.md` como fuente y actualiza **las instrucciones específicas** de cada proyecto según sus propios archivos `SETUP_CHATGPT.md`. Hasta entonces, el motor nuevo está instalado en GitHub pero puede no ejecutarse dentro del Proyecto.

Para verificarlo, utiliza los nuevos checks Q18–Q26 de `docs/QUALITY_CHECKS.md`. Consulta también `docs/UPGRADE_1.4.0.md`.
