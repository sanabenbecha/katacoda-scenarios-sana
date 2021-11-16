Le but de cet exemple est de définir un volume dans un Dockerfile (1/3)

-   Créez un fichier *Dockerfile* contenant les instructions
    suivantes :

```dockerfile
FROM alpine:3.8

VOLUME ["/data"]

```{{copy}}

-   Créez ensuite une image, nommée **imgvol**, à partir de ce fichier.


-   Lancez maintenant un shell interactif dans un container, nommé c2, basé sur l’image  **imgvol**


-   créez le fichier /data/hello.txt dans le conteneur


-   Quittez le terminal interactif démarré


-   inspectez pour récupérer la clé Mounts afin d’avoir le chemin d’accès du volume sur la machine hôte.


-   Supprimez le conteneur créé


-   Vérifiez l’existence du fichier hello.txt