1.	Faire afficher les noms des fichiers texte du répertoire /etc.

Commandes filtres utiles : awk, grep , sed. file.

`file /etc/* | grep text | awk '{print $1}' | sed 's/:$//'`{{execute}}

2.	Dans votre répertoire courant, afficher les caractéristiques des fichiers dont le nom commence par un point (uniquement ceux-là).

`ls -la | awk '$9 ~ /^\./ {print}'`{{execute}}

3.	Afficher les champs numéro 1 et 8 de la commande ps –aef

`ls -la | awk '$9 ~ /^\.[^.]/ {print}'`{{execute}}

4.	Formater l’affichage du résultat selon le modèle suivant :

		Utilisateur : {user}  CMD : {cmd}

`ps -ef | awk '{print "Utilisateur : " $1 " \t CMD: " $8}'`{{execute}}

5.	Le fichier adresse.txt contient les informations suivantes dans chaque ligne

Client|Adresse|CodePostal|Ville|Tel

`awk -F'|' '{print "Le uméro de ligne : " NR "\t Client: " $1}' adresse.txt`{{execute}}

6.	Affichage du numéro de ligne et du nom du client du fichier adresse.txt

`awk -F'|' '{print "Le uméro de ligne : " NR "\t Client: " $1}' adresse.txt`{{execute}}


7.	Afficher les lignes du fichier adresse.txt contenant au moins un "/"

`awk -F'|' '/[/]/ {print $0}' adresse.txt`{{execute}}

8.	Afficher les clients localisés dans le Morbihan (code postal commence par 56)

`awk -F'|' '$3 ~ /^56/ {print }' adresse.txt`{{execute}}

9.	 Afficher les clients qui ne sont pas localisés dans le Morbihan

`awk -F'|' '$3 !~ /^56/ {print }' adresse.txt`{{execute}}