# SETS Framework — v1.3.1

**SETS — Software Engineering Training System** es un framework reutilizable para entrenar competencias en ingeniería de software: comprensión profunda, programación, diseño, resolución de problemas, razonamiento crítico, evaluación con evidencias y continuidad del aprendizaje. No está limitado a arquitectura de software y no depende del framework educativo universal de otras disciplinas.

## División de responsabilidades

- **`sets-framework` (este repositorio):** motores, políticas de referencias y plantillas reutilizables, sin currículo ni progreso de una disciplina.
- **`sets-software-architecture` (primer proyecto):** currículo, referencias, entrevista, casos, laboratorios, decisiones y progreso del estudiante, con meta de Software Architect.
- **Otros repositorios futuros:** `sets-java-engineering`, `sets-apache-kafka`, etc.; cada uno define objetivos propios y reutiliza SETS sin exigir formación arquitectónica en todas las actividades.

## Estructura

```text
sets-framework/
├── core/
│   ├── PROJECT_INSTRUCTIONS.md
│   ├── INTERACTION_ENGINE.md
│   ├── DECISION_ENGINE.md
│   ├── PRACTICE_ENGINE.md
│   ├── ASSESSMENT_ENGINE.md
│   └── SESSION_HANDOFF.md
├── templates/
│   ├── PROJECT_CONFIG.template.yaml
│   ├── LEARNING_STATE.template.md
│   ├── EVIDENCE_LOG.template.md
│   └── ADR_TEMPLATE.md
├── docs/
│   ├── REFERENCE_POLICY.md
│   ├── LEARNING_SCIENCE.md
│   ├── EXAMPLE_SESSION.md
│   └── QUALITY_CHECKS.md
├── CHANGELOG.md
└── README.md
```

## Inicio rápido

1. Crea un repositorio separado para la disciplina, por ejemplo `sets-software-architecture`, usando la plantilla de configuración y estado, o el starter ya preparado.
2. En el Proyecto de ChatGPT de esa disciplina, pega `core/PROJECT_INSTRUCTIONS.md` en **Instrucciones del proyecto**. Los comandos `/start`, `/learn`, `/close` etc. son convenciones de texto, no comandos de software instalable.
3. Carga los motores relevantes y archivos de configuración, currículo y estado del repositorio de disciplina. `docs/REFERENCE_POLICY.md` explica cómo seleccionar fuentes; las referencias específicas pertenecen a `learning/REFERENCES.md` de cada disciplina.
4. Realiza `/start`. Para guardar avances, ejecuta `/close`, revisa los tres resultados (`LAST_HANDOFF`, `LEARNING_STATE`, delta de `EVIDENCE_LOG`), actualiza `state/` en la disciplina y haz commit.
5. Reemplaza en el Proyecto de ChatGPT los archivos adjuntos modificados: **no hay sincronización automática con GitHub**.

Para el proyecto inicial, sigue `SETUP_CHATGPT.md` dentro de `sets-software-architecture`.

## Migración SALS → SETS

El nombre anterior, **SALS — Software Architect Learning System**, reflejaba solo la primera disciplina. SETS adopta un ámbito general de ingeniería de software. Los motores principales se conservan; se actualizan la identidad, las rutas y las instrucciones que imponían arquitectura/entrevista como objetivos universales. Los registros históricos con IDs `SALS-*` se conservan y los nuevos usan `SETS-*`.

Si tus repositorios ya existen en GitHub, puedes **renombrarlos** en Settings y cambiar las referencias locales (`git remote set-url origin ...`). No borres commits ni evidencia histórica; el cambio de nombre no borra su contenido.

`main` debe contener una versión funcional. Mejoras del framework se revisan con `docs/QUALITY_CHECKS.md`; `feature/*` es opcional. No versionar secretos, información sensible o material propietario.

> **Estado:** versión preparada para pruebas reales de aprendizaje, no eficacia pedagógica validada mediante sesiones.
