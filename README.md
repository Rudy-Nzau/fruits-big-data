# Fruits! - Big Data image processing pipeline on AWS

Projet réalisé dans le cadre d'un cas AgriTech visant à construire une première chaîne de traitement Big Data pour des images de fruits.

## Objectif
Mettre en place un pipeline scalable capable de :
- lire des images depuis Amazon S3
- prétraiter les images
- extraire des features avec MobileNetV2
- diffuser les poids du modèle sur les workers Spark
- réduire la dimension avec une PCA PySpark
- sauvegarder les résultats sur S3

## Stack technique
- Python
- PySpark
- TensorFlow / Keras
- AWS S3
- AWS EMR
- Spark ML PCA

## Structure du projet
- `notebooks/` : notebook principal
- `scripts/` : scripts utilitaires, dont bootstrap EMR
- `docs/` : documentation architecture et AWS
- `reports/` : présentation et figures
- `deliverables/` : livrables officiels

## Pipeline
S3 -> lecture des images -> preprocessing -> MobileNetV2 -> features -> PCA -> S3

## Livrables
- notebook PySpark
- données / résultats
- support de présentation

## Remarques
Le projet met l'accent sur la scalabilité et l'architecture Big Data plutôt que sur l'entraînement d'un modèle final.
