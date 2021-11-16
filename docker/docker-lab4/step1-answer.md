
1. Exemple 1 : Créez un conteneur en se basant sur la description suivante : :

	•	Image : nodejscn/node
	•	Port à publier :
		o	Sur le host : 8080
		o	Dans le conteneur : 80
	•	Nom du conteneur : testAppNode
	
> `docker run --name serveurCI-CD --publish 8080:8080 --publish 50000:50000 jenkins:2.60.3`{{execute}}