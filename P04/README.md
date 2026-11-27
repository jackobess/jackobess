# 👥 P4 – Classification : prédire l'attrition RH

Projet du parcours *Data Scientist Machine Learning* (OpenClassrooms).

Classification du risque de démission des employés : comparaison de modèles (régression logistique, XGBoost, Gradient Boosting), choix du seuil de décision selon le compromis rappel / précision, et explicabilité des prédictions avec SHAP pour orienter les actions RH.

**Stack :** Python · pandas · scikit-learn · XGBoost · SHAP

## 🔗 Liens

- 🖼️ [Présentation de soutenance (PDF)](Bessire_Jacob_P4_3_Presentation.pdf)

## 📝 Évaluation

**Validé le 20 mai 2026**

### Notes de l'évaluateur

- **Configurer l'environnement de travail nécessaire à l'exploitation des données** : Fichier pyproject.toml fourni avec tous les packages nécessaires au projet.
- **Entraîner un modèle d'apprentissage** : Plusieurs modèles de classification supervisée entraînés (régression logistique, XGBoost, Gradient Boosting), avec des techniques de gestion du déséquilibre des classes pour chacun et une optimisation des hyperparamètres.
- **Évaluer le modèle d'apprentissage** : Modèles comparés sur trois métriques (rappel, précision, AUC). Analyse des features importantes pour l'explication globale et SHAP pour les interprétations individuelles.
- **Mettre en place un processus de nettoyage afin d'améliorer la qualité des données** : Étude préalable de la qualité des données : valeurs manquantes, doublons et structure.
- **Préparer et transformer des données afin de les adapter au modèle** : Variables catégorielles encodées avec trois techniques selon leur nature (label encoding, one-hot encoding, ordinal encoding). Normalisation avec StandardScaler.

### Points forts

- La présentation
- L'optimisation des hyperparamètres
- La gestion du compromis rappel / précision
- L'analyse SHAP

### Axes d'amélioration

- L'utilisation de SMOTE pour le rééchantillonnage.

### Remarques sur la soutenance

- RAS.