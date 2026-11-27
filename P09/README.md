# 🎭 P9 – Système RAG : assistant culturel de Nantes

Projet du parcours *Data Scientist Machine Learning* (OpenClassrooms).

Conception et déploiement d'un chatbot RAG qui répond aux questions sur les événements culturels de Nantes, à partir des données OpenAgenda : indexation vectorielle, pré-filtrage structuré avant la recherche, génération avec Mistral, API conteneurisée et évaluation sur un jeu de tests.

**Stack :** Python · OpenAgenda API · FAISS · Mistral (embeddings + LLM) · FastAPI · Docker · Ragas

## 🔗 Liens

- 💻 [Code source (dépôt OC_Projet9)](https://github.com/jackobess/OC_Projet9)
- 🖼️ [Présentation de soutenance (PDF)](projet9.pdf)

## 📝 Évaluation

**Validé le 3 septembre 2026**

### Notes de l'évaluateur

- **Créer les processus de test** : Suite de tests couvrant les aspects fonctionnels et qualitatifs du RAG : jeu de questions annoté (cas classiques et cas limites hors sujet / hors périmètre), tests Pytest des endpoints critiques (/health, /ask, /rebuild, erreurs 422), métriques Ragas automatisées (faithfulness, answer_relevancy) avec des scores de 0,72 à 1,00 sur les questions factuelles et une interprétation claire des scores bas hors périmètre.
- **Exposer les résultats aux directions via une API** : API FastAPI adaptée aux usages métier et bien documentée : endpoints cohérents (/ask, /ask_debug, /health…), exemples curl dans le README, validation stricte des entrées (Pydantic), protection optionnelle de /rebuild par clé API, choix techniques justifiés, système conteneurisé (Docker), réponses JSON prêtes à être consommées.
- **Identifier ou créer une API compatible et l'intégrer** : Intégration robuste de l'API OpenAgenda : pagination par curseur, gestion des erreurs avec backoff exponentiel et respect des limites, données nettoyées, dédupliquées et enrichies de métadonnées. Checkpointing des embeddings, sauvegarde de l'index avant reconstruction, routes opérationnelles (/rebuild, /recup_agenda).
- **Identifier ou créer un modèle adapté aux contraintes et aux besoins métier** : Choix de mistral-small-latest et mistral-embed cohérent avec le périmètre du PoC et justifié (rapport qualité / coût, fournisseur unique, simplicité). Deux prompts distincts (extraction de l'intention, génération) pour contrôler le comportement et éviter les hallucinations. Limites identifiées et pistes d'amélioration proposées.

### Points forts

- Chaîne RAG complète et fonctionnelle, de la collecte à la génération, avec une architecture claire et modulaire.
- Utilisation robuste d'une API externe (pagination, rate limiting, erreurs).
- Jeu de test annoté et métriques Ragas automatisées, avec une interprétation honnête des résultats.
- Documentation technique détaillée (choix d'architecture, limites, perspectives).
- Conteneurisation Docker permettant une exécution reproductible et une démonstration fluide.

### Axes d'amélioration

- Ajouter des métriques de performance (temps de réponse moyen, tokens consommés) pour anticiper coûts et latences en production.
- Fournir un fichier .env.template pour faciliter la prise en main.
- Versionner les slides de soutenance dans le dépôt.

### Remarques sur la soutenance

- PoC opérationnel avec une démonstration sur des cas d'usage réalistes (recommandations d'événements, gestion du hors sujet). Choix techniques justifiés par les besoins métier, rapport technique complet et honnête sur les limites, documentation et structure du dépôt facilitant la reprise. Démonstration des tests Ragas réalisée avec succès.
