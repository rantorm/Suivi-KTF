# Pilotage Com — Guide PWA

## Contenu
- `index.html` : application multi-campagnes (HTML/CSS/JavaScript intégrés)
- `manifest.webmanifest` : identité et options d’installation
- `service-worker.js` : cache de l’interface pour usage hors connexion
- `icons/` : icônes Android et iOS (à fournir)

## Important : HTTPS obligatoire
Une PWA nécessite une adresse web sécurisée en **HTTPS** (ou `localhost` pour les tests).  
Ouvrir `index.html` directement depuis l’application Fichiers (`file://`) ne permet pas d’activer le service worker ni l’installation PWA.

## Mise en ligne simple
1. Publiez **tout le contenu du dossier** sur un hébergement statique HTTPS (Netlify Drop, GitHub Pages, etc.).
2. Ouvrez l’URL HTTPS sur le téléphone.
3. Installez l’application :
   - **iPhone/iPad (Safari)** : bouton Partager → **Sur l’écran d’accueil**
   - **Android (Chrome)** : menu ⋮ → **Installer l’application**

## Fonctionnement
- Après un premier chargement réussi, l’interface est mise en cache et peut s’ouvrir hors connexion.
- Les données sont stockées dans `localStorage` (propres à l’appareil).
- Utilisez **Exporter / Importer** (Paramètres) pour sauvegarder ou transférer vers un autre appareil.
- Les rappels (notifications) dépendent du navigateur et des autorisations.

## Mise à jour
Pour une nouvelle version, remplacez `index.html` et augmentez la valeur `CACHE_NAME` dans `service-worker.js` (ex. `pilotcom-v2`), puis republiez.
