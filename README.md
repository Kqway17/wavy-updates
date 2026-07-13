# Wavy Eats Browser — mises à jour

Ce dépôt sert **uniquement** au système de mise à jour automatique de
Wavy Eats Browser. L'application lit le fichier [`version.json`](version.json)
pour savoir si une nouvelle version est disponible.

## Publier une nouvelle version

1. Dans l'app, augmente `"version"` dans `safe-electron-app/package.json`
   (ex. `1.1.0`), fais tes modifs, puis recrée le zip
   `WAVY-EATS-BROWSER-PACKAGE.zip`.
2. Crée une **Release** ici (onglet *Releases*), tag `v1.1.0`, et joins le zip.
3. Mets à jour [`version.json`](version.json) :
   - `version` → le nouveau numéro
   - `url` → le lien direct du zip de la release
   - `notes` → ce qui a changé (texte affiché dans l'app)
   - `sha256` (optionnel) → empreinte du zip pour vérification d'intégrité

L'application détectera la nouvelle version au prochain démarrage.
