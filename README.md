# Depôt local

comme son nom l'indique est depot local est un dossier créésur votre machine pour garder les versions d'un projet que vous realisez.
pour cela nous puvons utiliser l'outil Git fortement recommandé à cette effet. l'utilisation de cet outil est facile à travers 
l'éditeur de lignes de commande *Git Bash* avec un syntaxe tres simple et des interfaces graphiques *Gitg,Gitk*.

##Création et initiation du depôt,création de fichiers

pour creer un depôt local on sert de la commande *mkdir nom_depot* et pour l'initiation ,on utilise *git.init*.Attention ,il faut 
d'abord au repertoire du depôt avec de l'initialisation.le depôt etant initialisé,il suffit d'utiliser la commande *touche nom_fichier* pour la creation de fichier(s). *git status* montre l'état actuel du depôt.
![]( "C:/Users/skeita/Desktop/depotlocalf/1cdif.PNG")

## Modifications dans les fichiers et execution des commits
la commande *vi nom_fichier* permet d'apprter des modifications dans un fichier via l'editeur de texte **vi**.En effet deux  distingue deux princiales modes (* insert et commande*) sont disposibles pour la gestion de cet éditeur.ainsi pour inserer du texte ,il faut prealablement taper le lettre *i* au clavier .pour basculer en mode commande qui permet d'enregistrer les modifications ,on utilise les touches*échap et :wq*.pour realiser des commits,il faut imperativement ajouter  en premier le fichier à l'etape intermediaire de versionning en utilisant *git add nom_fi

