# Tarification Non-Vie - Assurance Auto (GLM)

Ce projet modélise la prime pure d'assurance automobile à l'aide de deux modèles GLM séparés : un pour la fréquence (Poisson) et un pour la sévérité (Gamma), conformément à l'approche classique utilisée en actuariat.

---

## 📦 Données

- Jeux de données publics `freMTPL2freq` et `freMTPL2sev` issus du package R [`CASdatasets`](https://cran.r-project.org/web/packages/CASdatasets/).

---

## 🧠 Objectifs

- Analyse exploratoire (EDA) et préparation des données
- Modélisation fréquence × sévérité avec GLM
- Estimation des primes pures et commerciales
- Évaluation de la rentabilité via le taux de sinistralité

---

## ⚙️ Technologies utilisées

- Python 3.11
- `rpy2`, `pandas`, `scikit-learn`, `statsmodels`, `matplotlib`, `seaborn`
- R + CASdatasets (via rpy2)

---

## 📈 Résultats

- Déviance Poisson (fréquence) : 0.47
- Déviance Gamma (sévérité) : 1.55
- Taux de sinistralité estimé : 92.54%

---

## 📁 Fichier principal

📍 `Notebook/Tarification non-vie.ipynb`

---

## 🧾 Recommandations

- Possibilités d’amélioration : validation croisée, modèles alternatifs (Tweedie, GBM)
- Proposition d’estimation rigoureuse du chargement commercial (hors modèle)

---
