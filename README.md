# Vos loisirs en Live

Cette application est le résultat d'une démarche de co-construction d'une application avec des utilisateurs...

## Informations générales 

L'application "Vos loisirs en live" suit le modèle
client-serveur classique. Elle est constituée de
deux entités distinctes : une API Rest JSON et un
front SPA.

L'API Rest sert d'agrégateur de contenu et formate
plusieurs flux JSON utilisés dans le front. Elle est
implémentée en PHP 7 et basée sur Slim
Framework 3.

Le front SPA permet l'affichage des flux. Il est
implémenté grâce au framework Ionic 3 qui repose
lui même sur le framework Angular 5.

L'ensemble du code source est disponible sous
licence GNU GPL v3 aux deux adresses suivantes :
https://github.com/Lab-numerique-LIVE/live-loisirs
https://github.com/Lab-numerique-LIVE/live-loisirs-api

⚠ La branche par défaut est celle de développement ​ **`develop​`**.

Les différents version livrées sont taguées et également disponibles sur la branche **`master​`**.

## Déploiement de l'application

### API

L'APi étant une application PHP 7 classique le
déploiement peut facilement se faire grâce à
Apache ou Nginx. 

https://ionicframework.com/docs/intro/installation/

Ci dessous les différents prérequis serveur :
https://www.slimframework.com/docs/v3/start/web-servers.html

Quelques détails concernant Apache :
https://www.slimframework.com/docs/v3/deployment/deployment.html

### Front

Le front quant à lui est développé en Typescript et
doit donc être préalablement transpilé vers
Javascript avant d'être déployé.

La chaîne de compilation nécessite les
dépendances suivantes :

+ NodeJS (version LTS)
+ NPM (>= 3.10) 
+ Ionic (>= 3)


NodeJS et NPM sont disponibles sous la forme d'un package à l'adresse suivante :
https://nodejs.org/en/

Il faut ensuite installer Ionic afin de pouvoir lancer
le build.
```sh
$ npm install -g ionic
```

On installera par la suite les dépendances nécessaires au build de l'applications.

⚠ A partir de cette étape toutes les commandes sont à exécuter dans le dossier de l'application.
```sh
$ npm install
```

Puis on peut lancer le build grâce à la commande
suivante qui va créer un dossier ​ www​ regroupant
l'ensemble des fichiers devant être servis par un
serveur web quelconque (comme du contenu
statique).
```sh
$ npm run build --prod
``` 

Pour tout complément d'information se reporter à
la documentation du framework :

https://ionicframework.com/docs/intro/installation/
