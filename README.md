# Pilotage Com

Application PWA de **pilotage de communication multi-campagnes**.

## Fonctionnalités

- **Multi-campagnes** : créez autant de campagnes / événements que vous voulez
- Écran d’accueil avec « Événements proches » et archives
- Dashboard complet par campagne (KPIs, planning, filtres, calendrier)
- Actions : création, modification, statut, priorité, canaux, responsable, rappels
- Résumé WhatsApp prêt à copier
- Export / Import JSON (sauvegarde & transfert entre appareils)
- 100 % local (localStorage) — aucune donnée envoyée ailleurs
- Installable en PWA (Android & iOS)

La campagne **SEHO MARO KANTO 2.0** est préchargée comme exemple.

## Fichiers

- `index.html` — application complète
- `manifest.webmanifest` — identité PWA
- `service-worker.js` — cache hors-ligne
- `icons/` — icônes (à ajouter)

## Déploiement

1. Publiez tout le contenu sur un hébergement HTTPS (GitHub Pages, Netlify, etc.)
2. Ouvrez l’URL sur le téléphone
3. Installez l’application (Ajouter à l’écran d’accueil)

## Mise à jour du cache

Augmentez `CACHE_NAME` dans `service-worker.js` (ex. `pilotcom-v2`) puis republiez.
