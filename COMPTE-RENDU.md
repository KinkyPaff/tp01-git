# Compte rendu - TP01 Git

## Question 0

La version de Git installée est 2.43.0 

## Question 1

https://github.com/KinkyPaff

## Question 2

user.name=Clementin
user.email=clementin.kuntzmann@e.rascol.net
init.defaultbranch=main
core.editor=nano

--global signifie que les configurations s'applique à tout les dépôts Git de l'utilisateur

Les fichiers de réglages sont enregistré dans le dossier .gitconfig dans le dossier personnel

## Question 3.1

git status : fatal: not a git repository (or any of the parent directories): .git

## Question 3.2

Dossier créé par git init : La commande a créé le dossier caché .git/

On ne le voyait pas car c'était un fichier caché

Git status indique que nous sommes sur la branche main et qu'il n'ya pas encore de commit

## Question 3.3

git status range README.md dans la section principale du repository (zone de travail). 



## Question 3.4 

La réponse de git status a changé grace à la commande git add README.md
Cette commande va prendre les fichiers en compte lors du prochain commit.

README.md se trouve désormais dans la zone de préparation.

## Question 3.5

commit bd77847e91e32a2df7058b66866d2bcaa24cfb16
Author: Clementin <clementin.kuntzmann@e.rascol.net>
Date:   Thu Oct 1 10:59:46 2026 +0200

    Création du README

Le hash contient 40 caractères.
Il est écrit en base 16.
Il représente 160 bits.

## Question 3.7

git status décrit README.md comme "modifié".

git diff montre les changements. Le + signifie ce qui a été ajouté au fichier.

## Question 3.8

b1c4fc2 (HEAD -> main, origin/main) Compte-rendu suite
d2f7d89 Modification du README
76279b5 Modification du memo
5b67cd3 Modification depuis l'interface github
5c94fd8 Ajout du fichier .gitignore
af59db8 Création de l'aide-mémoire Git
3060ed7 Ajout de l'année scolaire dans le README
55aafad Ajout du compte rendu (question 0 à 3.5)
bd77847 Création du README

Il est préférable de faire deux commits plutôt qu'un seul git add car on peut voir toute les modifications.

## Question 4.1

git show <hash> montre les modifications d'un commit précis.

## Question 4.2

git restore restaure la dernière version d'un fichier.
Non, on aurait pas pu récuperer le fichier si on ne l'avait jamais commité.

## Question 4.3

test.txt se trouve dans la staging area.
Le fichier n'a pas été supprimé du disque.

## Question 4.4

Les fichiers brouillons.txt, test.txt et log.txt ont disparu de la réponse de git status.
*.log signifie que tout les fichiers avec cette extension seront ignorés.
le fichier .gitignore apparait, il faut le commiter.

## Question 4.5

# TP01 - Découverte de Git

Dépôt réalisé par Clémentin Kuntzmann, 1CIEL-IR.

Ce dépôt contient mon compte rendu du TP01.


Le fichier contient désormais toute les réponse aux questions.

## Question 5.2

Les fichier id_ed25519.pub et id_ed25519 ont été crées.

Le .pub est la clé publique tandit que l'autre est la clé privé.

Permission clé publique : rwx------

Permissions clé privé : rw-------

La clé privé est en rw-------(600) car c'est la clé privé, elle ne doit pas sortir de l'ordinateur hôte et ne doit jamais être partagé.

## Question 5.4

Hi KinkyPaff! You've successfully authenticated, but GitHub does not provide shell access.

On peut donner sa clé publique sans problème à github car nous seul possédons la clé privé capable de la déchiffrer.

## Question 6.3

origin	git@github.com:KinkyPaff/tp01-git.git (fetch)
origin	git@github.com:KinkyPaff/tp01-git.git (push)


la branche 'main' est paramétrée pour suivre 'origin/main'.
Everything up-to-date


Non l'historique affiché n'est pas le même que celui affiché par git log --oneline.
Le fichier brouillon.txt n'est pas sur github car il a été ignore par le fichier .gitignore.

## Question 6.4 a

Le dépôt local ne contient pas la modification. 
git status indique qu'il y'a une version plus récente du commit.
Il faut utiliser la commande git pull pour mettre à jour vers le dernier commit.

## Question 6.4 b

Il s'est passé qu'on a récupérer les modifications du dernier commit enregistré.
L'auteur est KinkyPaff.

## Question 6.5

Répertoire de travail --(git add)--> Zone de préparation --(git commit -m)--> Dépôt local --(git push)--> GitHub
          ^                                                                               |
          +--------------------------------------( ? )------------------------------------+


## Question 7.1

Le clone contient uniquement la dernière version des fichiers.
Le fichier brouillon.txt n'est pas dans le clone car non envoyé sur github.
Non on à pas eu besoin de faire git init car le dépôt cloné est déja initialisé.

## Question 7.2

Car il faut absolument récuperer la dernière version des fichiers avant de commencer de travailler pour éviter les conflits et mauvaise surprises.
Et pour git push il faut toujours envoyer sur github en fin de scénace le travail.

## Question 7.3

TP01 — Découverte de Git et GitHub : vérification
Dépôt vérifié : /rhome/ckuntzmann/tp-git/tp01-git

=== Partie 2 — Configuration de Git ===
  [OK]     Nom configuré (user.name)
  [OK]     E-mail configuré (user.email)
  [OK]     Branche par défaut : main
  [INFO]   Auteur des commits : Clementin <clementin.kuntzmann@e.rascol.net>

=== Partie 3 — Premier dépôt ===
  [OK]     Le dossier est un dépôt Git
  [OK]     Branche courante : main
  [OK]     README.md est suivi
  [OK]     COMPTE-RENDU.md est suivi
  [OK]     memo-git.md est suivi
  [OK]     Au moins 8 commits
  [OK]     Messages de commit variés
  [INFO]   Nombre de commits : 9

=== Partie 4 — .gitignore ===
  [OK]     .gitignore est suivi
  [OK]     brouillon.txt est ignoré
  [OK]     Les fichiers *.log sont ignorés
  [OK]     brouillon.txt n'est pas dans le dépôt

=== Partie 5 — Clé SSH ===
  [OK]     Clé privée ~/.ssh/id_ed25519 présente
  [OK]     Clé publique ~/.ssh/id_ed25519.pub présente
  [ECHEC]  Clé privée protégée (600)
  [OK]     Authentification SSH auprès de GitHub
  [OK]     Aucune clé privée dans l'historique du dépôt

=== Partie 6 — Publication sur GitHub ===
  [OK]     Dépôt distant origin en SSH (git@github.com:…/tp01-git.git)
  [OK]     Dépôt distant accessible (git fetch)
  [OK]     Un commit fait depuis l'interface web de GitHub, récupéré avec git pull
  [ECHEC]  Aucune modification en attente (git status propre)
  [OK]     Tous les commits sont poussés sur GitHub

=== Partie 7 — Compte rendu ===
  [OK]     COMPTE-RENDU.md contient la partie 7

Score : 23 / 25 — corrigez les points en ECHEC, puis relancez le script.


Il se passe que rien n'est envoyé sur github car on a pas fait git add.


