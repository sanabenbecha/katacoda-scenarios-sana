Le but de cet Exemple est de définir un volume dans un Dockerfile

1.  Créez un fichier *Dockerfile* contenant les instructions
    suivantes :

```dockerfile
FROM alpine:3.8

VOLUME ["/data"]

```{{copy}}

-   Créez ensuite une image, nommée **imgvol**, à partir de ce fichier.

`docker build -t imgvol .`{{execute}}

-   Lancez maintenant un shell interactif dans un container, nommé c2, basé sur l’image  **imgvol**

`docker run -it --name c2 imgvol`{{execute}}

-   créez le fichier /data/hello.txt dans le conteneur

`echo "Ceci un fichier hello" > /data/hello.txt`{{execute}}

-   Quittez le terminal interactif démarré

`exit`{{execute}}

-   inspectez pour récupérer la clé Mounts afin d’avoir le chemin d’accès du volume sur la machine hôte.

`docker inspect c2`{{execute}}

-   Supprimez le conteneur créé

`docker rm –f c2`{{execute}}

-   Vérifiez l’existence du fichier hello.txt

`ls /data/ `{{execute}}