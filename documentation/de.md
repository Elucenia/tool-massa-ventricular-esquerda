<!-- ELUCENIA technical documentation · massa-ventricular-esquerda · de · no clinical/professional/rights approval -->

# Linksventrikuläre Masse und Geometrie

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/massa-ventricular-esquerda)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Interventrikuläres Septum (Diastole)

`siv`

cm · Bereich: 0,4–3

### Linksventrikulärer diastolischer Durchmesser

`ddve`

cm · Bereich: 2–9

### Hinterwand (Diastole)

`ppve`

cm · Bereich: 0,4–3

### Gewicht

`peso`

kg · Bereich: 20–300

### Körpergröße

`altura`

cm · Bereich: 100–230

### Geschlecht

`sexo`

- `F` — Weiblich
- `M` — Männlich

## Fassung der Methode

Devereux 1986 korrigierte kubische Gleichung 0,8×1,04+0,6; ASE/EACVI 2015; Indexierung auf Mosteller-KOF

## Dokumentierte Formel

LV-Masse (g) = 0,8 × 1,04 × \[(SIV + DDVE + PP)³ − DDVE³\] + 0,6 (Maße in cm; SIV: Dicke des interventrikulären Septums, DDVE: linksventrikulärer enddiastolischer Innendurchmesser, PP: Dicke der Hinterwand; alle Messungen am Ende der Diastole)

Massenindex = Masse ÷ Körperoberfläche (Mosteller)

Relative Wanddicke (RWT) = 2 × PP ÷ DDVE

## Grenzen und Population

Die lineare ASE/EACVI-Methode von 2015 erfordert Maße in Zentimetern, die am Ende der Diastole und senkrecht zur Längsachse des Ventrikels erhoben werden. Sie setzt eine geeignete Geometrie voraus; asymmetrische Hypertrophie, Dilatation und regionale Unterschiede der Wanddicke können sie ungenau machen. Da die Messwerte kubiert werden, verändern kleine Erfassungsfehler die Masse. Referenzwerte der linearen und der 2D-Methode sowie unterschiedlicher körperbezogener Indexierungen dürfen nicht automatisch ausgetauscht werden.

## Referenzen

- [Lang RM et al. Recommendations for cardiac chamber quantification by echocardiography in adults (ASE/EACVI). J Am Soc Echocardiogr, 2015.](https://doi.org/10.1016/j.echo.2014.10.003)

- [Devereux RB et al. Echocardiographic assessment of left ventricular hypertrophy: comparison to necropsy findings. Am J Cardiol, 1986.](https://doi.org/10.1016/0002-9149(86)90771-X)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Dokumentierte Ergebnisse

Die folgenden Angaben bewahren die Ausgaben der Methode für synthetische Beispiele. Sie stellen keine unabhängige klinische Validierung dar.

### 1

Normale Geometrie

| Ergebnisdetails | |
| --- | --- |
| Linksventrikuläre Masse | 182 g |
| Körperoberfläche | 1,82 m² |
| Relative Wanddicke | 0,40 |


### 2

Konzentrische Hypertrophie

| Ergebnisdetails | |
| --- | --- |
| Linksventrikuläre Masse | 243 g |
| Körperoberfläche | 1,82 m² |
| Relative Wanddicke | 0,57 |

