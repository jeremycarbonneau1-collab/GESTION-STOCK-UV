# Déploiement de l'outil tablette sur le VPS

URL cible : https://stock-univert.srv1745823.hstgr.cloud

## 1re installation (en SSH sur le VPS)
```bash
mkdir -p /docker/STOCK-UNIVERT/html
cd /docker/STOCK-UNIVERT
# copier docker-compose.yml ici, puis :
wget -O html/index.html "https://raw.githubusercontent.com/jeremycarbonneau1-collab/GESTION-STOCK-UV/main/index.html"
docker compose up -d
```
Le certificat HTTPS est créé automatiquement par Traefik (1re ouverture : quelques secondes).
Si le sous-domaine ne répond pas : vérifier le nom d'entrypoint de Traefik
(`docker inspect n8n-traefik-1 | grep entrypoints`) et l'ajuster dans docker-compose.yml.

## Mise à jour (nouvelle version de l'outil)
```bash
wget -O /docker/STOCK-UNIVERT/html/index.html "https://raw.githubusercontent.com/jeremycarbonneau1-collab/GESTION-STOCK-UV/main/index.html"
```
Pas besoin de redémarrer le conteneur.

## Sur la tablette
Ouvrir l'URL dans Chrome / Safari → menu → « Ajouter à l'écran d'accueil » :
l'icône UNI-VERT apparaît et l'outil s'ouvre en plein écran.
