# Mise en place AWS

## Services utilisés
- IAM pour les permissions
- S3 pour le stockage
- EMR pour le calcul distribué

## Principes retenus
- stockage et calcul dans une région européenne
- utilisation d'un cluster EMR seulement pour les tests et les démonstrations
- arrêt du cluster après usage pour limiter les coûts

## Données
- images d'entrée stockées sur S3
- résultats bruts et résultats PCA stockés sur S3 au format Parquet
