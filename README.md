TP : Apprentissage Non Supervisé (Clustering)
Objectif du ce travail
Dans ce travail, nous allons :
Comprendre un dataset
Prétraiter les données
Appliquer plusieurs algorithmes de clustering
Réduire les dimensions avec PCA et t-SNE
Comparer les performances des modèles
Visualiser les clusters
Analyser les résultats
 Conclusion
Analyse finale
Dans ce Travail :
plusieurs méthodes de clustering ont été appliquées ;
les données ont été prétraitées et standardisées ;
les performances ont été évaluées avec plusieurs métriques ;
PCA, t-SNE et UMAP ont permis de visualiser les clusters ;
DBSCAN et HDBSCAN ont montré une bonne robustesse au bruit ;
KMeans donne généralement de bonnes performances sur le dataset Iris.


Q1. Pourquoi certains algorithmes fonctionnent-ils mieux ?
    → K-Means et GMM supposent des clusters convexes et bien séparés, ce
      qui correspond à la structure du dataset Breast Cancer (deux groupes
      relativement distincts). Les algorithmes basés sur la densité
      (DBSCAN) sont moins bien adaptés ici car les clusters ne sont pas
      définis par des régions denses séparées par du vide.

Q2. Quel modèle est le plus robuste au bruit ?
    → Agglomerative Clustering (Ward) est le plus stable car il ne
      nécessite pas de centres de masse (moins sensible aux valeurs
      extrêmes) et l'approche hiérarchique absorbe mieux les perturbations
      locales.

Q3. DBSCAN détecte-t-il mieux les outliers ?
    → Oui. DBSCAN est le seul algorithme ici à identifier explicitement
      les points de bruit (label=-1). L'Isolation Forest est plus
      performant pour la détection d'anomalies pure, mais DBSCAN détecte
      simultanément les clusters ET les outliers.

Q4. Le scaling influence-t-il les résultats ?
...
      worst area, mean perimeter. Ces features morphologiques décrivent
      la taille et la forme des noyaux cellulaires — corrélées au caractère
      malin vs. bénin de la tumeur.
