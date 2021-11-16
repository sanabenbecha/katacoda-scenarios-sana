Exemple 2 : Une application Web Python simple exécutée sur Docker Compose (2/5)

Étape 2: Créez un Dockerfile 

Dans cette étape, vous écrivez un Dockerfile qui crée une image Docker. L'image contient toutes les dépendances requises par l'application Python, y compris Python lui-même.

Dans le répertoire de votre projet, créez un fichier nommé Dockerfile et collez ce qui suit:

```Dockerfile
FROM python:3.7-alpine
WORKDIR /code
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
EXPOSE 5000
COPY . .
CMD ["flask", "run"]
```{{copy}} 

Cela indique à Docker de:
-	Créez une image en commençant par l'image Python 3.7.

-	Définissez le répertoire de travail sur /code.

-	Définissez les variables d'environnement utilisées par la flaskcommande.

-	Installez gcc et d'autres dépendances

-	Copiez requirements.txtet installez les dépendances Python.

-	Ajoutez des métadonnées à l'image pour décrire que le conteneur écoute sur le port 5000

-	Copiez le répertoire actuel .du projet dans le répertoire .de travail de l'image.

-	Définissez la commande par défaut du conteneur sur flask run.
