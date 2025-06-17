# Tarification-non-vie
# Projet Actuariel : Tarification Non-Vie - Modélisation de la Prime Pure

## 🌟 Objectif

Ce projet vise à modéliser la prime pure (Pure Premium) d'un portefeuille d'assurance automobile non-vie en utilisant à la fois des méthodes traditionnelles (GLM Poisson) et des approches modernes de machine learning (XGBoost).

---

## 📂 Données

Le jeu de données contient plus de 670 000 contrats avec les informations suivantes :

* Variables explicatives : age du conducteur, puissance du véhicule, région, marque, etc.
* Variables cibles :

  * `ClaimNb` : nombre de sinistres (fréquence)
  * `ClaimAmount` : coût total des sinistres (sévérité)
  * `Exposure` : fraction de l'année assurée
  * `PurePremium` : créée comme `ClaimAmount / Exposure`

---

## 📊 Méthodologie

### 1. Exploration des données

* Analyse univariée des distributions
* Détection des outliers

### 2. Préparation

* Suppression des expositions nulles
* Encodage one-hot des variables qualitatives
* Création de la prime pure

### 3. Modélisation

* **GLM Poisson** : modélisation de la fréquence avec offset = log(Exposure)
* **XGBoost Regressor** : modélisation directe de la prime pure (fréquence x sévérité)

### 4. Évaluation

* RMSE / MAE sur la prime pure prédite
* Analyse de l'importance des variables
* Lecture du résumé statistique du GLM

---

## 📙 Structure du dépôt

```
/tarification-non-vie
├── data/
│   └── data.csv
├── outputs/
│   └── figures/
│       └── feature_importance_xgb.png
├── src/
│   └── model.py
├── README.md
└── requirements.txt
```

---

## 🎯 Performances (XGBoost)

* RMSE : \~X.XX
* MAE  : \~X.XX

*Le modèle XGBoost capture de manière plus flexible les non-linéarités que les GLMs tout en complétant une approche interprétable.*

---

## 🚀 Pour aller plus loin

* Ajouter un modèle Gamma pour la sévérité
* Tester des modèles Tweedie
* Intégrer une interface Streamlit pour simuler une tarification

---

## 🚫 Avertissement

Ce projet est à usage pédagogique. Il n'est pas destiné à un usage en production sans validation rigoureuse par des actuaires certifiés.

---

## 📚 Auteurs
