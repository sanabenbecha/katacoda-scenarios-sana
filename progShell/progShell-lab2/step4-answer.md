Le but de cet exercice est de créer des containers en foreground et en
background

1.  Lancez un container basé sur alpine en lui spécifiant la commande **ping 8.8.8.8**

`docker run alpine ping 8.8.8.8`{{execute}}

1.  Arrêter le container avec CTRL-C, le container est-il toujours en cours d’exécution ?

`docker ps`{{execute}}

- Non le conteneur est arrêté

Note: vous pouvez utiliser la commande **docker ps** que nous
détaillerons dans l'une des prochaines lectures), et qui permet de
lister les containers qui tournent sur la machine.

1.  Lancez un container en mode interactif en lui spécifiant la commande **ping 8.8.8.8**

`docker run -ti alpine ping 8.8.8.8`{{execute}}

1.  Arrêter le container avec CTRL-P CTRL-Q, le container est-il toujours en cours d’exécution ?

- Oui le conteneur est toujours fonctionnel

1.  Lancez un container en background, toujours en lui spécifiant la commande **ping 8.8.8.8**

`docker run -d alpine ping 8.8.8.8`{{execute}}

Le container est-il toujours en cours d’exécution ?
  
-   Oui le conteneur est toujours fonctionnel
