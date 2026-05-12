### Classification politique/apolitique

Ce dossier contient les fichiers utilisés pour le fine-tuning et l'inférence du modèle EuroBERT sur la tâche de classification des messages en politique/apolitique.

Il contient plusieurs sous-dossiers :
- A. `annotations_political` contient les notebooks utilisés pour annoter le dataset d'entraînement et de test du modèle, ainsi que le dataset lui-même ;
- B. `fine-tune-eurobert` contient le notebook utilisé pour l'entrainement ; 
- C. `inference-eurobert-political`contient le notebook utilisé pour l'inférence sur tous les messages ;
- D. `model_eurobert_political` contient les fichiers de configuration du modèle fine-tuné.

Ce dossier permet d'obtenir le dataset `flat_political_interactions.csv` dans le dossier `clean_data`.

N.B. Il n'est pas possible d'exécuter les fichiers d'entraînement et d'inférence sans GPU en un temps acceptable.