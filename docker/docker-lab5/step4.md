Exemple 2 : Une application Web Python simple exécutée sur Docker Compose (3/5)

Étape 3: définir les services dans un fichier de composition 

Créez un fichier appelé docker-compose.yml dans le répertoire de votre projet et collez ce qui suit:


```docker-compose.yml
version: "3.9"
services:
  web:
    build: .
    ports:
      - "5000:5000"
  redis:
    image: "redis:alpine"
```{{copy}

Ce fichier Compose définit deux services: web et redis.