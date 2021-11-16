Le but de cet exemple est de définir d’un volume au lancement d’un container (2/3)

-   Lancez un container avec les caractéristiques suivantes:
		o	basé sur l’image alpine:3.8
		o	nommé c3
		o	exécution en background (option -d)
		o	définition de /data en tant que volume (option -v)
		o	spécification d’une commande qui écrit dans le volume ci-dessus


-   Inspectez le container et repérez notamment le chemin d’accès du volume sur la machine hôte.


-   Supprimez le container c3.