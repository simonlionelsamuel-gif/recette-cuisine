# Nos courses (recette-cuisine)

App privée de liste de courses partagée, puis de recettes. Une seule base de code :

- **Web / iPhone** : https://simonlionelsamuel-gif.github.io/recette-cuisine/ → « Ajouter à l'écran d'accueil ».
- **Android** : APK publié dans les *Releases* de ce dépôt, installable et mis à jour via Obtainium (à venir).

Ce dépôt ne contient **que le code**. Les données (liste, favoris, recettes) sont dans le dépôt privé
`recette-cuisine-data`, lu et écrit par l'app avec un jeton d'accès limité à ce dépôt.

## Synchronisation
- Fichier `data/liste.json` dans le dépôt privé.
- Chaque téléphone vérifie les changements toutes les 10 s quand l'app est ouverte, et dès qu'on la rouvre.
- Fusion article par article (le plus récent gagne), suppressions gardées 30 jours pour la fusion.
- Hors ligne : tout est gardé sur le téléphone et envoyé au retour du réseau.
