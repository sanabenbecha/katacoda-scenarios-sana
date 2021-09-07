Le but de cet exercice est de vérifier les différences entre ENTRYPOINT
et CMD.

1.  Créez un fichier *Dockerfile-v1* contenant les instructions
    suivantes :

```dockerfile
FROM alpine

ENTRYPOINT ["ping"]
```{{copy}}

-   Créez ensuite une image, nommée **ping:1.0**, à partir de ce fichier.

`docker build -t ping:1.0 -f Dockerfile-v1 .`{{execute}}

-   Lancez maintenant un container basé sur l’image **ping:1.0**

`docker run ping:1.0`{{execute}}

-   Observez le résultat

-   Lancez un nouveau container en lui donnant l’adresse IP d’un DNS
    Google (8.8.8.8), en ajoutant également l’option -c 3 pour limiter
    le nombre de ping envoyés.

`docker run ping:1.0 8.8.8.8 -c3`{{execute}}

-   Observez de nouveau le résultat

2.  Créez un fichier *Dockerfile-v2* contenant les instructions suivantes :

```dockerfile

FROM alpine

CMD ["ping"]
```{{copy}}

-   Créez une image, nommée **ping:2.0**, à partir de ce fichier.

`docker build -t ping:2.0 -f Dockerfile-v2 .`{{execute}}

-   Lancez maintenant un container basé sur l’image **ping:2.0**

`docker run ping:2.0`{{execute}}

-   Observez le résultat

-   Lancez un nouveau container en lui donnant l’adresse IP d’un DNS
    Google (8.8.8.8), en ajoutant également l’option -c 3 pour limiter
    le nombre de ping envoyés.

`docker run ping:2.0 8.8.8.8 -c3`{{execute}}

-   Observez de nouveau le résultat

3.  Créez un fichier *Dockerfile-v3* contenant les instructions
    suivantes :

```dockerfile

FROM alpine

ENTRYPOINT ["ping"]

CMD ["-c3", "localhost"]

```{{copy}}

-   Créez une image, nommée **ping:3.0**, à partir de ce fichier.

`docker build -t ping:3.0 -f Dockerfile-v3 .`{{execute}}

-   Lancez maintenant un container basé sur l’image **ping:3.0**

`docker run ping:3.0`{{execute}}

`docker run ping:3.0 8.8.8.8`{{execute}}

-   Observez le résultat
