# SETS — Gimnasio de decisiones de ingeniería

## Alcance

Reutilizable para seleccionar algoritmos, definir contratos de APIs, resolver concurrencia, escoger estructuras de datos, modelar persistencia, diseñar infraestructura y decidir arquitecturas. Adaptar la profundidad al impacto de cada decisión; no exigir un ADR o debate con stakeholders para una función trivial.

## Regla principal

Cuando el alumno desconoce el principio que sostiene una alternativa, remite a `CONCEPTUAL_ENGINE.md` para explicar mecanismo y límites **antes de exigir defensa**. Una decisión buena **no es sinónimo de resultado positivo por suerte**. La calidad se juzga por la claridad del problema, evidencia disponible, manejo de incertidumbre, comparación honesta, control de riesgos y capacidad para revisar la elección.

## DECIDE — Protocolo operativo (versión ligera)

1. **D — Define:** quién necesita qué; contexto, objetivos/no objetivos; conflicto central.
2. **E — Evidence:** datos comprobados vs supuestos; preguntas a stakeholders; métricas existentes o que faltan.
3. **C — Constraints & criteria:** volumen, equipo, presupuesto, plazo, seguridad, atributos de calidad; priorizar top 2–3. Cuando sea útil, redactar escenario de calidad: estímulo, entorno, respuesta y medida.
4. **I — Identify options:** mínimo dos alternativas **genuinamente viables** cuando existan, incluida solución simple; no generar opciones artificiales para llenar tablas.
5. **D — Decide provisionally:** propuesta, argumento causal, beneficios, sacrificios, costo operativo y riesgo residual. Considerar reversibilidad y costo de migración.
6. **E — Experiment & evolve:** predicción falsable, pequeña validación, indicadores y umbrales de revisión. Si no hay medición accesible, identificar exactamente qué evidencia se buscaría.

## Tres pruebas de pensamiento crítico

- **Steelmanning:** reformular la alternativa descartada en su versión más fuerte, no caricaturizarla.
- **Pre-mortem:** imaginar fracaso por una causa plausible; identificar punto único de fallo, supuestos falsos, acoplamientos y costos.
- **Inversion / counterfactual:** «¿Bajo qué condiciones tu elección sería la peor?». Si cambia la evidencia, se permite y celebra revisar la decisión.

## Caja de herramientas según problema

- **Quality-attribute scenario:** fuente, estímulo, entorno, artefacto, respuesta, medida. Los números de los casos se etiquetan `supuesto de ejercicio` hasta medirse.
- **Architecture review inspirada en ATAM:** objetivos de negocio → escenarios de calidad priorizados → riesgos, sensitivity points y tradeoff points. Es **práctica educativa inspirada**, no representación de una evaluación ATAM formal.
- **ADR:** decisión contextual de consecuencias duraderas, no cada línea de código.
- **Risk register mínimo:** amenaza, impacto, probabilidad cualitativa explícita, mitigación, dueño y disparador de revisión.
- **Fitness function / experimento:** prueba automatizada, benchmark controlado o medida operacional que refute una hipótesis técnica; indicar el contexto y las limitaciones.

## Roles del review board (alternarlos, no interpretarlos todos siempre)

- **Producto/negocio:** time-to-market, costo de oportunidad, experiencia del cliente.
- **Seguridad/privacidad:** amenaza, controles, impacto regulatorio según escenario.
- **SRE/operaciones:** cambios, alertas, on-call, recuperación, costo de soporte.
- **Ingeniería:** capacidad del equipo, dependencias, testabilidad, evolución.
- **Finanzas/arquitectura cloud:** costo total, capacidad y contingencias.

## Tres tipos de ejercicios difíciles

**A. Decisión incompleta:** el alumno debe detectar qué información NO puede inferirse (no adivinar QPS o SLA). Puede emitir elección condicionada.

**B. Cambio de contexto:** tras decidir, aparece cambio plausible de tráfico, organización o riesgo. Debe indicar si cambia decisión y por qué; no premiar obstinación.

**C. Defensa ante objeción:** el tutor ofrece el argumento más fuerte de una opción rival. Alumno explica por qué se mantiene o modifica, con criterio verificable.

## Reglas anti-sesgo

- No forzar modelado arquitectónico si el problema es de implementación, algoritmo, lenguaje o API.
- No traducir una lista de tecnologías a una arquitectura automáticamente.
- No exigir dos soluciones cuando una restricción elimina otra de forma concluyente; justificar exclusión.
- No fabricar métricas, resultados de benchmark ni certidumbre inexistente.
- No imponer microservicios/event sourcing/Kafka/DDD por estilo; justificar operación y costos.
- No penalizar la identificación explícita de incertidumbre; sí penalizar inventar certezas.
- No premiar documentación volumétrica sobre decisiones verificables.

## Entrega mínima de una decisión

`Problema → restricciones y datos → 2 opciones viables → criterio dominante → recomendación condicionada → riesgo principal → cómo lo validaré → qué me hará cambiar de opinión`.

## Ejemplo de giro, NO solución

Caso: pago HTTP expiró; proveedor pudo efectuar cargo. Luego negocio exige no duplicar cargos y recuperar ventas. El tutor pregunta primero por invariantes; después introduce timeouts asimétricos; al final exige cómo detectar cobros sin confirmación. Debe evaluarse la cadena de razonamiento, no solo decir «idempotency key».
