# Créer le projet Firebase du calendrier Feno

1. Va sur https://console.firebase.google.com et connecte-toi avec un
   compte Google Feno.
2. "Ajouter un projet" → nom `feno-calendrier` (Google Analytics
   optionnel, tu peux le désactiver) → Créer le projet.
3. Dans le menu de gauche : Build > Firestore Database > "Créer une
   base de données" → mode "Production" → région `eur3 (europe-west)`
   (proche de la France) → Activer.
4. Toujours dans Firestore : onglet "Règles" → coller le contenu de
   `firestore.rules` (fourni dans le dépôt) → Publier.
5. Menu de gauche > Build > Authentication > "Get started" > onglet
   "Sign-in method" > activer "Anonyme" (Anonymous) → Enregistrer.
6. Icône ⚙️ (Paramètres du projet) > onglet général > tout en bas
   "Vos applications" > icône Web `</>`  → nom "Calendrier Feno" →
   Enregistrer l'application. Firebase affiche un objet
   `firebaseConfig = { apiKey: ..., authDomain: ..., ... }`.
7. Copie ces valeurs dans `firebase-config.js` (remplace chaque
   `REPLACE_ME`), ou envoie-les moi et je les intègre.

C'est tout : pas de carte bancaire nécessaire pour ce volume d'usage
(plan gratuit Spark, largement suffisant pour un calendrier d'équipe).
