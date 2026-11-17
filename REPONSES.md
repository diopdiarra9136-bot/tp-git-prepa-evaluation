    PARTIE1:

Q1. L'option --global enregistre la configuration dans le fichier ~/.gitconfig . La configuration sans --global est spécifique à un dépôt et est stockée dans .git/config, uniquement pour ce dépôt.

Q2. L'email configuré doit correspondre à celui du compte GitHub pour que les commits s'affichent correctement dans le profil GitHub et pour permettre l'authentification/identification des contributions.

          PARTIE2:

Q3. Le dossier .git contient le dépôt Git local : l'historique des commits, les références (branches, tags), l'index, la configuration locale, etc. Si on le supprime, on perd entièrement l'historique du dépôt et les données de versionning du projet (sans restaurer les fichiers du projet eux-mêmes).

Q4. git diff montre les modifications qui sont dans le répertoire de travail mais pas encore indexées. git diff --staged montre les modifications déjà indexées et qui seront incluses dans le prochain commit.

Q5. La suite de caractères au début de chaque ligne de git log --oneline correspond à l'identifiant abrégé du commit (SHA, en version raccourcie), qui permet d'identifier précisément chaque commit.
<<<<<<< HEAD

=======
         patrie3:
 Q6. On ne versionne pas Main.class parce qu'il est un fichier généré par la compilation Java, il peut être recréé à partir du code source. Le fichier .gitignore simplifie le travail avec git add . en évitant d'ajouter automatiquement les fichiers générés inutiles dans le dépôt.

Q7. git revert annule le dernier commit en créant un nouveau commit de correction ; l'historique est conservé et il est sûr pour un commit déjà poussé. git reset --hard revient en arrière en réécrivant l'historique local ; il peut perdre des changements et est à utiliser avec prudence, surtout après push.

Q8. git reset --hard HEAD~1 supprime le dernier commit et toutes les modifications associées, donc le travail est perdu. HEAD~1 désigne le parent du commit courant ; c'est le commit précédent dans l'historique. "detached HEAD" signifie que HEAD pointe directement sur un commit, sans être attaché à une branche, donc on a quitté temporairement la branche main.
   partie4:
   9. La multiplication est absente de Main.java sur main parce que la branche multiplication est une ligne de développement différente : ses modifications n'existent que dans cette branche, tant qu'on ne les fusionne pas dans main.

Q10. Une fusion fast-forward se produit quand la branche courante n'a pas divergé : le pointeur de branche avance simplement au niveau du commit de l'autre branche. Dans l'étape 4.4, il y a un conflit de modification sur la même ligne dans README.md, donc Git ne peut pas simplement avancer et crée un commit de fusion avec résolution du conflit.

Q11. Les marqueurs <<<<<<< HEAD, =======, >>>>>>> titre indiquent le début de la version courante (HEAD), la séparation, puis la version de la branche fusionnée (titre). Git ne peut pas fusionner automatiquement quand les deux branches ont modifié la même zone du même fichier de façon conflictuelle.
     partie5
 Q12. origin désigne le dépôt distant enregistré comme nom de remote. L'option -u de git push enregistre la relation entre la branche locale et la branche distante pour que les futurs git push et git pull soient plus simples.

Q13. git fetch télécharge les nouveautés du dépôt distant sans fusionner dans la branche locale. git pull fait les deux à la fois : fetch + merge (ou rebase selon la configuration).

Q14. Le git push a été refusé parce que la branche locale était en retard par rapport au dépôt distant : un autre poste avait déjà modifié le même fichier. La bonne habitude est de faire un git pull (ou git fetch puis merge/rebase) avant de pousser pour intégrer les changements distants et éviter les conflits.
       PARTIE6:
 
Q15. Un fork est une copie de dépôt sur GitHub appartenant à l'utilisateur. Un clone est la copie locale d'un dépôt, qu'il soit public ou fork. Une branche est une ligne de développement parallèle dans un même dépôt, sans créer un autre dépôt.

Q16. On propose une PR depuis une branche dédiée pour isoler la fonctionnalité, garder main propre, faciliter la revue, et permettre de travailler sur plusieurs changements indépendants. La branche dédiée permet de comparer précisément la modification demandée avec la branche cible.

Q17. Les remotes servent à nommer les dépôts distants auxquels on va se connecter, par exemple origin (le dépôt principal que l'on a forké ou créé) et upstream (le dépôt d'origine auquel on souhaite mettre à jour son fork).
     partie7
 Q18. Niveau choisi : "Introduction Sequence" (exemple). Commandes :
- git commit
- git branch
- git merge          
