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

git status décrit README.md comme

git diff montre les changements. Le + signifie ce qui a été ajouté au fichier.
