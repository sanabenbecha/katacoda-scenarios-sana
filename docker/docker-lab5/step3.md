Le but de ce premier exercice est de Dockerizer un serveur web simple de
type nginx dans un conteneur basique.

1.  Développez (en se basant sur le code suivant) un serveur HTTP qui
    expose le endpoint /ping sur le port 80 et répond par PONG.

**Fichier 1 : pong.js**

```javascript
  var express = require('express');

  var app = express();

  app.get('/ping', function(req, res) {

    console.log("received");

    res.setHeader('Content-Type', 'text/plain');

    res.end("PONG");

  });

  app.listen(80);

```{{copy}}

**Fichier 1 : package.json**

```json
{

  "name": "pong",

  "version": "0.0.1",

  "main": "pong.js",

  "scripts": {

    "start": "node pong.js"

  },

  "dependencies": { "express": "\^4.14.0" }

}
```{{copy}}

2.  Créez le fichier Dockerfile qui servira à construire l'image
    de l'application. Ce fichier devra décrire les actions suivantes

-   image de base: alpine:3.10

-   installation du runtime du langage choisi

-   installation des dépendances de l’application

-   copie du code applicatif

-   exposition du port d’écoute de l’application

-   spécification de la commande à exécuter pour lancer le serveur

```dockerfile

FROM alpine:3.10

#MAJ des packages et install nodeJS

RUN apk update && apk add nodejs-npm

#Spécifier le répertoire courant de notre conteur

WORKDIR /app

#Copier les fichiers sources dans le dossier courant (/app)

COPY . .

# installer le Framework node JS en

RUN npm install

# Expsoer le port 80 du serveur web HTTP

EXPOSE 80

#Démarrer le Framework nodeJS

CMD ["npm","start"]

```{{copy}}

1.  Construire l’image en la taguant pong:v1.0

`docker build -t pong:v1.0 .`{{execute}}

1.  Lancez un container basé sur cette image en exposant le port 80 du
    conteneur

`docker run -d pong:v1.0`{{execute}}

1.  Inspecter le conteneur créé afin de déterminé l’IP privé alloué puis
    tester l'application

`docker inspect CONTAINER-ID`{{copy}}

`curl CONTAINER-IP/ping`{{copy}}
