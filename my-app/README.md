# Cas pratique (My App)

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

Le seeder créera un utilisateur avec les identifiants suivants : 
* Email : email@email.com
* Mot de passe : helloworld

## Enoncé
1) Intégrer [Laravel Sanctum](https://laravel.com/docs/9.x/sanctum) pour permettre une connexion via API.
2) Créer 2 routes REST:
    * Une pour identifier l'utilisateur.
    * Une pour récupérer une liste de projets (par exemple GET /api/projects)

La route pour récupérer les projets appelera une méthode dans un controlleur.
La méthode devra appeler la deuxième application Laravel nommée "my-database" en spécifiant l'ID de l'utilisateur actuellement connecté.


L'idée est donc d'avoir quelque chose comme :

Postman --> GET /api/projects (my-app) <--> my-database (qui lira une table "projects").

L'idée est de simuler un appel entre 2 micro-services.
Il est libre de choisir le moyen de communication entre les 2 micro-services (REST, GraphQL, GRPC, Websocket).


3) Créer une collection Postman pour simuler
4) Créer un simple README en Anglais pour expliquer comment lancer cette application.