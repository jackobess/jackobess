# 💳 P8 – Scoring crédit : déploiement et monitoring en production

Projet du parcours *Data Scientist Machine Learning* (OpenClassrooms).

Mise en production d'un modèle de scoring crédit : API dockerisée, pipeline CI/CD, journalisation des prédictions dans une base PostgreSQL, suivi du data drift et optimisation des performances par profilage.

**Stack :** Python · FastAPI · Docker · GitHub Actions · Hugging Face Spaces · PostgreSQL (Neon) · Evidently · cProfile

## 🔗 Liens

- 💻 [Code source (dépôt OC_Projet8)](https://github.com/jackobess/OC_Projet8)
- ⚙️ [API (documentation Swagger)](https://jackobess-oc-projet8.hf.space/docs)
- 🖼️ [Présentation de soutenance (PDF)](projet8.pdf)

## 📝 Évaluation

**Validé le 17 juillet 2026**

### Notes de l'évaluateur

- **Prendre vos premiers pas en ML Engineering** : Pipeline CI/CD automatisant les tests et le déploiement, avec déclenchement automatique (push, PR…). Build Docker pour une exécution reproductible partout. Stockage des données de production pour le monitoring du modèle.
- **Concevoir un système de suivi du cycle de vie du modèle** : Surveillance de l'évolution des données de production par rapport aux données d'entraînement, comparaison entre données de référence et nouvelles données.

### Points forts

- Analyse du data drift : surveillance de l'évolution des données de production par rapport aux données d'entraînement.
- Stratégie de stockage expliquée.
- Optimisation des performances de l'API.

### Axes d'amélioration

- RAS.