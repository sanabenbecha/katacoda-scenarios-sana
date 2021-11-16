
Exemple 2 : Créez un conteneur basé sur l’image jenkins:2.60.3 en mappant les port 8080 et 50000.
	
> `docker run --name serveurCI-CD --publish 8080:8080 --publish 50000:50000 jenkins:2.60.3`{{execute}}