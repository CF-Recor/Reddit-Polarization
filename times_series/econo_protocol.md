# Econometrics

Ce dossier contient tous les scripts nécessaires pour passer des fichiers classifiés par les modèles NLP au résultat économétrique. 

Pour le répliquer, utiliser :
1. `merge_labels`: Prend les fichiers classifiés `flat_political`, `flat_toxic`, `flat_left_right` ainsi que le fichier structuré `struct_all_interactions`. Les fusionne pour produire le fichier `struct_classified_interactions`.
1. (Bis) `choose_scale`: Prend le fichier `struct_classified_interactions` pour étudier le nombre restant d'individus et de messages selon le choix d'aggrégation en panel.
2. `build_metrics`: Prend le fichier `struct_classified_interactions` et le transforme en panel, en créant les métriques utilisées ensuite, pour produire le fichier `full_panel_interactions`.
3. `PanelOLS`: prend le panel `full_panel_interactions` et estime quatre régression de panel avec effets fixes.
4. `PanelVAR`: prend le panel `full_panel_interactions` et estime la  les coefficients d'un PVAR(2) ainsi que les IRFs correspondantes.  