---
name: indice
description: "Índice de los 145 formularios de Recursos civiles: reposición, apelación, casación y queja. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Recursos civiles: reposición, apelación, casación y queja: índice de formularios

> Plugin `formularios-recursos-civiles` · 145 formularios · normativa revisada el 25-11-2026.

## Qué es

Para recurrir en el proceso civil: reposición y revisión contra resoluciones del Letrado de la Administración de Justicia, apelación y oposición o impugnación, casación tras el Real Decreto-ley 5/2023, queja, nulidad de actuaciones, aclaración y complemento de sentencia, y revisión de sentencias firmes.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Recurso de apelación contra una sentencia de juicio ordinario»
- «Oposición al recurso de apelación con impugnación»
- «Recurso de reposición contra una providencia»

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-recursos-civiles:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (6)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1307 | Demanda de revisión de sentencia firme | `demanda-revision-sentencia-firme-civ-1307` |
| CIV-1317 | Demanda de audiencia al demandado rebelde para rescindir la sentencia firme | `demanda-audiencia-demandado-rebelde-rescindir-civ-1317` |
| CIV-1328 | Demanda de revisión de sentencia firme por maquinación fraudulenta | `demanda-revision-sentencia-firme-maquinacion-civ-1328` |
| CIV-1329 | Demanda de revisión de sentencia firme por recuperación de documentos decisivos | `demanda-revision-sentencia-firme-recuperacion-civ-1329` |
| CIV-1376 | Demanda de revisión de sentencia de juicio verbal por maquinación fraudulenta | `demanda-revision-sentencia-juicio-verbal-maquinacion-civ-1376` |
| CIV-1384 | Demanda de rescisión de sentencia firme por el sucesor mortis causa del rebelde, con edictos | `demanda-rescision-sentencia-firme-sucesor-mortis-causa-civ-1384` |

