Le but de cet exercice est de montrer comment lancer un processus dans
un container existant.

1.  Lancez un container en background, basé sur l’image alpine.
    Spécifiez la commande **ping 8.8.8.8** et le nom ping\_container
    avec l’option --name

`docker run -d --name ping_container alpine ping 8.8.8.8`{{execute}}

1.  Observez les logs du container en utilisant l’ID retourné par la
    commande précédente ou bien le nom du container

`docker logs ping_container`{{execute}}

Quittez la commande de logs avec CTRL-C

1.  Lancez un shell sh, en mode interactif, dans le container précédent

`docker exec -it ping_container sh`{{execute}}

1.  Listez les processus du container

`ps`{{execute}}

Qu'observez vous par rapport aux identifiants des processus ?
