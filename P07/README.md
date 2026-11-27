# 🧠 P7 – Classification d'images en semi-supervisé : IRM cérébrales

Projet du parcours *Data Scientist Machine Learning* (OpenClassrooms).

Classification d'IRM cérébrales avec peu d'images annotées : extraction de caractéristiques par transfer learning (ResNet50), réduction de dimension (PCA), labels faibles obtenus par clustering (K-Means), puis entraînement semi-supervisé. Les limites des résultats sont analysées (test sur un petit échantillon).

**Stack :** Python · PyTorch / Keras · ResNet50 · scikit-learn (PCA, K-Means)

## 🔗 Liens

- 🖼️ [Présentation de soutenance (PDF)](projet7.pdf)

## 📝 Évaluation

**Validé le 7 juillet 2026**

### Notes de l'évaluateur

- **Identifier ou créer un modèle adapté** : Clustering OK : DBSCAN réellement lancé et comparé à K-Means, avec test des hyperparamètres. Le modèle entraîné est bien un CNN (ResNet, couches gelées) : bonne architecture. Comparaison supervisé / semi-supervisé faite sur seulement 20 images de test, trop peu pour conclure. Pas de courbe ROC, pas de « definition of done » chiffrée, hyperparamètres du CNN non testés.
- **Préparer et transformer les données** : Exploration soignée (tailles, modes, formats, déséquilibre bien repéré). Séparation labellisé / non labellisé tenue du début à la fin. Égalisation d'histogramme (CLAHE) ajoutée avec capture avant / après.

### Points forts

- Pipeline complet et lisible, notebooks bien titrés.
- Extraction ResNet50 propre et conforme.
- Bons réflexes : ARI sur les vrais labels, jeu de test tenu à l'écart, dropout et augmentation de données.
- A vu que rater un cancer (le rappel) est l'erreur qui compte.

### Axes d'amélioration

- Tester et noter les hyperparamètres du CNN.
- Jeu de test trop petit (20 images) : passer à de la validation croisée et ajouter une courbe ROC.
- Poser un objectif chiffré clair sur le rappel.

### Remarques sur la soutenance

- Bonne présentation.