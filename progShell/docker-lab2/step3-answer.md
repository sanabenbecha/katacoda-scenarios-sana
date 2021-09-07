Le but de cet exercice est de lancer des containers en mode interactif

1.  Lancez un container basé sur alpine en mode interactif sans lui spécifier de commande

`docker run -it alpine`{{execute}}

1.  Que s’est-il passé ?

1.  Quelle est la commande par défaut d’un container basé sur alpine

> sh

1.  Naviguez dans le système de fichiers

1.  Utilisez le gestionnaire de package d’alpine (apk) pour ajouter un package

`apk update`{{execute}}

`apk add curl`{{execute}}
