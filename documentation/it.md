<!-- ELUCENIA technical documentation · massa-ventricular-esquerda · it · no clinical/professional/rights approval -->

# Massa del ventricolo sinistro e geometria ventricolare

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/massa-ventricular-esquerda)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Setto interventricolare (diastole)

`siv`

cm · intervallo: 0,4–3

### Diametro diastolico del ventricolo sinistro

`ddve`

cm · intervallo: 2–9

### Parete posteriore (diastole)

`ppve`

cm · intervallo: 0,4–3

### Peso

`peso`

kg · intervallo: 20–300

### Altezza

`altura`

cm · intervallo: 100–230

### Sesso

`sexo`

- `F` — Femminile
- `M` — Maschile

## Edizione del metodo

Devereux 1986 equazione cubica corretta 0,8×1,04+0,6; ASE/EACVI 2015; indicizzazione SC Mosteller

## Formula documentata

Massa del VS (g) = 0,8 × 1,04 × \[(SIV + DDVE + PP)³ − DDVE³\] + 0,6 (misure in cm; SIV: spessore del setto interventricolare, DDVE: diametro interno telediastolico del ventricolo sinistro, PP: spessore della parete posteriore; tutte le misure a fine diastole)

Indice di massa = massa ÷ superficie corporea (Mosteller)

Spessore parietale relativo (SPR) = 2 × PP ÷ DDVE

## Limiti e popolazione

Il metodo lineare ASE/EACVI 2015 richiede dimensioni in centimetri ottenute alla fine della diastole e perpendicolari all’asse lungo del ventricolo. Dipende da una geometria adeguata; l’ipertrofia asimmetrica, la dilatazione e la variazione regionale dello spessore possono renderlo impreciso. Poiché le misure vengono elevate al cubo, piccoli errori di acquisizione alterano la massa. I riferimenti dei metodi lineare e 2D e delle diverse indicizzazioni corporee non devono essere scambiati automaticamente.

## Riferimenti

- [Lang RM et al. Recommendations for cardiac chamber quantification by echocardiography in adults (ASE/EACVI). J Am Soc Echocardiogr, 2015.](https://doi.org/10.1016/j.echo.2014.10.003)

- [Devereux RB et al. Echocardiographic assessment of left ventricular hypertrophy: comparison to necropsy findings. Am J Cardiol, 1986.](https://doi.org/10.1016/0002-9149(86)90771-X)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
