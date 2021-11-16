L'objectif de cette manipulation est l'exécution d'un conteneur avec Docker Compose

-   Tout d'abord, créez un répertoire pour notre fichier YAML:

-   Créez maintenant le fichier YAML docker-compose.yml 

-   Mettez le contenu suivant dans le fichier:

```docker-compose.yml
my-test:
  image: hello-world
```{{copy}}

-   Exécutez la commande suivante pour créer le conteneur:

`docker-compose up`{{execute}}

-   Afficher votre groupe de conteneurs pour le projet hello-world

`docker-compose ps`{{execute}}

-   Arrêter tous les conteneurs du projet hello-world

`docker-compose stop`{{execute}}