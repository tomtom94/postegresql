# Installer Postegresql sur Mac

```
brew update
```

```
brew install postgresql && brew install --cask pgadmin4
```

```
brew services start postgresql
```

```
psql postgres
```

```
CREATE ROLE root WITH LOGIN PASSWORD 'password';
ALTER ROLE root CREATEDB;
```

Ouvrir PgAdmin4 qui est une application comme une autre dans le Dock Mac.

Puis ajouter une nouveau serveur, clique droit sur Server, puis Create server.

Donner un `name` à son serveur, puis dans les paramètres de connexion il faut mettre `localhost` dans le `host` et le `login`/`password` sont `root` et `password`.
