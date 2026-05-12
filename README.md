# Reddit-Polarization
Ce repo contient tous les codes utilisés pour produire notre analyse sur la polarisation parmi les utilisateurs français de Reddit. 

La plupart des fichiers de données utilisés sont trop volumineux pour être ajoutés sur Git. Ils sont donc récupérables sur Dropbox, sur ce [lien](https://www.dropbox.com/scl/fo/7oj8snoagj4my7oq1y5z3/AMcv6AY2zkoJPAd0vIEHBWg?rlkey=grbbl96123z8bt1njtgdrm6zj&st=livskc64&dl=0) (si le lien de partage dropbox expire, merci de nous reconta). Il sera précisé à chaque étape quels fichiers sont nécessaires à l'exécution du code, et lesquels sont produits. Tous ces fichiers doivent être ajoutés dans un dossier `clean_data`, actuellement inexistant. 

Ce README liste les grandes étapes de réplication, en orientant vers des dossiers contenus dans ce repo. Chaque dossier contient ses propres instructions (fichiers "protocol"), excepté le dossier `description`. Les étapes que nous avons réalisées sont les suivantes :

1. Récupération des données Reddit &rarr; `data_building`
2. Statistiques descriptives &rarr; `description`
3. A. Annotations pour NLP 
3. B. Inférence des modèles de NLP &rarr; `NLP_inference`
4. Estimation des modèles économétriques &rarr; `econometrics`. 





