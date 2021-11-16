Le but de cet exercice est l'inspection d’un container

1.  Lancez, en background, un nouveau container basé sur nginx:1.14 en
    exposant le port 80 du container.

`docker run -d --expose=80 nginx`{{execute}}

1.  Notez l'identifiant du container retourné par la commande précédente.

1.  Inspectez le container en utilisant son identifiant

`docker inspect c09d806264c4`{{execute}}

1.  En utilisant le format Go template, récupérez le nom et l’IP du
    container

`docker inspect --format '{{.NetworkSettings.IPAddress}}' c09d806264c4`{{execute}}

1.  Manipuler les Go template pour récupérer d'autres informations

1.  Pour plus de pratique, comment déterminer rapidement et
    succinctement l'identifiant de l'image et la date de création
    d'une image Alpine?

`docker inspect alpine:latest --format='{{.Id}} {{.Created}}'`{{execute}}
