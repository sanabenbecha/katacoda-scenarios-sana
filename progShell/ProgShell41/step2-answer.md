1.	À l’aide la commande sed, transformez ce fichier comme ceci :

	unix 
	<date>28-30 jan</date> 
	<date>17-19 juin</date> 
	<date>18-20 nov</date> 
	 
	shell 
	<date>23 mars</date> 
	<date>15 juil</date> 
	<date>7 sep</date>
	
`sed 's/^[0-9].*$/<date>&<\/date>/' dates_cours.txt `{{execute}}

ou

`sed 's/^\([0-9].*\)$/<date>\1<\/date>/' dates_cours.txt`{{execute}} 

2.	Remplacer le shell ‘bash’ du fichier passwd par le shell csh.

`cat passwd | sed 's/bash/csh/g'`{{execute}}

3.	remplacer le shell ‘bash’ du fichier passwd par le shell csh et enregistrer le résultat dans le fichier passwd_2 (ne pas utiliser la redirection).

`cat passwd | sed 's/bash/csh/w passwd_2'`{{execute}}

4.	remplacer le shell ‘bash’ du fichier passwd par le shell csh, de la 10eme ligne jusqu’au la fin du fichier.

`cat passwd | sed '10,$s/bash/csh/w passwd_2'`{{execute}}

5.	Remplacer toute l'occurrence du mot « unix » en « linux ».

`sed 's/unix/linux/g' linux.txt`{{execute}}

6.	Remplacer trois occurrences du mot « unix » en « linux ».

`sed 's/unix/linux/3g' linux.txt`{{execute}}

7.	Mettre en parenthèse le début de chaque mot.

`cat linux.txt | sed 's/^\(.\)/\(\1\)/g'`{{execute}}

8.	Mettre en parenthèse le début de chaque mot.

` cat linux.txt | sed 's/^\(.\)/\(\1\)/g'`{{execute}}