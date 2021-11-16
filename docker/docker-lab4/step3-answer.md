
Exemple 3 : Depuis le docker hub, cherchez une image correspondante à la version 7.9 du sonarqube et créez un conteneur pour mapper les ports nécessaires.
	
> `docker run    --publish 9000:9000  --name sonar3 sonarqube`{{execute}}