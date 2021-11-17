En se servant de la commande expr, vérifier si la liste des emails enregistrés dans le fichier mails.txt. est valide ou non 

```mails.sh
#!/bin/bash
while read mail
do
        result=$(expr "$mail" : '^[a-zA-Z].*@[a-zA-Z].*\..*$')

        if [[ $result == 0 ]] ; then
                echo -e "$mail \tn'est un mail pas valide"
        else
                echo -e "$mail \tc'est un mail valide"
        fi
done < $1
```{{copy}}

`bash mails.sh mails.txt`{{execute}}