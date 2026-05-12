### Classification gauche-droite

Ce dossier contient les scripts utilisés pour classifier les messages politique en gauche et droite. 

Puisque nous avons utilisé deux modèles différents selon la langue des messages, ce dossier est séparé en deux. Il contient donc les sous-dossiers :
- A. `annotations_left-right` contient les notebooks utilisés pour annoter le dataset d'entraînement et de test du modèle, ainsi que le dataset lui-même ;
- B. `sep_english_french` est le notebook qui permet de séparer les messages (`flat_all_interactions`) entre anglais et français. 
- C. `english` contient les notebooks pour tester le [modèle](https://huggingface.co/matous-volf/political-leaning-deberta-large) DeBERTa fine-tuné pour la classification politique ainsi que le notebook pour l'inférence. 
- D. `french`contient les notebooks pour entraîner la tête de classification XGBoostClassifier sur les embeddings d'un [SentenceBERT](https://huggingface.co/sentence-transformers/paraphrase-multilingual-mpnet-base-v2), ainsi que le notebook pour l'inférence.

Enfin, le notebook `merge_english_french` à la racine de ce dossier permet de fusionner les deux datasets (français en anglais) après classification. Il permet d'obtenir le dataset `clean_data/flat_left_right_interactions.csv`.

N.B. Il n'est pas possible d'exécuter les fichiers d'entraînement et d'inférence sans GPU en un temps acceptable.