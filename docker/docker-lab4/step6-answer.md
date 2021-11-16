Le but de cet exemple est d'utiliser des volumes via la CLI (3/3)

-   Créez un volume nommé html

> `docker volume create --name html`{{execute}}

-   Listez les volumes existants et vérifiez que le volume html est présent

> `docker volume ls`{{execute}}

-   Inspectez le volume créé

> `docker volume inspect html`{{execute}}

-   Lancer un container basé sur nginx et monter le volume html sur le point de montage /usr/share/nginx/html du container. En publiant également le port 80 du container sur le port 8080 de l'hôte.

> `docker run --name nginxServer1 -p 8080:80  -d   -v html:/usr/share/nginx/html nginx`{{execute}}

-   Affichez le contenu du volume html.

> `ls /var/lib/docker/volumes/html/_data/`{{execute}}