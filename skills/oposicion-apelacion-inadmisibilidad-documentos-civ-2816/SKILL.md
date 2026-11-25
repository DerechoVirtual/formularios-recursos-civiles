---
name: oposicion-apelacion-inadmisibilidad-documentos-civ-2816
description: "Oposición a la apelación por inadmisibilidad de documentos en procesos anteriores al 20-03-2024. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la apelación por inadmisibilidad de documentos en procesos anteriores al 20-03-2024

> Formulario **CIV-2816** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 25-11-2026.

## Qué es

Escrito de oposición al recurso de apelación, interpuesto en procedimiento de separación o divorcio, en el que se alega que los documentos aportados por el apelante, no lo fueron en el momento procesal oportuno. Régimen anterior al RDL 6/2023, aplicable a procesos incoados con anterioridad al 20/03/2024.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la apelación por inadmisibilidad de documentos en procesos anteriores al 20-03-2024» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la apelación por inadmisibilidad de documentos en procesos anteriores al 20-03-2024” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:oposicion-apelacion-inadmisibilidad-documentos-civ-2816`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] COMPLETAR
- [ ] DESCRIBIR
- [ ] Nº

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Habiéndose dado curso a la interposición de la apelación, las demás partes personadas podrán oponerse al recurso o, aprovechando su existencia, impugnar aquellos extremos de la resolución recurrida que también pudieran resultarles desfavorables. Téngase presente que de conformidad con lo prevenido en el número 3 del artículo 461, está ya fuera de toda duda que también la parte apelada, y no solo el apelante, podrán acompañar documentos a su escrito de oposición y solicitar el recibimiento a prueba en segunda instancia, pudiendo realizar también, cuando hubiera sido la parte contraria quien lo hubiese interesado, las alegaciones que estimen oportunas sobre la admisibilidad de los documentos acompañados de contrario y de la pertinencia o impertinencia de las pruebas propuestas. También será en este escrito de oposición al recurso de apelación en el que la parte apelada podrá alegar las razones que tuviere para mantener que el recurso de apelación formulado de contrario ni siquiera debió haber sido admitido a trámite, conforme a lo que se establecía en el artículo 457.5º de la ley de enjuiciamiento civil, en sede de preparación del recurso, actual art. 458.4 LEC, en sede de interposición.

(2) El artículo 461.3º de la ley de enjuiciamiento civil permite a la parte apelada que, al tiempo de oponerse al recurso interpuesto de contrario, formule las alegaciones que estime oportunas sobre la admisibilidad de los documentos aportados y de las pruebas propuestas por el apelante. Al respecto, en la nueva regulación del artículo 270 de la ley de enjuiciamiento civil, merecen ser destacados dos aspectos importantes, a saber; de un lado, en relación con los documentos que sean de fecha posterior a la demanda o contestación, no es suficiente con que el documento, medio o instrumento sea, efectivamente, de fecha posterior, sino que es necesario, además, que no se hubiesen podido confeccionar ni obtener con anterioridad, poniéndose coto con ello a una práctica nada infrecuente de aportar como documentos nuevos aquellos que debieron y pudieron aportarse con la demanda o contestación, mediante el ardid de fecharlo con posterioridad; respecto de los documentos anteriores no resulta ya suficiente con el simple juramento de la parte que los presente de no haber tenido antes conocimiento de su existencia, --como era exigido por la ley de enjuiciamiento civil de 1881--, sino que resulta ahora preciso que la parte que los presente justifique esa circunstancia.


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