### Contestaciones, oposiciones y alegaciones (30)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1270 | Oposición a la apelación e impugnación de la sentencia con petición de prueba en segunda instancia | `oposicion-apelacion-e-impugnacion-sentencia-peticion-civ-1270` |
| CIV-1271 | Escrito de oposición al recurso de apelación, modelo general | `escrito-oposicion-recurso-apelacion-modelo-general-civ-1271` |
| CIV-1274 | Escrito de oposición al recurso de revisión contra un decreto por razones formales o de fondo | `escrito-oposicion-recurso-revision-contra-decreto-civ-1274` |
| CIV-1275 | Oposición al recurso de reposición contra diligencias de ordenación o decretos no definitivos | `oposicion-recurso-reposicion-contra-diligencias-civ-1275` |
| CIV-1276 | Oposición al recurso de reposición contra una providencia o un auto | `oposicion-recurso-reposicion-contra-providencia-auto-civ-1276` |
| CIV-1282 | Oposición a la apelación e impugnación de la sentencia en materia familiar (Derecho catalán) | `oposicion-apelacion-e-impugnacion-sentencia-materia-civ-1282` |
| CIV-1288 | Escrito de oposición al recurso de apelación (Derecho civil catalán) | `escrito-oposicion-recurso-apelacion-derecho-civil-civ-1288` |
| CIV-1301 | Oposición al recurso de apelación alegando su inadmisibilidad | `oposicion-recurso-apelacion-alegando-inadmisibilidad-civ-1301` |
| CIV-1319 | Oposición al incidente excepcional de nulidad de actuaciones | `oposicion-incidente-excepcional-nulidad-actuaciones-civ-1319` |
| CIV-1324 | Oposición al recurso de casación con petición de vista | `oposicion-recurso-casacion-peticion-vista-civ-1324` |
| CIV-1326 | Contestación al incidente de nulidad de actuaciones planteado por la parte contraria | `contestacion-incidente-nulidad-actuaciones-planteado-civ-1326` |
| CIV-1327 | Alegaciones de la parte sobre la nulidad de actuaciones planteada de oficio | `alegaciones-parte-sobre-nulidad-actuaciones-planteada-civ-1327` |
| CIV-1333 | Oposición al recurso de casación por infracción de norma procesal | `oposicion-recurso-casacion-infraccion-norma-procesal-civ-1333` |
| CIV-1334 | Alegaciones del recurrente en la admisión del recurso de casación (anterior al RDL 5 2023) | `alegaciones-recurrente-admision-recurso-casacion-civ-1334` |
| CIV-1336 | Contestación a la demanda de revisión de sentencia firme civil | `contestacion-demanda-revision-sentencia-firme-civil-civ-1336` |
| CIV-1338 | Oposición al recurso extraordinario por infracción procesal (régimen anterior al RDL 5 2023) | `oposicion-recurso-extraordinario-infraccion-procesal-civ-1338` |
| CIV-1349 | Oposición a la impugnación de la sentencia formulada en apelación | `oposicion-impugnacion-sentencia-formulada-apelacion-civ-1349` |
| CIV-1350 | Escrito de oposición al recurso de apelación con impugnación de la sentencia | `escrito-oposicion-recurso-apelacion-impugnacion-civ-1350` |
| CIV-1372 | Alegaciones del apelante frente a la impugnación de la resolución apelada | `alegaciones-apelante-frente-impugnacion-resolucion-civ-1372` |
| CIV-1378 | Escrito de oposición del recurrido al recurso de casación | `escrito-oposicion-recurrido-recurso-casacion-civ-1378` |
| CIV-1388 | Oposición a la apelación por motivos procesales en materia de tráfico | `oposicion-apelacion-motivos-procesales-materia-trafico-civ-1388` |
| CIV-1391 | Oposición e impugnación de la apelación de tráfico por motivos materiales y falta de consignación | `oposicion-e-impugnacion-apelacion-trafico-motivos-civ-1391` |
| CIV-2798 | Oposición a la apelación en separación o divorcio con petición de prueba en segunda instancia | `oposicion-apelacion-separacion-divorcio-peticion-civ-2798` |
| CIV-2799 | Escrito de oposición a la apelación contraria e impugnación de la sentencia de separación o divorcio | `escrito-oposicion-apelacion-contraria-e-impugnacion-civ-2799` |
| CIV-2800 | Escrito de oposición a la apelación contra la sentencia de separación o divorcio | `escrito-oposicion-apelacion-contra-sentencia-civ-2800` |
| CIV-2801 | Escrito de oposición a la apelación en separación o divorcio con aportación de documentos | `escrito-oposicion-apelacion-separacion-divorcio-civ-2801` |
| CIV-2802 | Escrito de oposición a la apelación y a la prueba en segunda instancia en separación o divorcio | `escrito-oposicion-apelacion-prueba-segunda-instancia-civ-2802` |
| CIV-2805 | Escrito de oposición a la apelación que alega su inadmisibilidad en separación o divorcio | `escrito-oposicion-apelacion-alega-inadmisibilidad-civ-2805` |
| CIV-2814 | Escrito de oposición a la apelación por infracción de normas sustantivas en proceso matrimonial | `escrito-oposicion-apelacion-infraccion-normas-civ-2814` |
| CIV-2816 | Oposición a la apelación por inadmisibilidad de documentos en procesos anteriores al 20-03-2024 | `oposicion-apelacion-inadmisibilidad-documentos-civ-2816` |

