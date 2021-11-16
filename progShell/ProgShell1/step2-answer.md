B.	Gérer une liste des commandes (séparateurs, tubes, redirection, regroupement)

11.	Comment écrire les deux commandes suivantes sur la même ligne ?

$ cd /tmp 
$ ls -l 

`cd /tmp ; ls -l `{{execute}}

12.	Dans une seule commande en utilisant "echo", afficher un message sous le format suivant :

Les commandes dans le shell sont:
                                 Commandes internes
                                 Commandes externes
								 
`$ echo -e "Les commandes dans le shell sont : \vCommandes ineternes\n\t\t\t\t   Commandes externes"`{{execute}}

13.	Soit la commande who -A, qui génère un message d’erreur :

`$ who -A`{{execute}} 


-	Relancer cette commande et rediriger les erreurs dans un fichier.

`$ who -A 2> erreurs`{{execute}}

-	Relancer cette commande et faire disparaître les erreurs, sans les rediriger dans un fichier.

`$ who -A 2> /dev/null`{{execute}}

14.	Soit les commandes suivantes

echo "f1:f2:f3:f4" | cut -d: -f1,3 /etc/passwd
echo "f1:f2:f3:f4" | cut -d: -f1,3
cut -d: -f1,3

-	Exécuter les commandes et évaluer le résultat.
-	Dans quel cas l’utilisation de tube est inutile ?

15.	Soit la commande suivante : 
cat /etc/passwd | file
	i.	Expliquer pourquoi la commande retournera des erreurs d’exécution

> La commande file exige le nom du fichier (ne lit pas par défaut de l’entrée standard)

16.	Soit les deux commandes suivantes

	-	La commande "ps -aef " permet de listes tous les processus en cours d’exécution

	-	La commande "grep motif" permet de chercher le motif dans flux textuel (entrée standard, fichier, résultat d’une autre commande)

ii.	En se servant de ces commandes proposer une commande permettant de stocker la liste de tous les processus en cours d’exécution dans un fichierpros.txt et affiche sur l’écran avec le nom "bash"

`ps –aef | grep bash > fichierpros.txt`{{execute}}

iii.	Modifier la commande précédente pour rediriger les erreurs d’exécution dans le fichier erreur

`ps –aef | grep bash > fichierpros.txt 2> erreurs.txt`{{execute}}