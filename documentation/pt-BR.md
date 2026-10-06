<!-- ELUCENIA technical documentation · massa-ventricular-esquerda · pt-BR · no clinical/professional/rights approval -->

# Massa do VE e geometria ventricular

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/massa-ventricular-esquerda)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Septo interventricular (diástole)

`siv`

cm · intervalo: 0,4–3

### Diâmetro diastólico do VE

`ddve`

cm · intervalo: 2–9

### Parede posterior (diástole)

`ppve`

cm · intervalo: 0,4–3

### Peso

`peso`

kg · intervalo: 20–300

### Altura

`altura`

cm · intervalo: 100–230

### Sexo

`sexo`

- `F` — Feminino
- `M` — Masculino

## Edição do método

Devereux 1986 equação cúbica corrigida 0,8×1,04+0,6; ASEEACVI 2015; indexação SCMosteller

## Fórmula documentada

Massa do VE (g) = 0,8 × 1,04 × \[(SIV + DDVE + PP)³ − DDVE³\] + 0,6 (medidas em cm)

Índice de massa = massa ÷ superfície corporal (Mosteller)

Espessura relativa da parede (ERP) = 2 × PP ÷ DDVE

## Limites e população

O método linear ASE/EACVI 2015 requer dimensões em centímetros obtidas ao final da diástole e perpendiculares ao eixo longo do ventrículo. Depende de geometria adequada; hipertrofia assimétrica, dilatação e variação regional da espessura podem torná-lo inexato. Como as medidas são elevadas ao cubo, pequenos erros de aquisição alteram a massa. Referências de métodos linear, 2D e indexações corporais diferentes não devem ser intercambiadas automaticamente.

## Referências

- [Lang RM et al. Recommendations for cardiac chamber quantification by echocardiography in adults (ASE/EACVI). J Am Soc Echocardiogr, 2015.](https://doi.org/10.1016/j.echo.2014.10.003)

- [Devereux RB et al. Echocardiographic assessment of left ventricular hypertrophy: comparison to necropsy findings. Am J Cardiol, 1986.](https://doi.org/10.1016/0002-9149(86)90771-X)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

Geometria normal

| Detalhes do resultado | |
| --- | --- |
| Massa do VE | 182 g |
| Superfície corporal | 1,82 m² |
| Espessura relativa da parede | 0,40 |


### 2

Hipertrofia concêntrica

| Detalhes do resultado | |
| --- | --- |
| Massa do VE | 243 g |
| Superfície corporal | 1,82 m² |
| Espessura relativa da parede | 0,57 |

