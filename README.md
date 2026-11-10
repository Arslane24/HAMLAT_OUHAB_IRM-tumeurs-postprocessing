# Détection de tumeurs cérébrales sur IRM — focus post-traitement

Projet de la matière « Analyse et restitution ».

## Problématique
Les modèles de segmentation (YOLO-seg, Mask R-CNN, SAM 3) produisent des masques bruités :
faux îlots, trous internes, contours crénelés. Notre objectif est de mesurer, par une étude
d'ablation chiffrée, quel post-traitement améliore la segmentation (Dice, IoU, HD95)
**sans perdre de petites tumeurs réelles**, puis de recommander un pipeline par modèle.

> Ce projet est une aide à la décision, pas un outil de diagnostic.

## Données
Brain MRI Segmentation (Kaggle, LGG), environ 110 patients, découpage **par patient** (70/15/15).
Les images ne sont pas versionnées : elles seront téléchargées via `scripts/download.py`.


