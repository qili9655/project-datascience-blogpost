# Métriques des Modèles - Saison 2020-2021

## Saison Régulière

| Modèle | AUC | Précision | Rappel | F1 |
|--------|----------|-----------|--------|--------|
| LR (distance) | 0.699031 | 0.000000 | 0.000000 | 0.000000 |
| LR (angle) | 0.559902 | 0.000000 | 0.000000 | 0.000000 |
| LR (distance+angle) | 0.715517 | 0.000000 | 0.000000 | 0.000000 |
| XGBoost (tuned+FS) | 0.567873 | 0.000000 | 0.000000 | 0.000000 |
| Ensemble (final) | 0.693603 | 0.317568 | 0.036321 | 0.065187 |

## Séries Éliminatoires (Playoffs)

| Modèle | AUC | Précision | Rappel | F1 |
|--------|----------|-----------|--------|--------|
| LR (distance) | 0.675961 | 0.000000 | 0.000000 | 0.000000 |
| LR (angle) | 0.573355 | 0.000000 | 0.000000 | 0.000000 |
| LR (distance+angle) | 0.698033 | 0.000000 | 0.000000 | 0.000000 |
| XGBoost (tuned+FS) | 0.565428 | 0.000000 | 0.000000 | 0.000000 |
| Ensemble (final) | 0.677020 | 0.285714 | 0.026087 | 0.047809 |

## Comparaison des AUC

| Modèle | Saison Régulière | Playoffs | Différence |
|--------|------------------|----------|------------|
| LR (distance) | 0.699031 | 0.675961 | -0.023070 |
| LR (angle) | 0.559902 | 0.573355 | +0.013453 |
| LR (distance+angle) | 0.715517 | 0.698033 | -0.017484 |
| XGBoost (tuned+FS) | 0.567873 | 0.565428 | -0.002445 |
| Ensemble (final) | 0.693603 | 0.677020 | -0.016583 |

## Observations

- **Meilleur modèle** : LR (distance+angle) avec AUC = 0.716 (saison régulière)
- **Généralisation** : Tous les modèles montrent des performances similaires entre saison régulière et playoffs
- **Problème de seuil** : Seul l'Ensemble produit des prédictions binaires (Précision, Rappel, F1 > 0)
- **Modèles sous-performants** : LR (angle) et XGBoost (AUC < 0.58)