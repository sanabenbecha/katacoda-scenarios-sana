Exemple 2 : Une application Web Python simple exécutée sur Docker Compose (5/5)

Étape 5: Modifiez le fichier de composition pour ajouter un montage de liaison

Modifiez docker-compose.yml dans votre répertoire de projet pour ajouter un montage de liaison pour le web service:

```
version: "3.9"
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/code
    environment:
      FLASK_ENV: development
  redis:
    image: "redis:alpine"
```{{copy}

La nouvelle clé **volumes** monte le répertoire du projet (répertoire courant) sur l'hôte à l’intérieur du /code du conteneur, vous permettant de modifier le code à la volée, sans avoir à reconstruire l'image. 

La clé **environment** définit la variable d'environnement **FLASK_ENV**, qui indique **flask run** de s'exécuter en mode développement et de recharger le code en cas de modification. Ce mode ne doit être utilisé qu'en développement.