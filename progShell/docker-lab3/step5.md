1.  Créer un répertoire local nommé WebApp

2.  Télécharger les deux fichiers index.html et linux.png dans le
    répertoire déjà créé depuis le repository github suivant :
    **https://github.com/medsalahmeddeb/docker**

3.  Créer un fichier Dockerfile dans le même répertoire qui permet
    d’automatiser les tâches suivantes en se basant sur la dernière
    image stable de Nginx :

-   Copier les deux fichiers index.html et linux.png dans le répertoire
    : **/usr/share/nginx/html**

-   Exposer les deux ports 80 et 443

-   Lancer la commande suivante **["nginx", "-g", "daemon off;"]**
    automatiquement avec le démarrage d’un conteneur en se basent sur
    l’image en question.

```dockerfile
FROM nginx:1.14

COPY linux.png index.html /usr/share/nginx/html/

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]

```{{copy}}

`docker build -t webapp .`{{execute}}

1.  Tester l’accès à la page index.html en utilisant l’adresse IP du conteneur

`docker inspect CONTAINER-ID`{{copy}}

Depuis un navigateur, lancez : http://CONTAINER-IP/