### Recursos (65)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1269 | Escrito de interposición de recurso de apelación por cláusula suelo | `escrito-interposicion-recurso-apelacion-clausula-suelo-civ-1269` |
| CIV-1272 | Recurso de apelación contra el auto que estima la declinatoria por sumisión a mediación | `recurso-apelacion-contra-auto-estima-declinatoria-civ-1272` |
| CIV-1273 | Recurso de reposición ante el Letrado de la Administración de Justicia contra decretos | `recurso-reposicion-ante-letrado-administracion-civ-1273` |
| CIV-1277 | Recurso de reposición contra una providencia o un auto civil | `recurso-reposicion-contra-providencia-auto-civil-civ-1277` |
| CIV-1278 | Recurso de revisión contra un decreto del Letrado de la Administración de Justicia, modelo general | `recurso-revision-contra-decreto-letrado-administracion-civ-1278` |
| CIV-1281 | Recurso de reposición contra la diligencia que exige la tasa judicial por falta de hecho imponible | `recurso-reposicion-contra-diligencia-exige-tasa-civ-1281` |
| CIV-1283 | Recurso de reposición frente al auto que aprecia la falta de competencia territorial | `recurso-reposicion-frente-auto-aprecia-falta-civ-1283` |
| CIV-1284 | Escrito de interposición de apelación por conflicto de aplicación del Derecho civil catalán | `escrito-interposicion-apelacion-conflicto-aplicacion-civ-1284` |
| CIV-1286 | Recurso de casación por interés casacional frente a doctrina del TSJ (Derecho civil catalán) | `recurso-casacion-interes-casacional-frente-doctrina-civ-1286` |
| CIV-1287 | Apelación contra la sentencia de un proceso matrimonial (Derecho civil catalán) | `apelacion-contra-sentencia-proceso-matrimonial-derecho-civ-1287` |
| CIV-1289 | Recurso de reposición oral contra la inadmisión de una prueba propuesta | `recurso-reposicion-oral-contra-inadmision-prueba-civ-1289` |
| CIV-1290 | Recurso de apelación contra sentencia desestimatoria en un proceso declarativo de tráfico | `recurso-apelacion-contra-sentencia-desestimatoria-civ-1290` |
| CIV-1291 | Recurso de apelación con consignación, depósito y justificante de la tasa judicial | `recurso-apelacion-consignacion-deposito-justificante-civ-1291` |
| CIV-1293 | Recurso de reposición por indefensión en la práctica de la prueba | `recurso-reposicion-indefension-practica-prueba-civ-1293` |
| CIV-1294 | Impugnación del recurso directo de revisión contra un decreto del LAJ | `impugnacion-recurso-directo-revision-contra-decreto-laj-civ-1294` |
| CIV-1295 | Recurso de queja por vulneración del derecho al juez predeterminado por la ley (art. 24 CE) | `recurso-queja-vulneracion-derecho-juez-predeterminado-civ-1295` |
| CIV-1299 | Recurso por defecto de jurisdicción en conflicto negativo de competencia | `recurso-defecto-jurisdiccion-conflicto-negativo-civ-1299` |
| CIV-1302 | Recurso de revisión contra el decreto del LAJ que estima el desahucio por falta de pago | `recurso-revision-contra-decreto-laj-estima-desahucio-civ-1302` |
| CIV-1303 | Recurso de revisión contra el decreto del LAJ que da por terminado el desahucio por enervación | `recurso-revision-contra-decreto-laj-da-terminado-civ-1303` |
| CIV-1304 | Apelación contra el auto que estima la declinatoria por sumisión a arbitraje | `apelacion-contra-auto-estima-declinatoria-sumision-civ-1304` |
| CIV-1305 | Recurso de casación por conflicto en la aplicación del Derecho civil foral o especial | `recurso-casacion-conflicto-aplicacion-derecho-civil-civ-1305` |
| CIV-1306 | Recurso de apelación contra la sentencia de un proceso de menores | `recurso-apelacion-contra-sentencia-proceso-menores-civ-1306` |
| CIV-1308 | Recurso directo de revisión contra la diligencia que cambia el procedimiento por razón de cuantía | `recurso-directo-revision-contra-diligencia-cambia-civ-1308` |
| CIV-1309 | Recurso de revisión del demandante contra el decreto que inadmite la demanda en juicio ordinario | `recurso-revision-demandante-contra-decreto-inadmite-civ-1309` |
| CIV-1310 | Recurso de reposición genérico contra una diligencia de ordenación del LAJ | `recurso-reposicion-generico-contra-diligencia-civ-1310` |
| CIV-1313 | Recurso de reposición del demandado contra el decreto que admite la demanda en juicio ordinario | `recurso-reposicion-demandado-contra-decreto-admite-civ-1313` |
| CIV-1314 | Recurso directo de revisión contra el decreto que alza la suspensión por prejudicialidad penal | `recurso-directo-revision-contra-decreto-alza-civ-1314` |
| CIV-1315 | Recurso directo de revisión contra el decreto del LAJ que inadmite un recurso de reposición | `recurso-directo-revision-contra-decreto-laj-inadmite-civ-1315` |
| CIV-1318 | Apelación del demandado rebelde por nulidad de actuaciones, con otrosí subsidiario de prueba | `apelacion-demandado-rebelde-nulidad-actuaciones-otrosi-civ-1318` |
| CIV-1323 | Recurso en interés de ley ante el Tribunal Supremo (régimen anterior al RDL 5 2023) | `recurso-interes-ley-ante-tribunal-supremo-regimen-civ-1323` |
| CIV-1330 | Recurso de casación por razón de la cuantía (régimen anterior al RDL 5 2023) | `recurso-casacion-razon-cuantia-regimen-anterior-rdl-5-civ-1330` |
| CIV-1331 | Recurso de casación por interés casacional (régimen anterior al RDL 5 2023) | `recurso-casacion-interes-casacional-regimen-anterior-civ-1331` |
| CIV-1337 | Recurso en proceso que lleva aparejado el lanzamiento (escrito) | `recurso-proceso-lleva-aparejado-lanzamiento-escrito-civ-1337` |
| CIV-1339 | Recurso de revisión contra el decreto del LAJ que inadmite la demanda | `recurso-revision-contra-decreto-laj-inadmite-demanda-civ-1339` |
| CIV-1341 | Recurso de queja contra la denegación del recurso de casación (anterior al RDL 5 2023) | `recurso-queja-contra-denegacion-recurso-casacion-civ-1341` |
| CIV-1343 | Recurso de apelación por motivos de fondo | `recurso-apelacion-motivos-fondo-civ-1343` |
| CIV-1353 | Recurso de apelación que plantea antes la falta de jurisdicción o competencia objetiva o funcional | `recurso-apelacion-plantea-antes-falta-jurisdiccion-civ-1353` |
| CIV-1354 | Recurso de apelación por infracción de normas o garantías procesales | `recurso-apelacion-infraccion-normas-garantias-civ-1354` |
| CIV-1355 | Recurso de apelación por falta de jurisdicción de los tribunales civiles | `recurso-apelacion-falta-jurisdiccion-tribunales-civiles-civ-1355` |
| CIV-1356 | Recurso de apelación por infracción de normas sustantivas de la sentencia | `recurso-apelacion-infraccion-normas-sustantivas-civ-1356` |
| CIV-1357 | Recurso de reposición oral contra la inadmisión de prueba en la audiencia previa | `recurso-reposicion-oral-contra-inadmision-prueba-civ-1357` |
| CIV-1358 | Recurso de reposición oral contra la admisión de prueba en la audiencia previa | `recurso-reposicion-oral-contra-admision-prueba-civ-1358` |
| CIV-1362 | Recurso de reposición oral genérico contra la resolución sobre admisión de prueba, con protesta | `recurso-reposicion-oral-generico-contra-resolucion-civ-1362` |
| CIV-1363 | Recurso de reposición del demandante contra la admisión de la reconvención por ser inadmisible | `recurso-reposicion-demandante-contra-admision-civ-1363` |
| CIV-1367 | Recurso de casación por interés casacional genérico | `recurso-casacion-interes-casacional-generico-civ-1367` |
| CIV-1368 | Recurso de reposición genérico contra resoluciones judiciales o del LAJ | `recurso-reposicion-generico-contra-resoluciones-civ-1368` |
| CIV-1369 | Recurso de audiencia en justicia contra el acuerdo sancionador por vulnerar la buena fe procesal | `recurso-audiencia-justicia-contra-acuerdo-sancionador-civ-1369` |
| CIV-1370 | Apelación contra sentencia de juicio ordinario por infracción de normas y garantías procesales | `apelacion-contra-sentencia-juicio-ordinario-infraccion-civ-1370` |
| CIV-1374 | Recurso de casación ante el TSJ por oposición a doctrina jurisprudencial en Derecho civil propio | `recurso-casacion-ante-tsj-oposicion-doctrina-civ-1374` |
| CIV-1381 | Recurso de reposición contra diligencia de ordenación que resuelve materia propia de providencia | `recurso-reposicion-contra-diligencia-ordenacion-civ-1381` |
| CIV-1389 | Apelación de tráfico por error fáctico e infracción material, con vista (pleito previo al 20-3-2024) | `apelacion-trafico-error-factico-e-infraccion-material-civ-1389` |
| CIV-1390 | Recurso de apelación en materia de tráfico por infracción de normas y garantías procesales | `recurso-apelacion-materia-trafico-infraccion-normas-civ-1390` |
| CIV-2796 | Recurso de reposición contra el auto de la Audiencia que deniega prueba en segunda instancia | `recurso-reposicion-contra-auto-audiencia-deniega-civ-2796` |
| CIV-2803 | Recurso de queja contra la inadmisión de la apelación por no citar los pronunciamientos impugnados | `recurso-queja-contra-inadmision-apelacion-no-citar-civ-2803` |
| CIV-2804 | Recurso de queja contra el auto que inadmite la apelación por haberse presentado fuera de plazo | `recurso-queja-contra-auto-inadmite-apelacion-haberse-civ-2804` |
| CIV-2806 | Recurso de reposición contra el auto que admite a trámite la reconvención en proceso matrimonial | `recurso-reposicion-contra-auto-admite-tramite-civ-2806` |
| CIV-2807 | Recurso de apelación contra la sentencia que deniega la separación o divorcio, con petición de vista | `recurso-apelacion-contra-sentencia-deniega-separacion-civ-2807` |
| CIV-2808 | Recurso de apelación contra la sentencia que deniega la separación o divorcio, aportando documentos | `recurso-apelacion-contra-sentencia-deniega-separacion-civ-2808` |
| CIV-2809 | Recurso de apelación del actor contra la desestimación de la impugnación de paternidad, con prueba | `recurso-apelacion-actor-contra-desestimacion-civ-2809` |
| CIV-2810 | Recurso de apelación contra la resolución con medidas distintas de las propuestas por los cónyuges | `recurso-apelacion-contra-resolucion-medidas-distintas-civ-2810` |
| CIV-2811 | Recurso de apelación por la prueba denegada en primera instancia en filiación extramatrimonial | `recurso-apelacion-prueba-denegada-primera-instancia-civ-2811` |
| CIV-2813 | Recurso de reposición que pide la nulidad de actuaciones por no demandar al Ministerio Fiscal | `recurso-reposicion-pide-nulidad-actuaciones-no-civ-2813` |
| CIV-2815 | Recurso de reposición contra la negativa a celebrar a puerta cerrada el juicio de paternidad | `recurso-reposicion-contra-negativa-celebrar-puerta-civ-2815` |
| CIV-2817 | Recurso de apelación contra la sentencia que deniega la separación o divorcio, pidiendo prueba | `recurso-apelacion-contra-sentencia-deniega-separacion-civ-2817` |
| CIV-2818 | Recurso de reposición contra el auto que inadmite una petición en un juicio civil de tráfico | `recurso-reposicion-contra-auto-inadmite-peticion-civ-2818` |

