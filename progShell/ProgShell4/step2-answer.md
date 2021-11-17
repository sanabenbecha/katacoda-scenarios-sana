Utilisez le fichier chiffres.txt dans les manipulations suivantes.

1.	Afficher toutes les lignes qui contiennent le chiffre ‘1’ puis les chiffres ‘11 puis ‘111’

`cat chiffres.txt | egrep -E 1`{{execute}}

`cat chiffres.txt | egrep -E 11`{{execute}}

`cat chiffres.txt | egrep -E 111`{{execute}}

2.	Début et fin de la ligne

	^ : Correspond au début de la ligne

	$ : Correspond à la fin de la ligne

-	Afficher les lignes qui commencent par « 11 »

`cat chiffres.txt | egrep -E "^11"`{{execute}}

-
	Afficher les lignes qui se terminent par « zz »

`cat chiffres.txt | egrep -E "zz$"`{{execute}}

-	Afficher les lignes qui ne contiennent que la chaine « zz »

`cat chiffres.txt | egrep -E "^zz$"`{{execute}}

3.	Les quantificateurs (liée à lettre qui la précède directement)

-	Afficher les liges qui ne contiennent que le chiffre 1 ou les lignes vides

`cat chiffres.txt | egrep -E "^1?$"`{{execute}}


-	Afficher les liges qui ne contiennent que le chiffre 1 ou une série du chiffre 1 ou les lignes vides .

`cat chiffres.txt | egrep -E "^1*$"`{{execute}}

-	Afficher les liges qui ne contiennent que le chiffre 1 ou une série du chiffre 1 en utilisant deux sortes de quantificateurs.


`cat chiffres.txt | egrep -E '^1+$`{{execute}}

`cat chiffres.txt | egrep -E '^11*$`{{execute}}


-	Afficher les liges qui contiennent une série du chiffre 1 (au moins un) :

`cat chiffres.txt | egrep -E "^1*$"`{{execute}}

-	Afficher les lignes qui contiennent une série du chiffre 1 de taille compris entre [3 et 7]

`cat chiffres.txt | egrep -E '^1{3,7}$'`{{execute}}

-	Afficher les liges qui ne contiennent que le chiffre 1 ou une série du chiffre 1 en utilisant le quantificateur {}

`cat chiffres.txt | egrep -E '^1{1,}$'`{{execute}}

4.	Regroupement des caractères, pour regrouper des des caractères utilisez les ()

-	Afficher les lignes qui contiennent les chaines 11 ou zz

`cat chiffres.txt | egrep -E '(11|zz)'`{{execute}}

-	Afficher les lignes qui ne contiennent que les chaines 11 ou zz

`cat chiffres.txt | egrep -E '^(11|zz)$'`{{execute}}

5.	Une séquence des caractères à l’aide des []

-	Afficher toutes lignes qui commencent par 1 ou z

`cat chiffres.txt | egrep -E '^[1z]'`{{execute}}

-	Afficher toutes lignes qui ne contiennent que 1 ou z 

`cat chiffres.txt | egrep -E '^[1z]$'`{{execute}}

-	Afficher toutes lignes qui ne contiennent que 1 ou z au moins une fois

`cat chiffres.txt | egrep -E '^[1z]+'`{{execute}}

-	Afficher les lignes qui contiennent un ou plusieurs espaces

`cat chiffres.txt | egrep -E '[[:space:]]+'`{{execute}}

-	 Afficher la liste des lignes qui ne commencent pas par 1 ou z
	 
`cat chiffres.txt | egrep -E '^[^1z]'`{{execute}}