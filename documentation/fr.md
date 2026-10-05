<!-- ELUCENIA technical documentation · massa-ventricular-esquerda · fr · no clinical/professional/rights approval -->

# Masse et géométrie du ventricule gauche

[conditions, sources et autorisations](https://elucenia.org/fr/outils/massa-ventricular-esquerda)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Septum interventriculaire (diastole)

`siv`

cm · intervalle: 0,4–3

### Diamètre diastolique du ventricule gauche

`ddve`

cm · intervalle: 2–9

### Paroi postérieure (diastole)

`ppve`

cm · intervalle: 0,4–3

### Poids

`peso`

kg · intervalle: 20–300

### Taille

`altura`

cm · intervalle: 100–230

### Sexe

`sexo`

- `F` — Féminin
- `M` — Masculin

## Édition de la méthode

Devereux 1986 équation cubique corrigée 0,8×1,04+0,6 ; ASE/EACVI 2015 ; indexation surface corporelle Mosteller

## Formule documentée

Masse du VG (g) = 0,8 × 1,04 × \[(SIV + DDVE + PP)³ − DDVE³\] + 0,6 (mesures en cm ; SIV : épaisseur du septum interventriculaire, DDVE : diamètre interne télédiastolique du ventricule gauche, PP : épaisseur de la paroi postérieure ; toutes les mesures en fin de diastole)

Indice de masse = masse ÷ surface corporelle (Mosteller)

Épaisseur pariétale relative (EPR) = 2 × PP ÷ DDVE

## Limites et population

La méthode linéaire ASE/EACVI 2015 exige des dimensions en centimètres mesurées en fin de diastole et perpendiculaires au grand axe du ventricule. Elle dépend d’une géométrie appropriée ; l’hypertrophie asymétrique, la dilatation et les variations régionales d’épaisseur peuvent la rendre inexacte. Les mesures étant élevées au cube, de petites erreurs d’acquisition modifient la masse. Les références des méthodes linéaire et 2D et des différentes indexations corporelles ne doivent pas être interchangées automatiquement.

## Références

- [Lang RM et al. Recommendations for cardiac chamber quantification by echocardiography in adults (ASE/EACVI). J Am Soc Echocardiogr, 2015.](https://doi.org/10.1016/j.echo.2014.10.003)

- [Devereux RB et al. Echocardiographic assessment of left ventricular hypertrophy: comparison to necropsy findings. Am J Cardiol, 1986.](https://doi.org/10.1016/0002-9149(86)90771-X)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
