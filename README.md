#  vacance de rêve un blog avec  Wordpress

## procédure d'installation:

1.
initialiser le projet avec `composer init`=> On valide avec entrée tout du long sauf pour les questions.

```
Would you like to define your dependencies (require) interactively [yes]? no
Would you like to define your dev dependencies (require-dev) interactively [yes]? no
```

ce `composer init` crée notre `composer.json`

2.
on demande à composer d'installer le code de wordpress dans un répertoire `wp` (pas obligatoire)
On définit une option dans le fichier composer.json pour gérer (si on veut le faire )le nom du dossier dans lequel on installera wordpress
installer le package _johnpbloch/wordpress_ : `composer require johnpbloch/wordpress`

warning: il ne faut pas oublier d'ajouter au .gitignore (ou de l créer)

3. on récupère index.php et wp-config-sample.php depuis les fichiers de wordpress(installés dans le répertoire wp). Il faut adapter le chemin du require présent dans index.php : `'require _DIR_ ./wp/'`

```
vendor
wp
```
4. on ajoute nos identifiants de base de données dans une ***copie*** du fichier `wp-config.sample`  que l'on nomme `wp-config.php`!

On a maintenant accès à un formulaire nous permettant d'installer wp (ne pas utiliser)
