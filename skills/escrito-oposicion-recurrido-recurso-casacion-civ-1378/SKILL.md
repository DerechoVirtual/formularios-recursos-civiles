---
name: escrito-oposicion-recurrido-recurso-casacion-civ-1378
description: "Escrito de oposición del recurrido al recurso de casación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición del recurrido al recurso de casación

> Formulario **CIV-1378** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 25-11-2026.

## Qué es

Escrito de oposición de la parte recurrida a un recurso de casación (art. 485 LEC), ante la Sala Primera del Tribunal Supremo o ante la Sala de lo Civil del Tribunal Superior de Justicia. El modelo desarrolla, como ejemplo, la oposición a un recurso de una Comunidad Autónoma en un pleito sobre arrendamiento de finca rústica (condición de cultivador personal y acceso a la propiedad), e incluye la solicitud, o no, de celebración de vista.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición del recurrido al recurso de casación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición del recurrido al recurso de casación” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:escrito-oposicion-recurrido-recurso-casacion-civ-1378`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PARTE RECURRIDA (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] COMUNIDAD AUTÓNOMA
- [ ] CULTIVO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LOCALIDAD
- [ ] Nº
- [ ] OTRA ACTIVIDAD DEL ARRENDATARIO
- [ ] PARTE RECURRENTE
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 485 LEC
- art. 15 Ley 83/1980
- art. 276.3 LEC

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…otras partes personadas (art. 273 LEC), para su traslado por el propio tribunal.»: comprobar la redacción vigente de los arts. 477 a 485 LEC tras el Real Decreto-ley 6/2023 antes de usar el modelo. El ejemplo se refiere a la legislación de arrendamientos rústicos de 1980 y 1992, aplicable por razones de vigencia temporal; verificar la normativa aplicable al caso concreto.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO: Formulario adaptado a la reforma procesal de la LO 1/2025. Este modelo responde a la oposición a un recurso de casación fundado en infracción de norma sustantiva por oposición a doctrina jurisprudencial, pero es válido, con las necesarias adaptaciones, para formular la oposición a cualquier recurso de casación. La LEC no impone forma intrínseca ni extrínseca alguna al escrito de oposición, pero en cualquier caso deberá rebatir los motivos del recurso en orden correlativo (salvo que por evidente conexión entre ellos quepa hacerlo conjuntamente), podrá poner de manifiesto la concurrencia de causas de inadmisión no advertidas por la Sala, y es el adecuado para solicitar la celebración de vista si interesa a la parte recurrida. De no existir en la sede del tribunal ante el que se presenta el escrito el servicio de recepción de notificaciones a que se refiere el art. 28.3 LEC, deberán acompañarse tantas copias literales del mismo cuantas sean las otras partes personadas (art. 273 LEC), para su traslado por el propio tribunal.

Recurso n.º [Nº DE PROCEDIMIENTO]: [Nº DE RECURSO/AÑO]

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— A LA SALA PRIMERA DEL TRIBUNAL SUPREMO

— A LA SALA DE LO CIVIL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE [COMUNIDAD AUTÓNOMA]


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
