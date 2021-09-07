1.  Lancez un container basé sur une image alpine:3.8, en mode
    interactif, et en lui donnant le nom c1

`docker run -ti --name c1 alpine:3.8`{{execute}}

1.  Lancez la commande curl google.com

`curl google.com`{{execute}}

> /bin/sh: curl: not found

1.  Qu'observez-vous ?

2.  Installez curl à l’aide du gestionnaire de package apk

`apk update && apk add curl{{execute}}`

1.  Quittez le container avec CTRL-P CTRL-Q (pour ne pas killer le processus de PID 1)

2.  Créez une image, nommée myping, à partir du container c1
    Utilisez pour cela la commande ***commit*** (docker commit --help pour
    voir le fonctionnement de cette commande)

`docker run -it myping:c1`{{execute}}

1.  Lancez un shell intéractif dans un container basée sur l’image
    *myping* et vérifiez que curl est présent

`docker run -it myping:c1`{{execute}}
