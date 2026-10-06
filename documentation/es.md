<!-- ELUCENIA technical documentation · massa-ventricular-esquerda · es · no clinical/professional/rights approval -->

# Masa del ventrículo izquierdo y geometría ventricular

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/massa-ventricular-esquerda)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Tabique interventricular (diástole)

`siv`

cm · intervalo: 0,4–3

### Diámetro diastólico del ventrículo izquierdo

`ddve`

cm · intervalo: 2–9

### Pared posterior (diástole)

`ppve`

cm · intervalo: 0,4–3

### Peso

`peso`

kg · intervalo: 20–300

### Estatura

`altura`

cm · intervalo: 100–230

### Sexo

`sexo`

- `F` — Femenino
- `M` — Masculino

## Edición del método

Devereux 1986 ecuación cúbica corregida 0,8×1,04+0,6; ASE/EACVI 2015; indexación SC Mosteller

## Fórmula documentada

Masa del VI (g) = 0,8 × 1,04 × \[(SIV + DDVE + PP)³ − DDVE³\] + 0,6 (medidas en cm; SIV: espesor del septo interventricular, DDVE: diámetro interno telediastólico del ventrículo izquierdo, PP: espesor de la pared posterior; todas las medidas al final de la diástole)

Índice de masa = masa ÷ superficie corporal (Mosteller)

Espesor relativo de pared (EPR) = 2 × PP ÷ DDVE

## Límites y población

El método lineal ASE/EACVI 2015 requiere dimensiones en centímetros obtenidas al final de la diástole y perpendiculares al eje largo del ventrículo. Depende de una geometría adecuada; la hipertrofia asimétrica, la dilatación y la variación regional del grosor pueden hacerlo inexacto. Como las medidas se elevan al cubo, pequeños errores de adquisición alteran la masa. Las referencias de los métodos lineal y 2D y de distintas indexaciones corporales no deben intercambiarse automáticamente.

## Referencias

- [Lang RM et al. Recommendations for cardiac chamber quantification by echocardiography in adults (ASE/EACVI). J Am Soc Echocardiogr, 2015.](https://doi.org/10.1016/j.echo.2014.10.003)

- [Devereux RB et al. Echocardiographic assessment of left ventricular hypertrophy: comparison to necropsy findings. Am J Cardiol, 1986.](https://doi.org/10.1016/0002-9149(86)90771-X)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

Geometría normal

| Detalles del resultado | |
| --- | --- |
| Masa del VI | 182 g |
| Superficie corporal | 1,82 m² |
| Espesor relativo de la pared | 0,40 |


### 2

Hipertrofia concéntrica

| Detalles del resultado | |
| --- | --- |
| Masa del VI | 243 g |
| Superficie corporal | 1,82 m² |
| Espesor relativo de la pared | 0,57 |

