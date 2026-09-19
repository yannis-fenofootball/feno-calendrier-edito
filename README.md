# Calendrier éditorial Feno Football

Site statique (HTML/CSS/JS, aucun build) déployé sur Vercel, données
partagées via Firebase Firestore.

## Déploiement

1. Créer un projet Firebase (voir `FIREBASE.md`), activer Firestore +
   l'authentification anonyme, puis remplir `firebase-config.js` avec la
   config du projet (Console Firebase > Paramètres du projet > Tes
   applications).
2. Publier les règles `firestore.rules` dans Firestore (onglet "Règles").
3. Pousser ce dépôt sur GitHub.
4. Sur vercel.com : "Add New Project" → importer ce dépôt → aucun réglage
   de build nécessaire (site statique) → Deploy.
5. Dans le projet Vercel : Settings > Domains > ajouter
   `calendrier.fenofootball.fr`, puis créer chez votre registrar/DNS le
   enregistrement CNAME indiqué par Vercel pointant vers
   `cname.vercel-dns.com`.

## Fichiers

- `index.html` — l'application complète (calendrier, formulaires, rendu).
- `firebase-config.js` — configuration Firebase (à remplir, non secrète).
- `firestore.rules` — règles de sécurité Firestore à publier côté Firebase.
- `vercel.json` — réglages Vercel (URLs propres).
