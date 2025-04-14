# 📉 Bank Distress Prediction

Ce projet vise à prédire la faillite d'une entreprise à partir de ses **ratios financiers**, en s'appuyant sur la méthodologie **CRISP-DM** (Cross Industry Standard Process for Data Mining).

## 🔍 Objectif

Classer les entreprises selon leur **santé financière** :  
- `0` : Entreprise saine  
- `1` : Entreprise en difficulté ou en faillite

## 🧠 Données

- **Source** : [Taiwanese Bankruptcy Prediction](https://archive.ics.uci.edu/dataset/572/taiwanese+bankruptcy+prediction) – UCI Machine Learning Repository  
- **Période** : 1999 à 2009  
- **Volume** : 6819 entreprises, 95 variables explicatives (valeurs continues)  
- **Variable cible** : `Bankrupt?` (0 ou 1)  
- **Licence** : Creative Commons Attribution 4.0 International (CC BY 4.0)

## 📈 Méthodologie CRISP-DM

### 1. Compréhension métier
Prédire le risque de faillite d’une entreprise à partir de ses indicateurs comptables/financiers.

### 2. Compréhension des données
- Exploration des ratios financiers
- Vérification de la qualité des données
- Analyse des distributions, des valeurs aberrantes et des corrélations

### 3. Préparation des données
- Nettoyage
- Normalisation (RobustScaler + Yeo-Johnson)
- Échantillonnage pour équilibrer les classes (0/1)

### 4. Modélisation
- **Régression logistique** avec `class_weight='balanced'`
- Sauvegarde des datasets transformés (`train`, `test`) et du modèle `.pkl`

### 5. Évaluation
- **Courbe ROC**
- **Matrice de confusion**
- **Rapport de classification** : précision, rappel, F1-score

### 6. Déploiement (non réalisé ici, mais modèle sauvegardé)

## 📊 Résultats

| Classe            | Précision | Rappel | F1-score |
|------------------|-----------|--------|----------|
| Non-faillite (0) |    0.80   |  0.80  |   0.80   |
| Faillite (1)     |    0.80   |  0.80  |   0.80   |

- **Accuracy globale** : `80%`

