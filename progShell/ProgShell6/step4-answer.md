Effectuer les opérations suivantes avec l'éditeur vi (mode ex) sur le fichier expr.txt :

`vi expr.txt`{{execute}}

- Les numéros de téléphone qui se terminent par 48 doivent désormais se terminer par 50

`:1,$s/48$/50/`{{execute}}

-	Remplacer sur la ligne 2 la chaîne "annie2" par "annie" (sans se déplacer sur la ligne 2).

`:2s/annie2/annie/`{{execute}}

-	Remplacer les lignes vides par "VIDE".

`:1,$s/ˆ$/VIDE/`{{execute}}

-	Remplacer tous les prénoms qui commencent et finissent par la lettre X par XxxxxxxX.

`:1,$s/X[ˆ]*X/XxxxxxxX/`{{execute}}

-	Remplacer chaque chiffre de fin de ligne par 0, sauf si ce chiffre est égal à 8.

`:1,$s/[0-79]$/0/`{{execute}}

-	Remplacer dans les numéros de téléphone les "/" par des "."

:1,$s/\(..\)\/\(..\)\/\(..\)\/\(..\)$/\1.\2.\3.\4/`{{execute}}

-	Insérer un caractère "|" en début et fin de chaque ligne.

`:1,$s/ˆ\(.*\)$/|\1|/`{{execute}}