### Comunicaciones, requerimientos y cartas (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1279 | Solicitud de que el tribunal resuelva tras desestimar la reposición ante el Letrado de la AJ | `solicitud-tribunal-resuelva-tras-desestimar-reposicion-civ-1279` |
| CIV-1320 | Solicitud de nulidad de actuaciones de la sentencia por falta de citación a juicio | `solicitud-nulidad-actuaciones-sentencia-falta-citacion-civ-1320` |
| CIV-1321 | Solicitud de nulidad de actuaciones de la sentencia por quien debió ser parte en el juicio | `solicitud-nulidad-actuaciones-sentencia-quien-debio-civ-1321` |
| CIV-1360 | Solicitud de aclaración de sentencia civil para rectificar un error material | `solicitud-aclaracion-sentencia-civil-rectificar-error-civ-1360` |
| CIV-1361 | Solicitud de complemento de sentencia por omisión de pronunciamiento | `solicitud-complemento-sentencia-omision-pronunciamiento-civ-1361` |
| CIV-1371 | Solicitud de aclaración de resolución judicial (art. 267.2 LOPJ) | `solicitud-aclaracion-resolucion-judicial-art-267-2-lopj-civ-1371` |
| CIV-1386 | Solicitud de nulidad de actuaciones por falta de diligencia de reparto en la demanda | `solicitud-nulidad-actuaciones-falta-diligencia-reparto-civ-1386` |

