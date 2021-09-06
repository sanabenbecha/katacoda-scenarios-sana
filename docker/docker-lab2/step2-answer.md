Le but de cet exercice est de manipuler des commandes récurrentes

Exécutez les commandes suivantes
`docker run -it --name=test1 alpine:latest date
docker run -it --name=test1 alpine:latest date`

1.  Pourquoi ça ne marche pas?

> Le problème est que le même nom de conteneur a été utilisé pour les deux
exécutions et que le premier conteneur n'a pas été supprimé.

1.  Que pouvez-vous faire pour les faire fonctionner tous les deux (il y
    > a au moins deux façons)?

Vous pouvez supprimer le conteneur (en utilisant --rm) avec la première
commande d'exécution ou vous pourrez peut-être utiliser un nom unique
pour la deuxième exécution.

`docker run -it --name=test1 --rm alpine:latest date`{{execute}}
`docker run -it --name=test1 alpine:latest date`{{execute}}

Vous pouvez supprimer manuellement le premier conteneur après l'avoir
exécuté.

`docker run -it --name=test1 alpine:latest date`{{execute}}

`docker rm test1`{{execute}}

`docker run -it --name=test1 alpine:latest date`{{execute}}

Changez le nom du conteneur.

`docker run -it --name=test1 alpine:latest date`{{execute}}

`docker run -it --name=test2 alpine:latest date`{{execute}}
