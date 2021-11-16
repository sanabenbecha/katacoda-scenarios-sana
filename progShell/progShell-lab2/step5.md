Le but de cet exercice est de montrer les différentes options pour
lister les containers du système

1.  Listez les containers en cours d’exécution

`docker ps`{{execute}}

1.  Est-ce que tous les containers que vous avez créés sont listés ?

Non il y a des conteneurs arrêtés

1.  Utilisez l’option -a pour voir également les containers qui ont été stoppés

`docker ps -a`{{execute}}

1.  Utilisez l’option -q pour ne lister que les IDs des containers (en cours d’exécution ou stoppés)

`docker ps -a -q`{{execute}}
