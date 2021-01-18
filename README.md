# API Platform Tutorial

Well hi there! This repository holds the code and script
for the [API Platform](https://symfonycasts.com/screencast/api-platform) course on SymfonyCasts.

## Setup

If you've just downloaded the code, congratulations!!

To get it working, follow these steps:

**Download Composer dependencies**

Make sure you have [Composer installed](https://getcomposer.org/download/)
and then run:

```
composer install
```

You may alternatively need to run `php composer.phar install`, depending
on how you installed Composer.

**Start the built-in web server**

You can use Nginx or Apache, but Symfony's local web server
works even better.

To install the Symfony local web server, follow
"Downloading the Symfony client" instructions found
here: https://symfony.com/download - you only need to do this
once on your system.

Then, to start the web server, open a terminal, move into the
project, and run:

```
symfony serve ou ici on voit ce que on fait
symfony serve -d pour travailler en arrier plan
```

(If this is your first time using this command, you may see an
error that you need to run `symfony server:ca:install` first).

Now check out the site at `https://localhost:8000`

Have fun!

## Have Ideas, Feedback or an Issue?

If you have suggestions or questions, please feel free to
open an issue on this repository or comment on the course
itself. We're watching both :).

## Thanks!

And as always, thanks so much for your support and letting
us do what we love!

<3 Your friends at SymfonyCasts

1. composer require api

2. https://127.0.0.1:8000/api

3. dans le .env on parametre la BDD
   DATABASE_URL="mysql://root:db_password@127.0.0.1:3306/cheese_whiz

4 composer require maker --dev

5
"config": {
"preferred-install": {
"\*": "dist"
},
"sort-packages": true
"platform": []
},

6 On le suprimer cette ligne du config de composer.json
"platform": []

7 php bin/console make:entity

8 On créer l'Entity CheeseListing

9 yes

10 et on créer le champs de notre table

11 On fait la migration avec le
composer require migrations
Parce que se une API

12 php bin/console doctrine:database:create

13 php bin/console make:migration

14 php bin/console doctrine:migrations:migrate

1555555
Dites bonjour à votre API!

Brillant! À ce stade, nous avons une entité Doctrine complètement traditionnelle à l' exception de celle-ci, l' @ApiResource()annotation. Mais cela change tout. Cela indique à API Platform que vous souhaitez exposer cette classe en tant qu'API.

Vérifiez-le: actualisez la /apipage. Woh! Tout à coup, cela signifie que nous avons cinq nouveaux points de terminaison, ou «opérations»! Une GETopération pour récupérer une collection de CheeseListings, une POSTopération pour en créer un nouveau, GETpour en récupérer un seul CheeseListing, DELETEpour ... vous savez ... supprimer et PUTmettre à jour un existant CheeseListing. C'est un CRUD complet basé sur l'API!

Et ce n'est pas que de la documentation: ces nouveaux terminaux fonctionnent déjà . Voyons-les ensuite, disons bonjour à quelque chose appelé JSON-LD et apprenons un peu comment cette magie fonctionne dans les coulisses.

16 php bin/console debug:router

17
