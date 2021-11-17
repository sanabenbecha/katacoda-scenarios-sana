E.	Test et comparaison

10.	Écrire un script exist.sh qui affiche “fichier présent” si l’argument de la commande correspond à un fichier qui existe.

```
#!/bin/bash
if [[ -e $1 ]]
then
echo fichier existe  
fi
```{{copy}}

12.	Écrire un script verifUser.sh qui permet de vérifier si un utilisateur (passé en paramètre) existe.

```
#!/bin/bash
user=$(cut -d: -f1 /etc/passwd| grep $1 | wc -l)
echo $user

if [[ $user !=  0  ]]
then
        echo "l'utilisateur $1 existe"
else
        echo "l'utilisateur $1 n'existe pas"
fi
```{{copy}}