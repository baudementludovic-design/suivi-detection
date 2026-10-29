# Suivi de détection F.F.P.J.P. — application installable

Ce dossier contient l'application prête à être mise en ligne sur **GitHub Pages** (gratuit).
Une fois en ligne, elle s'installe sur PC, tablette et téléphone et fonctionne **hors connexion**.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | l'application (identique au fichier « Suivi de détection.html ») |
| `manifest.webmanifest` | nom, couleurs et icônes de l'application |
| `sw.js` | fonctionnement hors connexion et mises à jour |
| `icons/` | icônes FFPJP (écran d'accueil, barre des tâches, onglet) |

Le dossier ne contient **aucune donnée de joueur** : les notes restent enregistrées sur chaque appareil.

## 1. Mettre l'application en ligne (une seule fois, ~10 minutes)

1. Créez un compte gratuit sur <https://github.com> (ou connectez-vous).
2. En haut à droite, cliquez sur **+** → **New repository**.
   - *Repository name* : `suivi-detection`
   - Cochez **Public** (obligatoire pour GitHub Pages gratuit — seul le code de l'application est public, jamais les données).
   - Cliquez sur **Create repository**.
3. Sur la page du dépôt, cliquez sur **uploading an existing file** (ou **Add file → Upload files**).
4. Faites glisser **tout le contenu du dossier** (`index.html`, `manifest.webmanifest`, `sw.js`, `LISEZMOI.md` et le dossier `icons`), puis cliquez sur **Commit changes**.
5. Allez dans **Settings** → **Pages** (menu de gauche).
   - *Source* : **Deploy from a branch**
   - *Branch* : **main** et **/ (root)** → **Save**.
6. Patientez 1 à 2 minutes puis rafraîchissez la page : l'adresse s'affiche en haut, du type
   `https://VOTRE-COMPTE.github.io/suivi-detection/`

C'est cette adresse que vous transmettez aux éducateurs.

## 2. Installer l'application

- **PC (Chrome ou Edge)** : ouvrez l'adresse, puis cliquez sur l'icône **Installer** à droite de la barre d'adresse (ou menu ⋮ → *Installer Suivi de détection*). L'application apparaît dans le menu Démarrer et peut être épinglée à la barre des tâches.
- **Android (Chrome)** : ouvrez l'adresse → menu ⋮ → **Installer l'application** / **Ajouter à l'écran d'accueil**.
- **iPhone / iPad (Safari)** : ouvrez l'adresse → bouton **Partager** → **Sur l'écran d'accueil**.

Après la première ouverture, l'application fonctionne sans connexion (terrain, gymnase…).

## 3. Mettre à jour l'application

Quand vous recevez une nouvelle version : sur GitHub, ouvrez le dépôt → **Add file → Upload files** → déposez le nouveau `index.html` → **Commit changes**.
Les appareils récupèrent la nouvelle version automatiquement à la prochaine ouverture avec connexion.
(Si vous changez aussi les icônes, augmentez le numéro `suivi-detection-v1` → `v2` dans `sw.js`.)

## 4. Les données

- Chaque appareil garde **ses propres données** (elles ne sont pas envoyées sur Internet).
- Pour **transférer** des saisies d'un appareil à l'autre, ou depuis l'ancien fichier HTML vers l'application installée :
  **Paramètres → Exporter (.json)** sur l'appareil d'origine, puis **Paramètres → Importer (.json)** sur l'autre
  (ou **Enregistrer une copie avec les données**).
- ⚠ L'import JSON remplace les données présentes sur l'appareil.
- Pensez à exporter régulièrement une sauvegarde (.json), notamment avant de changer d'appareil ou de vider le navigateur.
- Données de jeunes joueurs : ne déposez **jamais** de fichier .json ou de copie avec données sur GitHub.
