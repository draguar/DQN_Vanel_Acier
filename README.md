# Projet d'apprentissage profond par renforcement

Le code se trouve sous forme d'un notebook jupyter. Il est issu de [google colab](https://colab.research.google.com) et il est conseillé de l'y importer afin d'assurer un fonctionnement immédiat avec toutes les dépendances satisfaites.

Un rapport est également présent sous forme de fichier PDF, ainsi que différents GIFs montrant des exemples de parties après 10h d'entraînement sans prioritized experience replay, ou 5h avec.


Résultat du DQN avec 10h d'entrainement  
![](breakout_simple_10h_training.gif)

Résultats avec prioritized experiences replay et 5h d'entrainement  
![](breakout_prioritized_replay_5h_training.gif)
![](breakout_prioritized_replay_5h_training_2.gif)

## Quatres solutions pour tester notre code : 
    * Google Colab avec Google Drive
    * Google Colab sans Google Drive (non recommandé)
    * Jupyter Notebook (non recommandé)
    * Plain Python (non recommandé)

## Google Colab avec Google Drive
Pour pouvoir tester les modèles sur Google Colab il faut simplement connecter son Google drive au notebook grâce à la première cellule. 
Il faut ensuite créer un dossier "Reinforcement" dans son drive et y ajouter le/les modèle(s) que l'on souhaite charger.
Il faudra alors modifier dans les cellules les noms des modèles pré-écrit par exemple "XX.data" par le nom du modèle que l'on souhaite charger, les lignes concernées sont indiquées avec un commentaire "[LOAD MODEL]"

## Google Colab sans Google Drive
Dans ce cas il ne faut pas executer la première cellule et décommenter les cellules indiqué avec le commentaire "[NO GOOGLE DRIVE]" elle feront apparaitre un input HTML permettant d'uploader les modèles à la main

## Jupyter Notebook
Dans le cas ou Google Colab n'est pas utilisable il faudra installer toutes les dépendances à la main en utilisant la commande :

``` pip3 install -r requirements.txt ```  

puis démarrer un notebook jupyter dans le dossier où se trouve le fichier "TP_reinforcement.ipynb"

``` jupyter notebook ```

[Plain Python]
Pour l'utiliser il faut simplement lancer le fichier TP_reinforcement.py

``` python3 TP_Reinforcement.py ```

# Chargement des modèles

Les deux modèles utilisés pour le jeu breakout sont fournis dans le dossier "models/classic" pour la version classique du DQN et "models/prioritized" pour le modèle avec l'experience replay prioritized