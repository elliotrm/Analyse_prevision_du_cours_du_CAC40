# Projet M1 Master MAS

# Étude du cours du CAC40 📈

## Auteurs
- **Elliot Rault-Maisonneuve**
- **Benoît Grandlin**

## Date
- **19 avril 2025**

## Description du projet

Dans ce projet, nous analysons et prévoyons l'évolution de l'indice boursier **CAC 40**, principal indice de la Bourse de Paris.

Notre objectif est double :
- Étudier le comportement temporel de la série des **cours d’ouverture** du CAC 40,
- Réaliser des **prévisions** sur le mois de janvier 2025 à l'aide de différents modèles statistiques.

---

## Démarche

### 1. **Préparation et nettoyage des données**
- Importation des données historiques du CAC 40.
- Intégration de calendriers spécifiques (jours fériés, vacances de Noël).
- Remplacement des données manquantes par la moyenne des valeurs voisines.

### 2. **Analyse exploratoire**
- Visualisation des tendances, saisons et comportements extrêmes.
- Tests de stationnarité (**ADF** et **Phillips-Perron**) pour déterminer le besoin de différenciation.
- Décomposition pour identifier tendance et saisonnalité.

### 3. **Modélisation et prévision**
Trois méthodes sont comparées :
- **ARIMA** (Auto-Regressive Integrated Moving Average)
- **Holt-Winters** (exponentielle lissée sans saisonnalité)
- **Prophet** (développé par Facebook)

Chaque méthode est évaluée en comparant les prédictions aux valeurs réelles de janvier 2025.

---

## Technologies utilisées 🛠

- **R** (langage principal)
- **Libraries :**
  - `dplyr`, `tidyverse`, `ggplot2`
  - `forecast`, `astsa`, `urca`
  - `prophet`
  - `xts`, `readxl`

---

## Organisation des fichiers 📁

| Dossier/Fichier | Contenu |
|:----------------|:--------|
| `data/` | Dossiers de données (`Data_TS.xlsx`, `dates_jf.xlsx`, `dates_vc_noel.xlsx`, `dates_pred.xlsx`) |
| `script.Rmd` | Script complet d’analyse et de modélisation |
| `README.md` | Présentation du projet (ce fichier) |

---

## Résultats principaux

- La série du CAC 40 est **non stationnaire** ; elle nécessite une double différenciation pour modélisation.
- **ARIMA** fournit une prévision modérée mais ne capture pas la forte croissance de janvier 2025.
- **Holt-Winters** surestime la tendance haussière.
- **Prophet** propose une prévision plus souple mais reste perfectible face aux retournements rapides.

---

## Visualisation finale

Le résultat de notre analyse ainsi que les prévisions sont intégrés dans un **dashboard Power BI** pour une meilleure visualisation interactive des tendances, comparaisons entre modèles et performances de prédiction.

---

## Remarques

📌 Le comportement boursier, influencé par des événements exogènes (économie, géopolitique), complique l'usage de modèles purement statistiques.

---
