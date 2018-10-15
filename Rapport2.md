
# Dépôt distant

contrairement à un depot local ,le dépot distant est hebergé sur une  machine autre que votre ordinateur personnel.
cette plateforme favorise un travail colaboratif .Elle permet ainsi aux differents collaborateurs autour d'un même projet  
de suivre l'evolution  de leurs travaux même à distance.

## Création d'un dépôt sur le serveur Gogs et sa récuperation  dans un dépôt local

pour créer un dépôt sur le serveur **Gogs**,il faut prealablement  avoir un compte d'utilisateur et un mot de passe qui vous 
permettront de vous connecter sur la plateforme.

![]("C:/Users/skeita/Desktop/depotDistant/creation de dopt en ligne.PNG")

En créant le dépôt à distant,apres lui avoir donné un nom,vous pouvez specificier s'il est privé 
(c'est à dire qu'il ne sera vu dans ce cas que par vos collaborateurs) ou visible par tous les utilisateurs du réseau
( par la mention public).

La commande ** git clone "l'url du dépôt distant" permet de le récuperer en local où l'on peut constater qu'un fichier README.md 
et un fichier .git sont créés par defaut pour l'initialiser. si c'est pas le cas, on peut directement creer le fichier README.md
si bésoin en local dans ledépôt ainsi importé.


![]("C:/Users/skeita/Desktop/depotDistant/recuperation du dupot.PNG")

## Ajout/commit/push de quelques fichiers dans le dépôt importé du Gogs

Il est obligatoire au prealable d'acceder au repertoire du dépôt (par la commande ** cd "nom_dépot" **) pour y ajouter des fichiers.
Vous pouvez utilser la  commande **touch "nom_fichier" pour la création de fichier(s).Avant d'executer le commit(par la commande **git comit -a),il faut les ajouter à 
l'étape intermediaire(**git add .** qui ajoute toutes les modifications à la fois).La commande **git push** permet de remonter ces nouvelles modifications au dépôt distant.


![]("C:/Users/skeita/Desktop/depotDistant/ajout_commit_push.PNG")


## vérification sur le site Gogs  des  modifications remontées

Il suffit de retourner au  Gogs et cliquer le le bouton "refresh".


## Association aux collaborateurs.

La collaboration se fait sur le serveur Gogs en accedant simplement à l'onglet **collaboration**.Ensuite on cherche le(s) 
futur(s) collaborateur(s) pour l'ajout.


![]("C:/Users/skeita/Desktop/depotDistant/ajoutCollaborateur.PNG")


## Récuperation du projet d'un collaborateur par un autre

le collaborateur recuperant le projet de son collèque  devra utiliser la commande **git clone "l'url du dépôtde son collègue"**.


![]("C:/Users/skeita/Desktop/depotDistant/recuperation du projet coll.PNG")


Dans l'exemple ci dessus ,sous  la demande de Ariane j'ai recupéré son projet au quel j'ai accédé pour consultation de son conténu.
*pour que cette operation soit possible,il faudrait que les deux soient collaborateurs avant*.A défaut, elle ne serait pas possible.


## Vérification  au local des  modifications realisées  par un collaborateur 

un colaborateur ayant apporté des modifications au projet de son coté(au local) devra les commiter puis pusher (vers le serveur)pour qu'elles accessibles par les
autres collaborateurs.Une fois cela faite ,les autres collaborateurs pourront récuperer ces modifications à parir du serveur par la commande **git pull**


## Modifications en parallèle d'un même fichier, Constat de situation de conflit et sa résolution.

vous serez confrontés à une situation de conflit(difference entre l'etat d'un fichier en local et son état à distance )si l'un de vos collaborateurs envoie des modifications sur le projet au moment où vous l'apportez vous aussi des modifications en local. dans une telle situation la mention "Master|Merging" apparait au bout du path du depôt (en ligne de commande)quant vous faites **git pull** vous demandant  de shynchroniser les differentes modificationsous. 


![]("C:/Users/skeita/Desktop/depotDistant/merging.PNG")


Quand on ouvre le fichier en question (en ligne de commande),la situation de conflit apparait comme dans l'exemple du contenu ci_dessous:


![]("C:/Users/skeita/Desktop/depotDistant/conflitt.PNG")


 Alors pour synchroniser ce fichier autrement dit  resoudre la situation de conflit,vous pouvez le faire manuellement en supprimant les lignes
indesirables dans le fichier(a travers un éditeur de texte  comme vi)  ou en utilisant  alternativement l'outil ** meld**,une interface graphique.


![]("C:/Users/skeita/Desktop/depotDistant/resolution...........PNG")


Ce contenu a été manuellement corrigé.Une fois la correction faite , il faut commiter de nouveau avant de faire **git push** pour remonter le fichier synchroniser.

