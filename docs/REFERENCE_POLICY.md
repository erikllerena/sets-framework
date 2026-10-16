# SETS — Reference Policy (política transversal)

**Ámbito:** cualquier disciplina de ingeniería de software que use SETS: diseño, lenguajes, bases de datos, redes, plataformas, seguridad, sistemas distribuidos, etc. Este archivo establece **cómo investigar y citar**; las bibliografías técnicas pertenecen a cada disciplina.

## 1. Jerarquía de fuentes
1. Para comportamiento, APIs y sintaxis: **documentación oficial, especificaciones, estándares y propuestas de cambios** de la versión estudiada.
2. Para decisiones de ingeniería: publicaciones técnicas primarias, postmortems, manuales de ingeniería, mediciones reproducibles y literatura especializada.
3. Para comprensión didáctica: libros, tutoriales y materiales de terceros, verificando que reflejen la versión y el contexto aplicables.
4. Experiencias comunitarias pueden revelar problemas y alternativas, pero **no equivalen por sí solas a evidencia generalizable**.

El orden es una preferencia que depende de la pregunta; no sustituye la evaluación de calidad de cada fuente.

## 2. Protocolo de investigación (por tema)
- Delimitar el problema concreto y qué afirmaciones necesitan verificación.
- Registrar versiones relevantes: lenguaje, runtime, framework, plataforma, fecha o estándar.
- Elegir 1–3 referencias pertinentes; explicar **qué aprender** de cada una y **por qué**.
- Distinguir `hecho documentado`, `supuesto`, `hipótesis`, `experiencia` y `resultado de prueba`.
- Comparar información contradictoria y declarar incertidumbre si no se puede resolver.
- Para asuntos cambiantes (seguridad, soporte, versiones, costos, servicios), comprobar vigencia cuando haya acceso a fuentes actualizadas.
- Nunca inventar enlaces, páginas, citas, benchmarks, ejecución de laboratorios ni acceso a documentación que no fue consultada.

## 3. Uso dentro de una sesión SETS
Una fuente debe habilitar una actividad observable: explicar un mecanismo sin notas, justificar una decisión, reproducir un ejemplo, diseñar un experimento o revisar un caso. No sustituir la práctica por una lista extensa de lecturas. Ajustar idioma, profundidad y carga al objetivo y tiempo del estudiante.

## 4. Separación de responsabilidades
- `sets-framework/docs/REFERENCE_POLICY.md`: esta política general.
- `sets-framework/docs/LEARNING_SCIENCE.md`: técnicas de aprendizaje y sus límites.
- `<repositorio-disciplina>/learning/REFERENCES.md`: fuentes y bibliografía del tema.

Cuando una disciplina no tenga `learning/REFERENCES.md`, SETS puede proponer referencias pertinentes siguiendo esta política, pero no debe fingir que existe una bibliografía cargada.
