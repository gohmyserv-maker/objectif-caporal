# Objectif Caporal

Appli de révision du grade de caporal sapeur-pompier (SDIS 70) : fiches, quiz, cartes, oral, examen blanc.

## Déploiement
GitHub Pages publie la branche `main` (racine). Chaque push met le site à jour.

## Mise à jour automatique
L'appli est une PWA installable. Le service worker (`sw.js`) charge toujours la dernière version en ligne
et recharge l'appli dès que `version.json` change (à l'ouverture et toutes les 30 min).
Hors ligne, la dernière version consultée reste disponible.

## Progression
Elle est stockée dans le navigateur (localStorage), propre à chaque appareil.

## Publier une mise à jour
Modifier `index.html`, puis changer la même valeur dans `APP_VERSION` (index.html), `VERSION` (sw.js) et `version.json`.
