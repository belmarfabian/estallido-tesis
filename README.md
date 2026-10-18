# Tesis sobre el estallido social

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23455927.svg)](https://doi.org/10.5281/zenodo.23455927)

Mapa longitudinal y base de referencias sobre las interpretaciones del estallido social chileno de 2019.

## Autoría

- **Tipología de las cuatro tesis** (transformacional, populista, estructural e insurreccional): Cristóbal Bellolio. Bellolio, C. [@cbellolio]. (2026, 17 de octubre). *A propósito del aniversario del 18O, hice un barrido por la literatura académica…* [Hilo]. X. https://x.com/cbellolio/status/2111498263115272614
- **Asignación de obras, subcorrientes, codificación de mecanismos, variables y visualización**: elaboración propia (Fabián Belmar). Bellolio no participó en la ubicación de los autores.

La base no se limita a la tipología de Bellolio. Las obras que no calzan en las cuatro tesis van a «Otras lecturas», y la codificación de mecanismos causales ofrece una segunda clasificación, independiente de esa tipología (ver `datos/libro_de_codigos.csv`).

- Visor interactivo: https://belmarfabian.github.io/estallido-tesis/
- Datos: `datos/tesis_estallido.csv` y `datos/tesis_estallido.json` (se generan con `datos/build.py`)
- Figuras: `figuras/figura_mapa_estallido.png` (tipología de Bellolio, claro), `figuras/figura_mapa_estallido_oscuro.png` y `figuras/figura_mapa_emergente.png` (mecanismos causales)
- Libro de códigos: `datos/libro_de_codigos.csv`; prueba de confiabilidad: `datos/confiabilidad.csv`
- Proponer una obra: usa el [formulario](https://github.com/belmarfabian/estallido-tesis/issues/new?template=nueva-obra.yml), aunque la obra no calce en la tipología de Bellolio.

## Variables

| Campo | Descripción |
|---|---|
| id | Identificador único |
| etiqueta | Autor y año, como aparece en la figura |
| autores | Autores o fuente |
| anio | Año de publicación o declaración |
| tesis | Tesis de Bellolio, u «Otras lecturas» |
| subcorriente | Variante dentro de la tesis (elaboración propia) |
| mecanismos | Códigos de todos los mecanismos causales que invoca la obra, separados por `;` (ver libro de códigos) |
| mecanismo_principal | Código del mecanismo central del argumento |
| confianza_codificacion | `alta` (texto leído), `media` o `baja` (codificación desde resúmenes o reseñas) |
| registro | `investigacion` (artículo arbitrado, monografía académica basada en evidencia, encuesta), `ensayo` (libro o capítulo interpretativo sin evidencia original sistemática) u `opinion` (texto breve: columna, crónica de prensa, entrevista, declaración, publicación en redes o documento de gobierno o de centro de estudios). Un libro nunca se clasifica como opinión |
| rol | `principal` o `antecedente` (anterior al 18-O) |
| referencia | Referencia completa |
| fuente_url | Fuente que verifica autor, año y argumento |
| nota | Observaciones |


## Confiabilidad

Un segundo codificador clasificó las 41 obras a ciegas con las mismas definiciones y el mismo libro de códigos. Fue un modelo de lenguaje, no una persona, por lo que la prueba es un contraste preliminar. Acuerdo en la tesis: 40 de 41 (kappa de Cohen = 0,97). Registro: kappa = 0,96. Mecanismo principal: kappa = 0,83. Conjunto de mecanismos: alfa de Krippendorff = 0,64, bajo el umbral de 0,667 para conclusiones tentativas (Krippendorff, 2004, pp. 241–243). Las dos codificaciones están en `datos/confiabilidad.csv`.

## Criterios

Solo se incluyen obras cuyo autor, año y argumento se verificaron en una fuente publicada. Cada obra se ubica en la tesis que domina su argumento sobre las causas del estallido. Las obras que no calzan en las cuatro tesis van a «Otras lecturas». Algunas obras son casos límite entre dos tesis; la columna `nota` lo indica. Cada referencia se verificó contra la fuente enlazada en `fuente_url`.

## Cómo citar

Belmar, F. (2026). *Tesis sobre el estallido social: mapa longitudinal y base de referencias* [Conjunto de datos]. Zenodo. https://doi.org/10.5281/zenodo.23455927

Si usas la tipología, cita también a Bellolio (2026).

Licencia: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es).
