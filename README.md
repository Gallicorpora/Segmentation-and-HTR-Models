Segmentation and HTR models

## Données 

Les données qui ont servi à l'entrainement des différents modèles sont issues du données disponibles dans les différents dépôts du projet Gallicropora : https://github.com/Gallicorpora, ainsi que des dépôts préexistants suivants :

- Cremma Medieval : https://github.com/HTR-United/cremma-medieval
- OCR17 : https://github.com/Heresta/OCR17plus
- FONDUE-FR-PRINT-16 :https://github.com/FoNDUE-HTR/FONDUE-FR-PRINT-16
- Pictocatalogs - Datasets for catalogs OCR and segmentation, https://github.com/PictoCatalogs/TrainingDataOCR

Elles sont au format alto (v.4) et suivent les normes de segmentation SegmOnto (https://segmonto.github.io). Toutes les données sont cataloguées sur HTR-United (https://htr-united.github.io). 

## Modèles

### Segmentation
Deux modèles de segmentation sont proposés ici :

- Un modèle de segmentation affiné à partir de blla.mlmodel qui est le modèle par défaut de segmentation de Kraken à l'aide de toutes les données de Gallicorpora et d’autres datasets cités ci-dessus. Toutefois pour l'instant les résultats ne sont pas satisfaisants.
- Un modèle entrainé à partir de YALtAi (afin de dépasser les difficultés rencontrées avec Kraken) et des mmêmes données que le modèle précédents. Les résultats sont, sans être parfaits, sont bien plus encourageants. Voir présentation : Ariane Pinche, Kelly Christensen, Simon Gabay. Between automatic and manual encoding: Towards a generic TEI model for historical prints and manuscripts. TEI 2022 conference : Text as data, Sep 2022, Newcastle, United Kingdom. ⟨10.5281/zenodo.7092214⟩. ⟨hal-03780302⟩

### HTR

Le projet a permis d'entrainer deux premiers modèles très encourageants :

- Le modèle *Gallicorpora+* pour les imprimés du 16e au 19e siècle (98,66%, test score). Le modèle à été entrainé à partir de tous les dépôts du projet Gallica en dehors de manuscrits du 15 et des dépôts suivants : *OCR17*, *FONDUE-FR-PRINT-16*, *Pictocatalogs - Datasets for catalogs OCR and segmentation*.
- Le modèle *Cremma-medievalGallicorpora15*, aussi appelé *Cortado*, pour les manuscrits et les incunables (95.54%, test score).  Le modèle a été entrainé à partir des dépôts des manuscrits et des incubalbes du 15e siècle du projet Gallica, ainsi que du dépôt *Cremma Medieval*.

Les modèles sont encore en cours d'amélioration et seront très bientôt disponibles sur Zenodo et directement dans kraken.

## Financeur

Ce projet est financé par le dataLab de la BnF (https://www.bnf.fr/fr/bnf-datalab).

## Projet

Gallicorpora propose de consolider et d'appliquer une chaîne de traitement pour les documents anciens de Gallica en diachronie longue, des premiers manuscrits français aux imprimés révolutionnaires. Au-delà de la simple extraction de texte en masse, nous améliorerons les jeux de données d'entraînement pour l'apprentissage machine, les outils et les modèles déjà existants pour l'extraction, l'annotation et la diffusion de données richement annotées provenant des collections de la Bibliothèque nationale de France (BnF).

## Citer le projet 

*Gallic(orpor)a: extraction, annotation et diffusion de l'information textuelle et visuelle en diachronie longue*, Benoît Sagot, Laurent Romary, Rachel Bawden, Pedro Javier Ortiz Suárez, Simon Gabay, Ariane Pinche, and Jean-Baptiste Camps.

## Infrastructure

Il est produit sur l'infrastructure du projet CREMMA (https://www.dim-map.fr/projets-soutenus/cremma/).
Les données pour l'HTR sont produites à l'aide de l'interface eScriptorium (https://gitlab.com/scripta/escriptorium).
Les données de lemmatisation sont produites à l'aide de l'interface Pyrrha (https://dh.chartes.psl.eu/pyrrha/).
