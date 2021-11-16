Commençons par revoir la création d’une image permettant d’empaqueter
l’utilitaire git dans une image basée sur la dernière version de Ubuntu

1. Créez un fichier docker-compose.yml  avec le contenu suivant :

```Dockerfile
my-test:
  image: hello-world

```{{copy}}

2. Exécutez la commande suivante pour créer le conteneur: 

`docker-compose up .`{{execute}}