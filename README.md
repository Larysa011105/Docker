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


Jour 2 – Volumes, Réseaux & Inspection

🔹 Volumes

docker volume create [nom]
Crée un volume nommé pour stocker des données persistantes.

docker volume ls
Liste tous les volumes existants.

docker volume inspect [nom]
Affiche les détails d’un volume (chemin, utilisation…).


🔹 Réseaux

docker network ls
Liste les réseaux Docker disponibles.

docker network inspect [nom]
Affiche les détails d’un réseau (type, conteneurs connectés…).

docker network create --driver overlay [nom]
Crée un réseau overlay, utilisé pour connecter des services dans un cluster Swarm.



Jour 3 – Docker Compose

docker-compose up -d
Lance les services définis dans le fichier docker-compose.yml en arrière-plan.

docker-compose down
Arrête et supprime les conteneurs, réseaux et volumes créés par Compose.

docker-compose exec [service] [commande]
Exécute une commande dans un conteneur d’un service donné.

docker-compose logs
Affiche les logs des services gérés par Compose.

docker-compose build
Construit les images définies dans le fichier docker-compose.yml.

docker-compose ps
Liste les conteneurs en cours d’exécution via Compose.

docker-compose config
Valide et affiche la configuration complète du fichier docker-compose.yml.



Jour 4 – Docker Swarm & Stack

docker swarm init
Initialise un cluster Swarm sur le nœud actuel.

docker node ls
Liste les nœuds du cluster Swarm.

docker service create ...
Crée un service dans le cluster Swarm (avec options comme image, ports, réplication…).

docker stack deploy -c [fichier.yml] [nom]
Déploie une application multi-service définie dans un fichier YAML via une stack.





Conclusion

Ces commandes constituent la base pour travailler efficacement avec Docker. Elles permettent de manipuler les conteneurs, les images, les volumes, les réseaux et les services. En les combinant avec Docker Compose et Docker Swarm, vous pouvez orchestrer des applications complexes et distribuées. N'hésitez pas à expérimenter dans un environnement de test pour bien comprendre leur fonctionnement.
