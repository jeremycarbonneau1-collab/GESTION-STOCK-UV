# Outil tablette « Tour du stock par chambre » — déploiement

En ligne : https://stock-univert.srv1745823.hstgr.cloud
VPS : projet Docker `stock-univert` (gestionnaire Docker Hostinger), même modèle que tours-culture.

## Mettre à jour l'outil
1. Remplacer `index.html` dans ce dépôt (branche main).
2. Redémarrer le projet `stock-univert` (hPanel → VPS → Docker Manager → Redémarrer) :
   au démarrage, le conteneur retélécharge `index.html` depuis GitHub.
   Si GitHub est injoignable, la version précédente est conservée.

## Sur la tablette
Ouvrir l'URL → menu du navigateur → « Ajouter à l'écran d'accueil » :
icône UNI-VERT, ouverture en plein écran.
