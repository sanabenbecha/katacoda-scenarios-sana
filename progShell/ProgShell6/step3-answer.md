10.	Afficher le nom et le tél des clients des lignes 1 et 4

`awk -F'|' 'NR == 1 || NR == 4 {print $1, "-" , $5}' adresse.txt`{{execute}}

11.	Afficher le nom et le tél des clients des lignes comprises entre ligne 1 et ligne 4

`awk -F'|' 'NR == 1 , NR == 4 {print $1, "-" , $5}' adresse.txt`{{execute}}