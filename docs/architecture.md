# Architecture du projet

## Objectif
Mettre en place une première chaîne de traitement Big Data pour des images de fruits.

## Briques principales
- **Amazon S3** : stockage des images d'entrée et des résultats
- **AWS EMR** : cluster de calcul distribué
- **PySpark** : traitement distribué des images
- **TensorFlow / Keras** : extraction de features via MobileNetV2
- **Spark ML PCA** : réduction de dimension

## Pipeline
S3 (images) -> Spark / EMR -> preprocessing -> MobileNetV2 -> broadcast des poids -> PCA -> S3 (résultats)
