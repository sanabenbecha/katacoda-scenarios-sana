Exemple 2 : Une application Web Python simple exécutée sur Docker Compose (1/5)

Présentation
L'application utilise le framework Flask et gère un compteur d'accès dans Redis. Bien que l'exemple utilise Python, les concepts présentés ici devraient être compréhensibles même si vous ne le connaissez pas.

Étape 1: Configuration 
Définissez les dépendances de l'application.

-	Créez un fichier appelé app.py dans le répertoire de votre projet et collez-le dans:
```app.py
import time
import redis
from flask import Flask

app = Flask(__name__)
cache = redis.Redis(host='redis', port=6379)

def get_hit_count():
    retries = 5
    while True:
        try:
            return cache.incr('hits')
        except redis.exceptions.ConnectionError as exc:
            if retries == 0:
                raise exc
            retries -= 1
            time.sleep(0.5)

@app.route('/')
def hello():
    count = get_hit_count()
    return 'Hello World! I have been seen {} times.\n'.format(count)
```{{copy}}

Dans cet exemple, redis est le nom d'hôte du conteneur redis sur le réseau de l'application. Nous utilisons le port par défaut pour Redis, 6379.

-	Créez un autre fichier appelé requirements.txt dans le répertoire de votre projet

```requirements.txt
Flask
redis
```{{copy}} 