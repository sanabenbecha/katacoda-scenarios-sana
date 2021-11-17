Écrire un script audit.sh qui permet de :

-	Écrire une fonction users_connect qui affichera la liste des utilisateurs actuellement connectés.

-	Écrire une fonction disk_space qui affichera l’espace disque disponible.

-	Le programme principal affichera le menu suivant :


		- 0 - Fin 
		- 1 - Afficher la liste des utilisateurs connectes 
		- 2 - Afficher l’espace disque 

Votre choix :

Une copie des messages affichés devra être sauvegardée dans le fichier output.txt.

*Indice* : Commandes utiles : **df**, **who**.

 ```audit.sh
 
 #! /bin/bash  

function pause 
{ 
   echo "Tapez sur Return pour continuer" 
   read x 
} 
   
function users_connect 
 { 
    who 
 } 
   
function disk_space 
 { 
   df -k  
 } 
   
while true  
 do 
   clear 
   echo "- 0 - Fin" 
   echo "- 1 - Afficher la liste des utilisateurs connectes"  
   echo "- 2 - Afficher l’espace disque" 
   echo "Votre choix : \c" #
   read choix 
   
   case $choix in 
   
   0)    exit 0 
      ;; 
   1) 
     users_connect 
      ;; 
   2) 
      disk_space 
      ;; 
   
   *) echo "Choix incorrect" 
      ;; 
   esac 
   pause 
 done
```{{copy}}

`bash audit.sh`{{execute}}
