# Modèle de Classification d'Iris avec Arbre de Décision

Ce projet présente un modèle de classification d'espèces d'Iris en utilisant un Arbre de Décision, entraîné sur le célèbre ensemble de données Iris. Le modèle est ensuite exposé via une API FastAPI, ce qui vous permet de faire des prédictions sur de nouvelles données.

## Structure du Projet

1. app.py : Fichier principal contenant le code de l'API FastAPI.
2. model.pkl : Modèle d'Arbre de Décision pré-entraîné sauvegardé avec Pickle.
3. requirements.txt : Liste des dépendances Python requises.
4. ml.ipynb : Jupyter Notebook pour l'entraînement du modèle.
4. IRIS.csv : Ensemble de données Iris utilisé pour l'entraînement.

## Comment utiliser l'API

1. Clonez ce répertoire sur votre machine locale 

2. Installation des dépendances

    ```shell
        pip install -r requirements.txt

3. Entraînez le Modèle

Avant d'utiliser l'API, assurez-vous d'entraîner le modèle. Exécutez le notebook Jupyter ml.ipynb pour entraîner le modèle de classification. Cela générera un fichier model.pkl qui sera utilisé par l'API

4. Lancement de l'API Démarrez l'API FastAPI en exécutant le fichier app.py :

    ```shell
       uvicorn main:app --reload

5. Exemple de Requête API

 Vous pouvez désormais envoyer des requêtes POST à l'API avec les caractéristiques de l'Iris que vous souhaitez classifier, au format JSON. Par exemple :

Ouvrez Postman et créez une nouvelle requête POST.

Définissez l'URL de la requête à localhost:8000.

Dans l'onglet "Body", sélectionnez "raw" et choisissez "JSON (application/json)".

Utilisez le format JSON suivant pour envoyer les caractéristiques du véhicule à prédire :

    ```json

    {
    "sepal_length": 5.1,
    "sepal_width": 3.5,
    "petal_length": 1.4,
    "petal_width": 0.2
    }

Cliquez sur "Send" pour envoyer la requête, et vous recevrez une réponse JSON contenant  la prédiction de l'espèce d'Iris.

