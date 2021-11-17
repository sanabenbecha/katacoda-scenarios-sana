Écrivez un script qui prend en argument un nom de fichier. Le fichier en question contient un nombre entier par ligne. Le script contiendra :

-	Un **test** permettant de vérifier que le fichier existe bien, sinon afficher un message d'erreur et faire un retour erreur.

-	Une fonction **addition** qui calcule et affiche la somme des lignes du fichier

-	Une fonction **nlignes** nombre lignes qui compte et affiche le nombre de lignes dans le fichier

-	Une fonction **minmax** qui calcule et affiche le minimum et le maximum des valeurs du fichier.

Tous les messages à afficher doivent être sauvegardés à la fin du fichier d’entrée.

```operation.sh
#/bin/bash
echo "Script $0"
fichier=$1

#La fonction addition
addition () {
somme=0
while read ligne
do
	somme=$(($somme+$ligne))
done<$fichier
echo "Somme : $somme"
}

#La fonction nlignes
nlignes () {
nb=0
while read ligne
do
	nb=$(($nb+1))
done<$fichier
echo "Nombre lignes : $nb"
}
#La fonction minmax
minmax () {
read min < $fichier
max=$min
while read ligne
do
	if [ $ligne -lt $min ]
	then
		min=$ligne
	fi

	if [ $ligne -gt $max ]
	then	
		max=$ligne
	fi

done<$fichier

echo "La valeure minimale est : $min"
echo "La valeure maximale est : $max"
}
addition
nlignes
minmax
```{{copy}}

`bash operation.sh`{{execute}}