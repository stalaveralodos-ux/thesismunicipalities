# Municipal Social Rights Lab — Evidence Extraction, Phase 0

## Qué es esto

Primer paso de la Sección 24 de la especificación: extraer de la tesis los conceptos, hallazgos y referencias existentes en una tabla de evidencia estructurada, antes de tocar código o dashboard.

## Qué se ha procesado hasta ahora

- **Capítulo VI (Conclusión) completo** — de "Theoretical and Conceptual Conclusions" hasta "Final Reflections" (pp. 239–257). Esta es la fuente de mayor densidad: aquí la tesis sintetiza sus propios hallazgos comparativos de coverage/accessibility/inclusion, capacidad constitucional, y migración/universalidad para las tres ciudades.
- **Introducción / estructura del Capítulo I** — la definición explícita del commitment-impact framework y cómo se aplica en los capítulos empíricos.
- **Un fragmento verificado del Capítulo III (Educación, Turín)** — porque contiene el único lugar donde la tesis aplica literalmente su propia "Commitment-Impact Matrix" a un caso concreto (Turín, educación: "high in commitment but only moderate-to-high in impact"). Esto es oro para validar el diseño del indicador MRCI/Impact del spec.

## Actualización — segunda pasada

Se ha añadido al codebook:

- **Capítulo II, sección 2.2.4 (Discusión comparativa) completa** — esta sección es prácticamente un mapeo 1:1 de las seis subdimensiones del MCC (spec Sec. 5.1: competencia legal, poder regulatorio, autonomía fiscal, capacidad administrativa, coordinación intergubernamental, capacidad de resolución de conflictos) aplicadas explícitamente a Turín/Barcelona/Atenas. Es la fuente más valiosa encontrada hasta ahora para operacionalizar el MCC.
- **Los seis bloques "ASSESSMENT"** (síntesis de cierre por ciudad y capítulo) que la tesis usa de forma consistente: Atenas-Educación, Turín-Salud, Barcelona-Salud, Turín-Vivienda, Barcelona-Vivienda, Atenas-Vivienda (esta última ya estaba en la primera pasada).
- Varios datos cuantitativos directos que antes no tenía: % de stock ERP en Turín (3.4%), % stock público en Barcelona (<2%), % de ingresos destinado a alquiler en Barcelona (46%), subida de alquileres (+70% en una década), tasas de escolarización de niños Roma en Atenas (29%/2%), clases de integración adecuadamente preparadas en Atenas (98/510).

## Cobertura actual: las 9 combinaciones Ciudad × Derecho

Con esta tercera pasada se completó lo que faltaba. El patrón de cierre por ciudad y capítulo no era uniforme en mayúsculas — la tesis usa "ASSESSMENT" (todo mayúsculas) en seis casos y "Assessment" (solo inicial) en otros tres, lo que explica por qué la primera búsqueda no los encontró. Ya está el conjunto completo:

| | Educación | Salud | Vivienda |
|---|---|---|---|
| **Turín** | ✅ (territorial + declive demográfico + Commitment-Impact Matrix explícita) | ✅ (rol facilitativo, ONGs cubren huecos) | ✅ (ERP 3.4% del stock) |
| **Barcelona** | ✅ (Consorci d'Educació, City Agreement 2030) | ✅ (superblocks, padrón como barrera) | ✅ (stock <2%, 46% renta/ingreso) |
| **Atenas** | ✅ (98/510 clases de integración, Roma 29%/2%) | ✅ (I Care, KYADA, dependencia de ONGs/UE) | ✅ (34.000 unidades Airbnb, Art.21(4) sin desarrollo) |

Cada celda tiene ya una entrada tipo "ASSESSMENT" en el codebook con su cita de página exacta.

## Qué falta todavía (siguiente sesión, si se quiere profundizar más)

- Capítulo II, secciones 2.1 (marco internacional) y 2.2.1–2.2.3 (narrativas históricas específicas de cada ciudad) — no leídas todavía, aunque 2.2.4 ya captura su síntesis comparativa completa
- El desarrollo intermedio de cada subcapítulo (constitutional framework, distribution of competences) de los Capítulos III, IV y V — ya se cubrieron las síntesis de cierre pero no todo el cuerpo de cada sección
- Bibliografía / Tabla de casos — para poblar `sources.csv` con metadatos completos (organización, tipo de fuente, fiabilidad)
- Capítulo V (Vivienda): fusionar esto con tu extracción ya hecha en `housing-rights-spain` en vez de re-extraer del todo

## Principio metodológico aplicado

Cada fila de `indicator-codebook-phase0.csv` distingue explícitamente:
- **thesis synthesis / documentary / academic study / official administrative data / legal interpretation** — algo que la tesis afirma con respaldo
- **thesis argument** — una tesis interpretativa de la autora, no un dato bruto
- **conceptual framework element / caution flag** — un concepto (constitucionalismo desde abajo, "local trap") que **no debe convertirse en un score numérico** sin trabajo metodológico adicional. Esto sigue literalmente la instrucción del spec: "the project should label the rule as a proposed extension rather than presenting it as an established empirical finding."

## Dato cuantitativo destacado

La tesis es mayormente cualitativa/documental. Los pocos datos numéricos directos encontrados hasta ahora:
- Turín: ~40% de familias matriculan fuera de su distrito asignado (segregación informal, Ch. III, p.98)
- Turín: programa Spazio Non Solo Mamme atendía ~50 madres/año, interrumpido en 2023
- Turín: servicios de discapacidad alcanzan 1.538 usuarios (dato de monitoreo municipal)
- Atenas: ~34.000 unidades de vivienda listadas en Airbnb al menos una vez entre 2014–2021

Esto confirma algo importante para el diseño del `scores.csv`: la mayoría de las observaciones serán **codificación cualitativa ordinal** (alto/medio/bajo, con nota de evidencia), no series numéricas continuas. El modelo de datos del spec ya lo anticipa (`evidence_type` incluye "qualitative coding" y "expert judgement"), así que no hay que ajustar el schema — solo ser realista sobre cuánto de la Fase 3 (MVP) dependerá de codificación manual cuidadosa en vez de import directo de estadísticas.

## Siguiente paso sugerido

Decidir: ¿continúo con el Capítulo II y III completos en la próxima sesión, o prefieres que primero fusione esto con lo que ya tienes extraído de vivienda (Ch. V) para tener las tres materias (housing/health/education) en paralelo aunque sea con distinto nivel de detalle?
