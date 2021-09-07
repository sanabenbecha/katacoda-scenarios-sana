Le but de ce premier exercice est de lancer des containers basés sur
l'image alpine

1.  Lancez un container basé sur **alpine** en lui fournissant la commande **echo hello**

`docker container run alpine echo hello`{{execute}}

2.  Quelles sont les étapes effectuées par le docker daemon ?

> 1. Télécharger l'image alpine à partir de Docker Hub
> 2. Créer le conteneur à partir de l'image alpine
> 3. Executer la commande echo Hello
> 4. Arrêter le conteneur

3.  Lancez un container basé sur alpine sans lui spécifier de commande. Qu’observez-vous ?

`docker run alpine`{{execute}}
