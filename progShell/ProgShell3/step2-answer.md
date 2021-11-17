B.	Substitution de commande


5.	En une seule commande, afficher la date courante sous le format suivant:

Nous sommes le jeu. avril 9 02:03:55 CEST 2020 2.

` echo Nous sommes le $(date)`{{execute}}

Même chose que ci-dessus, mais formater la date comme ceci :

Nous sommes le 09/04/2020 

` echo Nous sommes le `date``{{execute}}

6.	En une seule commande, extraire le nom du dernier utilisateur créé, affecter le à la variable user (utiliser les commandes tail et cut).

`user=$(tail -1 /etc/passwd | cut -d: -f1)

7.	En une seule commande, déterminer le nombre d’utilisateurs créés dans la variable nbUser. (Utiliser la commande wc -l).

`nbUser=`wc -l /etc/passwd``{{execute}}