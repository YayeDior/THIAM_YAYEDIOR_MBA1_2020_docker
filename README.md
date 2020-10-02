# THIAM_YAYEDIOR_MBA1_2020_docker

DOCUMENTATION PROJET DOCKER :BACKEND ET FRONTEND

Présentation:
Dans ce projet,il s'agit d’intégrer le déploiement d’une API Rest avec Docker afin de pouvoir le mettre dans un système d’intégration continue et de développement continue.

Prérequis:
Récupérer le projet API REST qui comporte une partie backend (API rest) et une partie frontend(reactJS)
Créer un/des fichier(s)DockerFile(s) pour builder notre image pour les serveurs de production
Créer un fichier docker-compose.yml pour démarrer nos containers, nos services
Modifier la documentation qui va expliquer le contenu de ces deux fichiers :
.DockerFile(s) pour builder notre imageb
.Docker-compose pour démarrer le(s) container(s) (Bien décrire l’ensemble desdifférentes étapes d’exécution des commandes associés aux services)

Consignes respectées:
Créer un nouveau repository sur GIT avec le code source de l’API rest : backend et Frontend
●Ajouter l’ensemble des nouveaux éléments dans la documentation du README
●Il est important de bien prendre en compte l’ensemble des configurations possibles au niveau des différents services utilisés pour l’API REST (BACKEND) et le FRONTEND
●Mettre en place des données par défaut dans mongoDB
●Définir bien l’ensemble des services dans votre docker-compose qui mettra en avant l’architecture de votre application web
●Le tout devra être sur une base principale avec Alpine (Pas forcément Alpine : Non obligatoire)

Projet:
Installation de MongoDB
j'ai utilisé MongoDB Atlas pour pouvoir connecter mon application avec ma base de données:J'ai mis mon projet dans mongoDB en créant un nouveau cluster dans le but de récuperer l'url qui me permet de me connecter à la base.

Pour vérifier si je suis bien connecté à la base,j'ai éffectué des test avec postman.

Mon  projet comporte deux fichiers Dockerfile:Dockerfile Backend et Dockerfile Frontend et un fichier docker-compose.yml qui se trouve à la racine du projet.
Les fichiers Dockerfile m'ont permis de builder mon image:j'ai utilisé les commandes suivantes pour les deux parties:Backend et Front end :
backend:
docker build -t backend .
docker images
docker run -p 8080:8080 backend
docker ps -a

Front end:
docker build -t frontend .
docker run -p 3000:3000 frontend
docker ps -a

Docker-compose.yml:
Ce fichier m'a permis de démarrer mes deux containers dans le meme docker:
La commande que j'ai utilisé est la suivantes:
docker-compose up --build:cette commande m'a permis de démarrer en meme temps MongoDB,ma partie front end et ma partie backend.

Bonus:
Mettre à jour mon image sur le registry public:Pour cela,j'ai utilisé Dockerhub:
Les commandes qui m'ont permis de faire cette tache sont:
docker login
docker tag aed1333b8f9b yayedior/projet_webservices_mds1_2020_backend:Back
docker push yayedior/projet_webservices_mds1_2020_backend
docker tag d4b2e4e874ce  yayedior/projet_webservices_mds1_2020_frontend
docker push yayedior/projet_webservices_mds1_2020_frontend

Ci dessous le lien de mon image sur Dockerhub

https://hub.docker.com/u/yayedior

Conclusion

Ce projet m'a permis de voir l'utilité de Docker qui est très interessant pour le déploiement des applications mais également d'intégrer une application dans ou plusieurs containers.
