            INTRODUCTION

"la plate-forme Docker offre un haut degré de portabilité ,ce qui permet aux utilisateurs de s'enregistrement et partager de conteneurs sur une grande variéte d'hotes au sein d'environnement publics et privés .Il est alors possible de développer des aplications de façon plus efficiente,en utilisant moins de ressorces,et de déployer ces applications rapidement.
Docker est un outil incontournable pour le développement moderne.


JOUR 1 Conteneurs & Images

🔹 Conteneurs

docker ps
Affiche la liste des conteneurs en cours d'exécution.

docker ps -a
Affiche tous les conteneurs, y compris ceux arrêtés.

docker rm [nom]
Supprime un conteneur arrêté.

docker rm -f [nom]
Force la suppression d’un conteneur, même s’il est actif.

docker exec -it [nom] /bin/bash
Ouvre un terminal interactif dans le conteneur pour y exécuter des commandes.

docker inspect [nom]
Affiche les métadonnées détaillées du conteneur (réseau, volumes, configuration…).


docker logs --tail 5 [nom]
Affiche les 5 dernières lignes de logs du conteneur.

🔹 Images

docker images
Liste les images Docker disponibles localement.

docker rmi [image]
Supprime une image locale.

docker build -t [nom] .
Construit une image à partir d’un Dockerfile situé dans le répertoire courant.

docker history [image]
Affiche les couches successives ayant servi à construire l’image.

docker pull [image]
Télécharge une image depuis Docker Hub.

docker push [image]
Envoie une image vers Docker Hub.

docker search [mot-clé]
Recherche des images sur Docker Hub en fonction d’un mot-clé.


🔹 Informations système

docker info
Affiche les informations générales sur l’environnement Docker (version, nombre de conteneurs, etc.).

docker [commande] --help
Affiche l’aide intégrée pour une commande spécifique
