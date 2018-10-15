# Dépôt local

comme son nom l'indique le dépôt  local est un dossier créé  sur  votre machine pour garder les versions d'un projet 
que vous realisez.pour cela nous puvons utiliser l'outil **Git** fortement recommandé à cet effet.
L'utilisation de cet outil est facile à travers l'éditeur de lignes de commande *Git Bash* avec un syntaxe tres simple 
et des interfaces graphiques **Gitg,Gitk**.


## Création et initilisation du dépot,création de fichiers

Pour créer un depôt local on  se sert de la commande **mkdir nom_depot** et pour l'initiation ,on utilise  **git.init**.
Attention ,il faut d'abord acceder au repertoire du dépôt avant son initialisation.le dépôt etant initialisé,il suffit
d'utiliser la commande **touch  nom_fichier** pour la creation de fichier(s). **git status** montre l'état actuel du dépôt.
 
![]( "C:/Users/skeita/Desktop/depotlocalf/1cdif.PNG")

## Modifications du conténu de fichiers et execution des commits
la commande **vi nom_fichier** permet d'apporter des modifications dans un fichier via l'editeur de texte **vi**.
En effet on distingue deux princiales modes (**insert et commande**) qui permettent inserer du texte et enregistrer des modifications.
à travers  cet éditeur.Pour inserer du texte ,il faut prealablement taper le lettre **i** au clavier .Les touches **échap** puis **:wq**
permettent de  basculer en mode commande puis enregistrer et quitter l'éditeur de texte.

![]( "C:/Users/skeita/Desktop/depotlocalf/modification_file+comit.PNG")

Dans ce cas, seul le fichier nommé file a été commité , on utiliserait **git commit -a** pour versionner les deux fichiers 
à la fois.Ce qui necessiterait l'utilisation d'une console pour ecrire le message du commit.

## Comment renommer et supprimer un fichier?
la commande **git mv "nom_fichier" "nom_fichier** permet de renommer un fichier.Pour  La supression on sert de **git rm "nom_fichier"**.

![]( "C:/Users/skeita/Desktop/depotlocalf/4 supre-renomme.PNG")

## Comment afficher l'historique des commits et revenir dans un état précédent du dépot?

pour afficher les diffrentes versions d'un projet ou l'historique des commits on utilise la commande **git log**. 
Le retour dans un état précédent du dépôt consiste à annuler les dernieres modifications du projet .pour cela on utilise 
la commande *git checkout -- .*

![]( "C:/Users/skeita/Desktop/depotlocalf/5_histo_retour.PNG")


## comment ajouter une étiquette à un ancien commit et vérifier sa presence dans l'historique des commits ou avec un client Git graphique.

La commande *git tag "etiquette" "commit"* permet d'étiquetter le commit passé en parametre.Pour verifier sa presence dans 
l'historique à partir d'interface graphique on peut utiliser **gitg ou gitk**

![]( "C:/Users/skeita/Desktop/depotlocalf/6etiquettecommit.PNG")

la ligne de commande **git log** ne permet pas d'afficher l'étiquette du commit dans l'historique.Mais en revenche ,elle apparait dans le client graphique *gitk*

![]( "C:/Users/skeita/Desktop/depotlocalf/gitk.PNG")

