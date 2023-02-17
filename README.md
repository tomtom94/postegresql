# Postgresql config

## Installer sur Docker

```
docker run --name postgresql -e POSTGRES_USER=myusername -e POSTGRES_PASSWORD=mypassword -p 5432:5432 -v postgres:/var/lib/postgresql/data -d postgres
```

## Installer Postgresql sur Mac

Voici les lignes de commande.

```
brew update
```

On installe la base de donnée

```
brew install postgresql
```

On installe le visuel qui permet de lire visuellement la base de donnée

```
brew install --cask pgadmin4
```

```
brew services start postgresql
```

On entre dans la base de donnée en ligne de commande, afin de créer le user root par défaut

```
psql postgres
```

```
CREATE ROLE myusername WITH LOGIN PASSWORD 'mypassword';
ALTER ROLE myusername CREATEDB;
```

Ouvrir PgAdmin4 qui est une application comme une autre dans le Dock Mac.

Puis ajouter une nouveau serveur, clique droit sur Server, puis Create server.

Donner un `name` à son serveur, puis dans les paramètres de connexion il faut mettre `localhost` dans le `host` et le `login`/`password` sont `root` et `password`.

On peut maintenant surfer dans le serveur postegresql.

## Tester la connexion avec Node.js

```
npm install
```

Puis lancer le fichier racine

```
node index.js
```