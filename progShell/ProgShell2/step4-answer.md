D.	Variables, affichages et lectures clavier

9.	Écrire un script affich.sh et réaliser les opérations suivantes :

-	Initialiser une variable prenom (récupérée de la variable substitutionnel numéro 1).

-	Initialiser une variable maDate qui contiendra la date courante.


En se servant de ces deux variables afficher message sous le format :

{prénom} nous somme le {date courante}

```affich.sh
#!/bin/bash
prenom=$1
maDate=`date`
echo "$prenom nous somme le $maDate"
```{{copy}}