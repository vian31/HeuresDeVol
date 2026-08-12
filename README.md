# HDV — Journal des heures de vol

Application web autonome et pensée pour smartphone (un seul fichier HTML) pour enregistrer les heures de vol. Elle note les heures de départ et d'arrivée (**BLOC**) ainsi que les relevés de l'horamètre moteur, puis calcule automatiquement le temps de vol et l'écart d'horamètre, tous deux affichés au format **HH h MM**.

## Fonctionnalités

- Saisie par **molettes tactiles** (roues verticales), sans clavier.
- **Icône horloge** pour capturer l'heure courante d'un simple appui.
- Bouton **« Copier départ »** pour recopier l'horamètre de démarrage dans la section Arrivée.
- Sections **Départ / Arrivée repliables**, repliées par défaut à l'ouverture.
- Bloc **Total** toujours visible, avec signalement d'erreur :
  - le temps de vol BLOC dépasse le total HORAMÈTRE ;
  - l'une des deux valeurs n'est pas saisie.
- Popup **Paramètres · Aide** :
  - thème clair / sombre ;
  - cinq palettes de couleur ;
  - police des chiffres au choix (dont un affichage à sept segments) ;
  - onglet d'aide intégré.
- Préférences conservées via **localStorage** (repli sur cookie).
- Interface en français, sans framework ni dépendance externe.

## Utilisation

Ouvrir la page, déplier une section, régler les molettes, et lire les totaux calculés en bas. La contrainte 24 h est gérée automatiquement sur les heures.

## Hébergement (GitHub Pages)

1. Créer un dépôt et y déposer le fichier `hdv.html` (idéalement renommé `index.html`).
2. Dans **Settings → Pages**, choisir la branche `main` et le dossier racine `/`.
3. Ouvrir l'URL `https://<utilisateur>.github.io/<dépôt>/` fournie.

> **Important — persistance des données.** Les préférences (et tout stockage web) ne sont conservées de façon fiable que si la page est servie depuis une vraie origine `https://`. C'est exactement ce que fournit GitHub Pages. Ouvrir le fichier en local (`file://` ou `content://` sur Android) empêche cette persistance.

## Installation sur l'écran d'accueil

Une fois la page en ligne, l'ouvrir depuis le navigateur mobile puis choisir **« Ajouter à l'écran d'accueil »**. Le raccourci pointe vers l'URL `https://`, ce qui préserve la persistance des réglages.

## Détails techniques

- HTML / CSS / JavaScript purs, un seul fichier autonome.
- Police à sept segments et icône embarquées en base64 (aucun appel réseau).
- Conçu en priorité pour smartphone ; le bureau reste utilisable.
