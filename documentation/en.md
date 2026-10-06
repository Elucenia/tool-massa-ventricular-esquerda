<!-- ELUCENIA technical documentation · massa-ventricular-esquerda · en · no clinical/professional/rights approval -->

# Left ventricular mass and geometry

[conditions, sources and permissions](https://elucenia.org/en/tools/massa-ventricular-esquerda)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Interventricular septum (diastole)

`siv`

cm · range: 0.4–3

### Left ventricular diastolic diameter

`ddve`

cm · range: 2–9

### Posterior wall (diastole)

`ppve`

cm · range: 0.4–3

### Weight

`peso`

kg · range: 20–300

### Height

`altura`

cm · range: 100–230

### Sex

`sexo`

- `F` — Female
- `M` — Male

## Method edition

Devereux 1986 corrected cubic equation 0.8×1.04+0.6; ASE/EACVI 2015; Mosteller BSA indexing

## Documented formula

LV mass (g) = 0.8 × 1.04 × \[(SIV + DDVE + PP)³ − DDVE³\] + 0.6 (measurements in cm; SIV: interventricular septum thickness, DDVE: left ventricular internal end-diastolic diameter, PP: posterior wall thickness; all measured at end-diastole)

Mass index = mass ÷ body surface area (Mosteller)

Relative wall thickness (RWT) = 2 × PP ÷ DDVE

## Limits and population

The ASE/EACVI 2015 linear method requires dimensions in centimeters measured at end-diastole and perpendicular to the ventricular long axis. It depends on suitable geometry; asymmetric hypertrophy, dilation and regional variation in wall thickness may make it inaccurate. Because the measurements are cubed, small acquisition errors change the mass. Reference values for linear and 2D methods and different body-size indexing methods must not be automatically interchanged.

## References

- [Lang RM et al. Recommendations for cardiac chamber quantification by echocardiography in adults (ASE/EACVI). J Am Soc Echocardiogr, 2015.](https://doi.org/10.1016/j.echo.2014.10.003)

- [Devereux RB et al. Echocardiographic assessment of left ventricular hypertrophy: comparison to necropsy findings. Am J Cardiol, 1986.](https://doi.org/10.1016/0002-9149(86)90771-X)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

Normal geometry

| Result details | |
| --- | --- |
| Left ventricular mass | 182 g |
| Body surface area | 1.82 m² |
| Relative wall thickness | 0.40 |


### 2

Concentric hypertrophy

| Result details | |
| --- | --- |
| Left ventricular mass | 243 g |
| Body surface area | 1.82 m² |
| Relative wall thickness | 0.57 |

