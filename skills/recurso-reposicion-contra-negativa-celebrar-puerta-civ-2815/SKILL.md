---
name: recurso-reposicion-contra-negativa-celebrar-puerta-civ-2815
description: "Recurso de reposición contra la negativa a celebrar a puerta cerrada el juicio de paternidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición contra la negativa a celebrar a puerta cerrada el juicio de paternidad

> Formulario **CIV-2815** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 25-11-2026.

## Qué es

Escrito de interposición de recurso de reposición presentado en juicio sobre impugnación de paternidad matrimonial, contra la providencia que deniega la celebración de actos y vistas a puerta cerrada.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición contra la negativa a celebrar a puerta cerrada el juicio de paternidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición contra la negativa a celebrar a puerta cerrada el juicio de paternidad” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-reposicion-contra-negativa-celebrar-puerta-civ-2815`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] COMPLETAR (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE

## Normas que cita el formulario

- art. 754 LEC
- art. 138 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Conforme el art. 451 de la Ley de Enjuiciamiento Civil sólo procede recurso de reposición contra las resoluciones que adopten forma de providencia o de auto que no sea definitivo.

En cuanto a las resoluciones que adoptan forma de providencia, son recurribles en reposición, como norma general, aquellas a que se refiere el art. 206.2.1ª de la Ley de Enjuiciamiento Civil.

Por lo que se refiere a las resoluciones que toman forma de auto, recurribles en reposición, debemos tener en cuenta el art. 206.2.2ª de la Ley de Enjuiciamiento Civil, en relación con el art. 207.1. de dicho Texto Procesal, del que se deduce que son autos definitivos aquellos que ponen fin a la primera instancia o que decidan recursos interpuestos frente a estos últimos, es decir que, como norma general, son recurribles en reposición aquellos autos que resuelvan sobre cuestiones que no pongan fin a la instancia o al recurso antes de su ordinaria tramitación.

Ha de repararse en la circunstancia de que, como se ha dicho, el artículo 451 de la Ley de Enjuiciamiento Civil establece la procedencia del recurso de reposición con carácter general, ya que no procederá en aquellos supuestos a los que la Ley 1/2000 concede un régimen de impugnación específico o para los que no se prevé recurso (por citar un ejemplo, el art. 35 de la Ley de Enjuiciamiento Civil no prevé recurso en los casos de fijación de honorarios a los Abogados).

Conviene dejar constancia de que la LEC 1/2000, al igual que venía haciendo la LEC de 1881, no otorga efectos suspensivos a la interposición del recurso de reposición, circunstancia que en la práctica ha de tenerse muy presente para evitar el transcurso de plazos que supongan el decaimiento de algún derecho o preclusión de un trámite. La literalidad de este precepto no permitirá invocaciones fundadas en el derecho a la tutela judicial efectiva o interdicción de la indefensión.

En último término, señalar que el artículo 451 de la LEC 1/2000 se está refiriendo a resoluciones escritas. En cuanto a las resoluciones que en audiencias o vistas se dictan oralmente, debemos estar a la regulación específica, no sólo del recurso procedente, sino también del momento que el legislador establezca para su interposición y trámite. A falta de regulación específica se tendrá en cuenta lo establecido en el art. 210.2.de la Ley de Enjuiciamiento Civil, que exige la manifestación en el acto en que dicta la resolución oral de la voluntad de recurrirla, a los efectos contenidos el párrafo segundo de la disposición mencionada.

(2) La LEC 1/2000 ha intentado suplir la falta en nuestro Derecho Procesal Civil de unas normas generales sobre los recursos, lo que en reiteradas ocasiones se había puesto de manifiesto por la doctrina y la jurisprudencia (la LEC de 1881 no contenía preceptos de esta índole, regulando en los art.376 y siguientes individualmente el régimen jurídico de cada recurso)

Así, en primer término, el art.448, la Ley de Enjuiciamiento Civil reconoce el derecho al recurso. La controvertida cuestión sobre si el derecho al recurso tiene un origen constitucional que algunos han visto en una interpretación a ultranza del derecho a la tutela judicial efectiva reconocido en el artículo 24 de la Constitución, puede considerarse resuelta por la doctrina del Tribunal Constitucional en la que sólo al acceso a los recursos en la forma establecida por la Ley forma parte del mencionado derecho a la tutela judicial efectiva. Es el legislador quien al elaborar las leyes decide qué es recurrible y qué no es recurrible, sin que se le pueda exigir un sistema absoluto de doble instancia.

Dicho esto, conviene destacar dos circunstancias:

- El derecho al recurso se le reconoce a las partes. Esta mención tan específica puede acarrear numerosos problemas en la práctica, ya que una interpretación literalista llevará a rechazar inicialmente el recurso presentado por quien, viéndose afectado por la resolución judicial, no ha sido parte en el proceso. Desde luego es un tema complejo que el legislador debiera haber analizado en profundidad otorgando una solución que coordine elementos tan diferentes como el derecho a la tutela judicial efectiva, razones de economía procesal y la interdicción de la mala fe o abuso del derecho. El tema no es infrecuente, especialmente en fase de ejecución de sentencias donde la cuestión se complica notablemente ante el derecho a la ejecución de sentencia en sus propios términos, integrante, según reiterada doctrina del Tribunal Constitucional, del derecho a la tutela judicial.
- Quienes recurran las resoluciones judiciales han de verse afectados desfavorablemente por ellas. Sin duda, resulta positivo que se recoja con carácter general la idea del "perjuicio" como fundamento del derecho a recurrir. La cuestión está en si este aspecto puede ser controlado de oficio por el Juez para evitar la dilación y gastos que supone un recurso sin fundamento o si debe apreciarse, tras su tramitación, al resolver el recurso. Cabe pensar que esta nueva norma de aplicación general a los recursos haría deseable que en los escritos de parte interponiendo los mismos se sustituyera la habitual referencia a "por serme desfavorable" por una breve descripción del perjuicio que causa (pensemos en los recursos en materia de admisión de prueba).

(3) En materia de filiación -como en los procesos sobre capacidad, matrimonio y menores- la LEC 1/2000 no deroga el principio de publicidad de las actuaciones que con carácter general ordena el art. 138 LEC 1/2000. El artículo 754 se limita a suavizar la vigencia de aquél, dejando a criterio del órgano judicial la valoración de las circunstancias que, bien apreciadas de oficio bien invocadas por las partes, aconsejen que las actuaciones tengan carácter reservado. Este precepto se refiere tanto a las vistas como a las actuaciones, y sin embargo, su referencia al artículo 138.2. da inevitablemente la impresión de que sólo está pensando en las actuaciones orales, por lo que entendemos que ha de precisarse la siguiente cuestión: es diferente la limitación del principio de audiencia pública de las actuaciones orales de la publicidad de las actuaciones en general, referida especialmente al acceso a lo actuado mediante petición del examen de autos o libramiento de testimonios. En este último caso debemos estar a lo dispuesto con carácter general en el artículo 140.1. LEC 1/2000, que limita el acceso a quien acredite interés legítimo y al apartado 3. de este precepto que permite una mayor reserva en los términos prevenidos en él.

Ciertamente, y como ha señalado con acierto la doctrina científica, no se puede partir en abstracto de la idea de que los procesos en que se diluciden cuestiones de estado afectan a la moral, al orden público o son motivo u ocasión de escándalo (arts. 314, 572 LEC 1881); antes bien, incumbe a las partes y al órgano jurisdiccional valorar, en atención a la concreta situación concurrente, si se produce alguna de esas derivaciones, por lo que el tratamiento de la Ley 1/2000 puede considerarse correcto.

El artículo 754 de la Ley nada dice acerca del procedimiento para acordar estas limitaciones por lo que no parece que haya inconveniente alguno en seguir el trámite de audiencia a que se refiere el artículo 138.2. del mismo Texto, aunque no es explicable -sin duda es una muestra más de la falta de coordinación en la elaboración de la LEC 1/2000- que en el artículo 754 el legislador prevea que este acuerdo adopte la forma de providencia mientras que en el apartado 3. del artículo 138 se refiere a auto. Aún así debemos entender que es cuestión irrelevante en tanto la resolución esté debidamente motivada, aunque pueda no estar tan claro el régimen de recursos (contra las providencias procede recurso de reposición según el artículo 451, mientras que contra el auto a que se refiere el artículo 138.3. no cabe recurso alguno sin perjuicio de formular protesta) plausible a la disminución de garantías y solemnidades en la resolución -el Auto del art. 138.3 se sustituye aquí por una providencia-.


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
