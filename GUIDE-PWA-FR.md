# SEHO MARO KANTO 2.0 — PWA

## Contenu
- `index.html` : dashboard mobile-first (HTML/CSS/JavaScript intégrés)
- `manifest.webmanifest` : identité et options d’installation de l’application
- `service-worker.js` : cache de l’interface pour un usage hors connexion après le premier chargement
- `icons/` : icônes Android et iOS

## Important : pourquoi le fichier ne s’ouvre pas comme une PWA depuis Fichiers
Une PWA nécessite une adresse web sécurisée en **HTTPS** (ou `localhost` pour les tests). Ouvrir `index.html` directement depuis l’application Fichiers avec une adresse `file://` ne permet pas d’activer le service worker ni l’installation PWA.

## Mise en ligne simple
1. Décompressez le ZIP.
2. Publiez **tout le contenu du dossier** sur un hébergement statique HTTPS (par exemple Netlify Drop, GitHub Pages ou votre hébergement habituel).
3. Ouvrez l’URL HTTPS publiée sur le téléphone.
4. Vérifiez que le dashboard s’affiche, puis installez-le :
   - **iPhone/iPad (Safari)** : bouton Partager → **Sur l’écran d’accueil**. Si proposé, activer « Ouvrir comme app web ».
   - **Android (Chrome)** : menu ⋮ → **Installer l’application** ou **Ajouter à l’écran d’accueil**.

## Fonctionnement hors ligne et données
- Après un premier chargement réussi, l’interface est mise en cache et peut s’ouvrir hors connexion.
- Les données gérées par le dashboard dans `localStorage` restent propres au navigateur/appareil. L’installation sur un autre appareil ne les transfère pas automatiquement : utilisez Exporter/Importer.
- La synchronisation Google Sheet nécessite une connexion Internet.
- Les notifications dépendent du navigateur, de l’appareil et des autorisations accordées.

## Mise à jour
Pour une nouvelle version, remplacez `index.html` et augmentez la valeur `CACHE_NAME` dans `service-worker.js` (ex. `v2`), puis republiez.
