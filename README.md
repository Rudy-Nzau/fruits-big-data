#  Fruits! - Big Data Image Processing Pipeline (AWS EMR)

##  Contexte

Ce projet a été réalisé dans le cadre d’un cas d’usage pour la startup **Fruits!**, spécialisée en AgriTech.

L’objectif est de construire une première **chaîne de traitement Big Data** permettant d’analyser des images de fruits afin de préparer un futur système de classification.

---

##  Objectifs

- Charger des images depuis le cloud (Amazon S3)
- Prétraiter les images
- Extraire des caractéristiques visuelles via **MobileNetV2**
- Distribuer les poids du modèle avec **Spark Broadcast**
- Réduire la dimension des données avec une **PCA PySpark**
- Stocker les résultats dans le cloud

---

##  Architecture

S3 (images)
↓
Spark / EMR
↓
Preprocessing
↓
MobileNetV2 (feature extraction)
↓
Broadcast des poids
↓
PCA (réduction dimension)
↓
S3 (résultats)


---

##  Stack technique

- Python
- PySpark
- TensorFlow / Keras
- AWS S3
- AWS EMR
- Spark ML (PCA)

---

## Structure du projet

notebooks/ → notebook principal
scripts/ → scripts utilitaires (bootstrap EMR)
docs/ → documentation technique
reports/ → présentation + figures
deliverables/ → livrables officiels


---

## Pipeline

1. Lecture des images depuis S3
2. Préprocessing (resize, normalisation)
3. Extraction de features avec MobileNetV2
4. Distribution du modèle via broadcast Spark
5. Réduction de dimension (PCA)
6. Sauvegarde sur S3

---

## Résultats

Chaque image est transformée en :
- un label
- un vecteur de caractéristiques réduit

Format de sortie : **Parquet**

---

## Limites

- coût du cluster EMR
- complexité de configuration cloud
- perte d’information possible avec PCA

---

## Améliorations possibles

- optimisation du nombre de composantes PCA
- ajout de monitoring
- gestion avancée des erreurs images
- migration vers Databricks

---

##  Auteur

Rudy Nzau
