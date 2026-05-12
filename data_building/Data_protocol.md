## Protocole de construction de notre dataset

### 1. Identification des utilisateurs ciblés

Notre première étape d’échantillonnage consiste à récupérer une longue liste de comptes Reddit français. Nous explorons le subreddit r/france et collectons les noms de tous les comptes différents ayant publié quoi que ce soit sur celui-ci. Nous procédons à cette collecte à l’aide du notebook `users_scraping`. La liste des noms d’utilisateurs extraits est stockée dans `usernames.txt`.

Une fois que nous avons rassemblé 100 000 noms différents, nous exécutons le notebook `users_filter`. Il divise la liste d'utilsateurs en trois parties. En effet, Reddit cherchant à limiter le web scraping, nous souhaitons exploiter nos différentes adresses IP afin que chacun des trois membres du groupe récupère la date d’inscription d’un tiers des utilisateurs. À cette fin, nous créons trois fichiers `covid_users_X.txt` (avec $X \in {1,2,3}$), dans lesquels chacun stocke les noms d’utilisateurs inscrits entre le 17 mars 2020 et le 17 septembre 2020 (soit les six mois suivant le début du premier confinement en France métropolitaine), noms d'utilisateurs récupérés avec le même notebook.

Ensuite, nous utilisons le notebook `content_scraping`. Il récupère l'ensemble des commentaires produits par les utilisateurs stockés dans les fichiers `covid_users_X.txt` ainsi que les commentaires et les posts auxquels ils répondent. Il applique un filtre après la première requête de 50 messages à Reddit pour exclure les utilisateurs qui s'expriment 10% ou moins en français (soit 5 messages sur 50). Il produit les fichiers structurés `data_X.csv`. Le travail est de nouveau parallélisé à 3. 

Finalement, nous utilisons le dernier notebook de ce dossier, `final_merge`. Il concatène les trois fichiers `data_X.csv` et supprime les doublons. 
