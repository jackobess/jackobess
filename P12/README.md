# 🌱 P12 – Agritech : recommandation de cultures par la donnée

Projet du parcours *Data Scientist Machine Learning* (OpenClassrooms).

L'objectif est de prédire les rendements agricoles et de recommander les cultures les plus adaptées, sur une chaîne ML complète : exploration et préparation des données, modélisation, API, application et MLOps.

**Stack :** Python · pandas · scikit-learn · LightGBM · FastAPI · Docker · Render · Streamlit · MLflow · GitHub Actions

## 🔗 Liens

- 💻 [Code source (dépôt OC_Projet12)](https://github.com/jackobess/OC_Projet12)
- 🚀 [Application Streamlit](https://ocprojet12-agritech-yield.streamlit.app/)
- ⚙️ [API (documentation Swagger)](https://agritech-api-latest.onrender.com/docs)
- 📄 [Rapport métier (PDF)](Bessire_Jacob_Rapport_metier_Agritech.pdf)
- 🖼️ [Présentation de soutenance (PDF)](projet12.pdf)

## 📝 Évaluation

**Validé le 13 novembre 2026**

### Notes de l'évaluateur

- **Ajuster les paramètres des procédures d'entraînement afin d'optimiser la performance** : Démarche structurée d'optimisation avec plusieurs expérimentations suivies dans MLflow. Hyperparamètres ajustés par RandomizedSearchCV et validation croisée GroupKFold. Modèles comparés sur des métriques pertinentes (RMSE, MAE, R²) ; choix final de LightGBM justifié par la validation croisée. Modèle final sauvegardé, rechargement vérifié.
- **Automatiser le déploiement en intégrant les évolutions du modèle** : Pipeline MLOps structuré automatisant prétraitement, entraînement et évaluation. Workflow GitHub Actions : tests, construction de l'image Docker, déploiement sur Render. Environnement reproductible, étapes bien organisées, gestion des erreurs prise en compte.

### Points forts

- Démarche de modélisation rigoureuse avec comparaison de plusieurs algorithmes.
- Utilisation pertinente de MLflow pour le suivi des expérimentations.
- Optimisation systématique des hyperparamètres et choix du modèle final justifié.
- Pipeline MLOps structuré avec séparation des étapes.
- Workflow CI/CD intégrant tests, construction et déploiement.
- Documentation et organisation du projet facilitant sa compréhension.

### Axes d'amélioration

- Approfondir l'analyse des écarts de performance entre validation croisée et jeu de test.
- Renforcer la traçabilité entre les versions de modèles enregistrées dans MLflow et celles déployées.
- Compléter la documentation des procédures de mise à jour et de redéploiement.

### Remarques sur la soutenance

- Démarche cohérente, de l'expérimentation des modèles jusqu'à l'automatisation de leur déploiement. Outils adaptés aux problématiques MLOps et d'intégration continue.
