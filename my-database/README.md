# Cas pratique (My database)

## Introduction & Installation

Ce package est une application Laravel 9 (LTS).

L'installation se fait de la manière suivante :

```bash
cd my-app/
cp .env.example .env
php artisan key:generate
composer i
```

Modifier le fichier .env pour définir les constantes propres à la base de données. Il est libre de choisir entre MySQL, PgSQL ou SQLite.
Migrer ensuite la base de données avec :
```bash
php artisan migrate --seed
```

Le seeder créera une liste de 30 projets.

## Enoncé
1) Créer une méthode dans un controlleur qui récuperera les projets attachés à un user_id specifique.
La requête pour récupérer les projets proviendra de l'application "my-app".

2) Ce package ne doit pas être requêté depuis une autre application que "my-app". Il faut donc ajouter un système pour sécuriser l'accès à cette application.
3) Créer un simple README en Anglais pour expliquer comment lancer cette application.