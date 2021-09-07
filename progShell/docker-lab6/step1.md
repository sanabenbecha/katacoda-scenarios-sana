Commençons par revoir la création d’une image permettant d’empaqueter
l’utilitaire git dans une image basée sur la dernière version de Ubuntu

1. Créez un fichier Dockerfile avec le contenu suivant :

```Dockerfile
FROM ubuntu:latest

MAINTAINER "devops@gk.fr"

RUN apt-get update && apt-get install -y git

ENTRYPOINT ["git"]
```{{copy}}

1. Créer l’image correspondant au Dockerfile avec le tag **ubuntu-git-latest**

`docker build -t ubuntu-git-latest .`{{execute}}
