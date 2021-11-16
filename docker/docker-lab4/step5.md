Le but de cet exemple est de définir d’un volume au lancement d’un container (2/3)

-   Lancez un container avec les caractéristiques suivantes:
		o	basé sur l’image alpine:3.8
		o	nommé c3
		o	exécution en background (option -d)
		o	définition de /data en tant que volume (option -v)
		o	spécification d’une commande qui écrit dans le volume ci-dessus

`docker run -d --name c3 -v /data alpine:3.8  sh  -c 'ping 8.8.8.8 >> /data/ping.txt'`{{execute}}

-   Inspectez le container et repérez notamment le chemin d’accès du volume sur la machine hôte.

`docker inspect c3`{{execute}}

-   Supprimez le container c3.

`docker rm c3`{{execute}}