### Escritos de trámite y otros (37)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1280 | Incidente de nulidad de actuaciones en un proceso hipotecario por falta de citación | `incidente-nulidad-actuaciones-proceso-hipotecario-civ-1280` |
| CIV-1285 | General (queja) | `general-queja-civ-1285` |
| CIV-1292 | Impugnación de un recurso de reposición por inadmisible al interponerse fuera de plazo | `impugnacion-recurso-reposicion-inadmisible-civ-1292` |
| CIV-1296 | Otrosí que aporta documentos y pide prueba en segunda instancia | `otrosi-aporta-documentos-pide-prueba-segunda-instancia-civ-1296` |
| CIV-1298 | Personación ante el Supremo y oposición a admitir la casación (previo al RDL 5 de 2023) | `personacion-ante-supremo-oposicion-admitir-casacion-civ-1298` |
| CIV-1300 | Escrito general de interposición del recurso de apelación | `escrito-general-interposicion-recurso-apelacion-civ-1300` |
| CIV-1311 | Impugnación genérica del recurso de reposición contra un decreto del LAJ | `impugnacion-generica-recurso-reposicion-contra-decreto-civ-1311` |
| CIV-1312 | Impugnación genérica del recurso de reposición contra una diligencia de ordenación del LAJ | `impugnacion-generica-recurso-reposicion-contra-civ-1312` |
| CIV-1322 | Comparecencia del demandado rebelde durante el proceso con solicitud de nulidad de actuaciones | `comparecencia-demandado-rebelde-durante-proceso-civ-1322` |
| CIV-1325 | Escrito de la parte que plantea la nulidad de actuaciones | `escrito-parte-plantea-nulidad-actuaciones-civ-1325` |
| CIV-1332 | Personación ante el Tribunal Supremo en casación pidiendo testimonio para ejecución provisional | `personacion-ante-tribunal-supremo-casacion-pidiendo-civ-1332` |
| CIV-1335 | Personación ante el Tribunal Supremo en casación civil con oposición a la admisión | `personacion-ante-tribunal-supremo-casacion-civil-civ-1335` |
| CIV-1340 | Escrito del apelante que subsana un defecto en la interposición del recurso | `escrito-apelante-subsana-defecto-interposicion-recurso-civ-1340` |
| CIV-1342 | Escrito de impugnación de un recurso de reposición | `escrito-impugnacion-recurso-reposicion-civ-1342` |
| CIV-1344 | Otrosí del recurso de apelación pidiendo prueba en segunda instancia por rebeldía involuntaria | `otrosi-recurso-apelacion-pidiendo-prueba-segunda-civ-1344` |
| CIV-1345 | Otrosí de apelación pidiendo prueba en segunda instancia por hechos posteriores a la sentencia | `otrosi-apelacion-pidiendo-prueba-segunda-instancia-civ-1345` |
| CIV-1346 | Otrosí de apelación pidiendo prueba en segunda instancia por prueba indebidamente denegada | `otrosi-apelacion-pidiendo-prueba-segunda-instancia-civ-1346` |
| CIV-1347 | Otrosí del recurso de apelación que aporta un documento conforme al artículo 270 LEC | `otrosi-recurso-apelacion-aporta-documento-conforme-civ-1347` |
| CIV-1348 | Otrosí de la oposición con alegaciones sobre la prueba que pide el apelante en segunda instancia | `otrosi-oposicion-alegaciones-sobre-prueba-pide-civ-1348` |
| CIV-1351 | Otrosí del recurso de apelación solicitando la celebración de vista | `otrosi-recurso-apelacion-solicitando-celebracion-vista-civ-1351` |
| CIV-1352 | Desistimiento del recurso de apelación con alegaciones sobre costas | `desistimiento-recurso-apelacion-alegaciones-sobre-civ-1352` |
| CIV-1359 | Reposición oral en el juicio contra la denegación de ilicitud de prueba por vulnerar derechos | `reposicion-oral-juicio-contra-denegacion-ilicitud-civ-1359` |
| CIV-1364 | Reposición contra la admisión de reconvención dirigida a persona no demandante por inadmisible | `reposicion-contra-admision-reconvencion-dirigida-civ-1364` |
| CIV-1365 | Reposición del demandado contra la admisión de la demanda por faltar documentos esenciales | `reposicion-demandado-contra-admision-demanda-faltar-civ-1365` |
| CIV-1373 | Personación ante el tribunal competente para conocer del recurso de casación | `personacion-ante-tribunal-competente-conocer-recurso-civ-1373` |
| CIV-1375 | Nulidad de actuaciones por mal emplazamiento en juicio de impugnación de acuerdos de comunidad | `nulidad-actuaciones-mal-emplazamiento-juicio-civ-1375` |
| CIV-1377 | Personación ante la Sala que, en el trámite de admisión de la casación, se ha declarado competente | `personacion-ante-sala-tramite-admision-casacion-ha-civ-1377` |
| CIV-1379 | Desistimiento del recurrente del recurso de casación | `desistimiento-recurrente-recurso-casacion-civ-1379` |
| CIV-1380 | Escrito de desistimiento de un recurso interpuesto | `escrito-desistimiento-recurso-interpuesto-civ-1380` |
| CIV-1382 | Desistimiento del apelante del recurso de apelación (art. 450 LEC) | `desistimiento-apelante-recurso-apelacion-art-450-lec-civ-1382` |
| CIV-1385 | Nulidad de actuaciones por falta de inmediación judicial en la vista del incidente de intereses | `nulidad-actuaciones-falta-inmediacion-judicial-vista-civ-1385` |
| CIV-1387 | Escrito pidiendo complemento de sentencia por omisión de pretensiones (art. 215.2 LEC) | `escrito-pidiendo-complemento-sentencia-omision-civ-1387` |
| CIV-1392 | Escrito pidiendo testimonio para ejecutar provisionalmente la sentencia apelada por la contraparte | `escrito-pidiendo-testimonio-ejecutar-provisionalmente-civ-1392` |
| CIV-1393 | Reposición del ejecutante contra el sobreseimiento de la ejecución provisional por revocación | `reposicion-ejecutante-contra-sobreseimiento-ejecucion-civ-1393` |
| CIV-2797 | Escrito que impugna el recurso de reposición contrario por inexistencia de apoderamiento | `escrito-impugna-recurso-reposicion-contrario-civ-2797` |
| CIV-2812 | Petición de aclaración de la sentencia de paternidad por error al expresar la acción ejercitada | `peticion-aclaracion-sentencia-paternidad-error-civ-2812` |
| CIV-2819 | Impugnación de la reposición contra el auto que inadmite una petición en un juicio civil de tráfico | `impugnacion-reposicion-contra-auto-inadmite-peticion-civ-2819` |
