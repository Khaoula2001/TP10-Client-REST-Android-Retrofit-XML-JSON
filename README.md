# TP 10 — Client REST Android (Retrofit)

## Objectif
Petite app Android qui consomme un service REST pour gérer des comptes bancaires (CRUD) avec Retrofit + RecyclerView.

## Démo vidéo
Voir la démo: https://github.com/user-attachments/assets/828d47e6-566d-402a-8fa7-247a783f0ccb

Astuce: remplacez le texte entre parenthèses par l’URL de votre vidéo (YouTube/Drive/etc.).

## ⚙️ Démarrage rapide
1. Ouvrez le projet dans Android Studio.
2. Base URL: éditez `app/src/main/java/ma/projet/restclient/config/RetrofitClient.java` (champ `BASE_URL`).
   - Émulateur: `http://10.0.2.2:8082/`
   - Appareil physique: `http://IP_DE_VOTRE_PC:8082/`
3. HTTP en clair: vérifiez `app/src/main/res/xml/network_security_config.xml` + `AndroidManifest.xml` (attribut `android:networkSecurityConfig`).
4. Démarrez le backend puis lancez l’app.

## Fonctionnalités
- Lister, ajouter, modifier, supprimer un compte
- JSON et/ou XML selon votre backend
- Affichage via `RecyclerView`

## Fichiers clés
- `MainActivity` — logique écran principal
- `CompteService` — endpoints REST
- `RetrofitClient` — config Retrofit (BASE_URL, converters)
- `CompteAdapter` — liste des comptes
- `entities/Compte`, `entities/CompteList` (XML)

## Test rapide
1. Démarrer le backend REST.
2. Ouvrir l’app, vérifier la liste des comptes.
3. Tenter un ajout/modification/suppression et observer Logcat en cas d’erreur.

## Notes
- Sur émulateur, utilisez `10.0.2.2` au lieu de `localhost`.
- XML: activer le converter SimpleXML et utiliser `CompteList` si le backend renvoie une liste XML.

