# Quizzeo
Plateforme de quiz légère pour écoles, entreprises et utilisateurs.

Description
-----------
Quizzeo est une application PHP simple de création et de participation à des quizz. Elle contient :
- une interface d'accueil, inscription et connexion
- gestion basique des utilisateurs via fichiers CSV
- pages de quiz pour écoles, entreprises et utilisateurs
- système de commentaires et blog

Prérequis
---------
- PHP 8.0+ (PHP 8.2 recommandé)
- MAMP / Apache ou un serveur capable d'exécuter PHP
- Wasmer CLI (si vous souhaitez déployer dans Wasmer)

Installation locale (MAMP)
--------------------------
1. Copier le dossier dans le répertoire web de MAMP (ex : `/Applications/MAMP/htdocs/Quizzeo`).
2. Démarrer Apache et MySQL via MAMP.
3. Ouvrir dans le navigateur : `http://localhost:8888/Quizzeo/public/index.php`.

Lancer avec le serveur PHP intégré
---------------------------------
```bash
cd /Applications/MAMP/htdocs/Quizzeo/public
php -S localhost:8000
# Ouvrir http://localhost:8000
```

Structure du projet
-------------------
Les fichiers importants :

- `public/index.php` : routeur central (point d'entrée)
- `config.php` : configuration globale
- `accueil/` : pages publiques (home, connexion, inscription, profil, commentaires)
- `accueil/*.css`, `accueil/*.js` : ressources statiques
- `accueil/*.php` : scripts de traitement (traitement_connexion.php, traitement_inscription.php, etc.)
- `quizz/images/` : assets images (logo)

Routage et URLs
---------------
Le routeur central mappe des chemins propres aux fichiers PHP dans `accueil/`.
Exemples d'URLs :

- `/` ou `/home` → page d'accueil
- `/connexion` → page de connexion
- `/inscription` → page d'inscription
- `/profil` → page profil
- `/commentaires` → page commentaires
- `/traitement-connexion` → endpoint POST pour connexion
- `/traitement-inscription` → endpoint POST pour inscription


Dépannage rapide
----------------
- Si le CSS/JS ne charge pas : vérifier que les fichiers existent dans `accueil/` et appeler `http://host/accueil/accueil.css`.
- Si formulaire ne soumet pas : vérifier `action` du formulaire (doit pointer vers `/traitement-...`).
- Page blanche : activer l'affichage des erreurs PHP (`ini_set('display_errors',1); error_reporting(E_ALL);`).

Contribuer
----------
1. Forkez le projet
2. Créez une branche feature
3. Ouvrez une Pull Request

Licence
-------
Indiquer la licence souhaitée ici (MIT, GPL, ...).

Pour toute aide supplémentaire, dites-moi précisément ce que vous voulez ajouter dans le README (ex : sections techniques, diagrammes, exemples d'API, captures d'écran). 