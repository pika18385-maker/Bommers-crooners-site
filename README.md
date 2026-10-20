# Boomers Crooners — site officiel

Site vitrine statique en français, conçu pour GitHub Pages. Le style mêle un fond sombre, des détails dorés et une typographie éditoriale. L'affichage est responsive sur ordinateur et téléphone.

## Contenu du dossier

- `index.html` — site public avec présentation, musique, concerts, galerie et contact.
- `site-data.json` — textes, images, liens, concerts et coordonnées affichés sur le site.
- `admin.html` — panneau de gestion qui prépare une branche et ouvre une Pull Request sans jamais la fusionner.
- `assets/favicon.svg` — icône du site.
- `assets/uploads/` — emplacement des photos envoyées avec le panneau d'administration.
- `404.html` et `styles.css` — page d'erreur personnalisée.
- `.nojekyll` — demande à GitHub Pages de servir les fichiers tels quels.

Les photographies actuelles sont des images génériques d'ambiance hébergées par Unsplash. Remplace-les par les photographies officielles du groupe quand elles sont disponibles. Aucun concert, e-mail ou profil social n'a été inventé : les champs non renseignés restent vides.

## Installation dans le dépôt GitHub

1. Télécharge le ZIP puis **extrais-le** sur ton appareil.
2. Ouvre le dépôt `pika18385-maker/Bommers-crooners` sur GitHub.
3. Choisis **Add file → Upload files** et envoie le contenu extrait du dossier (les fichiers doivent se retrouver à la racine du dépôt, avec le dossier `assets/`). Tu peux aussi utiliser GitHub Desktop.
4. Valide l'ajout des fichiers sur la branche `main` avec un message de commit, par exemple `Ajouter le site Boomers Crooners`.
5. Ouvre **Settings → Pages**. Sous **Build and deployment**, sélectionne **Deploy from a branch**, puis la branche `main` et le dossier `/ (root)`, et enregistre.
6. Une fois le déploiement terminé, le site devrait être accessible à `https://pika18385-maker.github.io/Bommers-crooners/`. Le panneau d'administration sera à `https://pika18385-maker.github.io/Bommers-crooners/admin.html`.

Le site n'est pas publié automatiquement par le simple fait de télécharger ce ZIP : il faut d'abord envoyer les fichiers et activer GitHub Pages.

## Panneau d'administration et Pull Requests

1. Sur GitHub, crée un **Fine-grained personal access token** avec accès uniquement au dépôt `Bommers-crooners`. Configure **Contents: Read and write** et **Pull requests: Read and write**. N'accorde pas des permissions plus larges que nécessaire.
2. Ouvre `admin.html` depuis le site hébergé et saisis le jeton dans le champ de connexion. Le jeton est gardé uniquement dans la mémoire de l'onglet pour la session courante ; le code ne l'inscrit ni dans un fichier ni dans le stockage du navigateur. Ferme l'onglet après utilisation.
3. Modifie les textes, les URLs des images, les liens ou les concerts. Pour envoyer une image depuis l'appareil, choisis JPG, PNG ou WebP de 4 Mo maximum.
4. Clique sur **Terminer — créer une Pull Request**. Le panneau crée une branche, commit les changements et ouvre une PR vers `main`.
5. Vérifie les fichiers modifiés dans GitHub. Fusionne la PR pour accepter les changements ou ferme-la pour les refuser. Le panneau ne fusionne jamais automatiquement.

### Sécurité à lire

Cette administration est destinée à un petit site statique. Son code est public et n'intègre aucun mot de passe secret. La protection des actions d'écriture repose sur le jeton GitHub fourni par l'administrateur ; une personne qui obtiendrait ce jeton pourrait agir dans la limite de ses permissions. Ne le partage jamais et ne le colle jamais dans une conversation, dans le dépôt ou dans une capture d'écran. Pour plusieurs administrateurs ou des données sensibles, préfère une authentification côté serveur/OAuth.

## Personnalisation

Les principaux textes et médias peuvent être mis à jour depuis `admin.html`, ou en modifiant `site-data.json` à la main. Les images importées depuis le panneau sont ajoutées à la branche de la Pull Request dans `assets/uploads/`.
