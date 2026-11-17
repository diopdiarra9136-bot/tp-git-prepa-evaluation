    PARTIE1:

Q1. L'option --global enregistre la configuration dans le fichier ~/.gitconfig . La configuration sans --global est spécifique à un dépôt et est stockée dans .git/config, uniquement pour ce dépôt.

Q2. L'email configuré doit correspondre à celui du compte GitHub pour que les commits s'affichent correctement dans le profil GitHub et pour permettre l'authentification/identification des contributions.

          PARTIE2:
          
Q3. Le dossier .git contient le dépôt Git local : l'historique des commits, les références (branches, tags), l'index, la configuration locale, etc. Si on le supprime, on perd entièrement l'historique du dépôt et les données de versionning du projet (sans restaurer les fichiers du projet eux-mêmes).

Q4. git diff montre les modifications qui sont dans le répertoire de travail mais pas encore indexées. git diff --staged montre les modifications déjà indexées et qui seront incluses dans le prochain commit.

Q5. La suite de caractères au début de chaque ligne de git log --oneline correspond à l'identifiant abrégé du commit (SHA, en version raccourcie), qui permet d'identifier précisément chaque commit.
