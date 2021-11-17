Créez un script ajoutPersonne.sh qui permet la saisie du formulaire suivant :


>	Civilité d’une personne (M., Mme, Mlle)

>	Son nom

>	Son prénom

>	Sa date de naissance sous forme de jj/mm/aaaa

>	Sa situation familiale (Célibataire, Divorcé(e), Marié(e))

>	Nombre d’enfants à charge 

>	Sa nationalité

>	Sa profession


Ces informations sont ajoutées dans un fichier nommé Personnes. Elles sont séparées par des points-virgules. Chaque ligne contient les données d’une personne. La structure d’une ligne du fichier est la suivante :

civilité ; nom ; prénom ; date de naissance ; situation familiale ; nombre d’enfants ; nationalité ;profession


Le script effectue un tri sur le fichier avant d’en sauvegarder une copie dans le répertoire /tmp.

-	Pour éviter des erreurs de saisie d’une part et pour accélérer la saisie d’autre part, l’utilisateur se contente de taper la première lettre concernant sa situation familiale (C pour Célibataire, ...). Le script interprète la lettre par le motre correspondant dans la base.

-	Le script précédent présente un grand inconvénient quant à la redondance d’informations. Remédiez à ce problème en interrompant le script lorsque l’utilisateur saisi le nom et prénom d’une personne existante.

-	Dans une boucle while, demandez à l’utilisateur s’il voudrait ajouter une nouvelle personne en tapant « Y » et « N » pour arrêter.