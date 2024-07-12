# Mémo Git et GitHub

## Git

### Installation Git

- Se mettre sur le terminal 
- sudo apt install Git
- git --version ==> Vérifier si il a bien été installé

### Initialisation

- cd et/ ou mkdir et/ ou ls ==> Se mettre sur le bon dossier à tracer 
- git init
- touch test.py ==> Création du fichier
- git status ==> Vérifier 

### Staging et commit

- git add test.py
- git commit -m "message de commit"

### Checking

- git log ==> Visualiser l'historique de commits
- git diff ==> Avant de faire un nouveau commit, visualiser la modif faite dans mon fichier 
- git status ==> Vérifier s'il y a eu de la modif non commit

### Branch

- git branch nom_de_branch ==> Créer une nouvelle branch
- git branch ==> Afficher toutes les branchs créées et montrer sur quelle branche je suis actuellement
- git checkout master/ nom_de_branch/ identifiant_unique ==> Se déplacer entre les branchs

### Fusionner les branchs

- git checkout master ==> Se mettre sur master
- git merge nom_de_branch ==> Fusionner
- git branch -d nom_de_branch ==> Supprimer le branch fusionné car il n'y a plus d'intérêt de le garder 

## Différence entre Git et GitHub

Git est un projet open source de gestion de versions de code.

GitHub est une platforme d'hébergement de projets Git. 

## Création du code SSH

- Sur le terminal, faire : cd .ssh/ ==> Se mettre sur le bon dossier
- ssh-keygen -t ed25519 -C "your_email@example.com" ==> Créer un code SSH
- Faire "Entrée" plusieurs fois pour aller jusqu'au bout 
- eval "$(ssh-agent -s)" ==> Assurer que l'agent est présent
- ssh-add ~/.ssh/id_ed25519 ==> Ajouter le clé à l'agent
- cat id_ed25519.pub ==> Visualiser le clé 
- Pour ajouter ce clé sur GitHub, aller sur Settings 

## Workflow Git et GitHub de base 

- Faire une modif en local
- git add readme.md
- git commit -m "message de commit"
- git push origin main ==> pousser les modifs locales vers GitHub

## Aligner mon git local et mon repository GitHub

- Il faut d'abord créer mon repository sur GitHub
- Sur le terminal, se mettre sur le bon dossier
- Initialiser git, ajouter mon fichier concerné (ce fichier on peut soit le créer à la main sur vs code soit faire echo) 
- Faire le permier commit
- git branch -M main ==> Renommer le master, obligatoire pour x raison
- git remote add origin le_lien_du_repository_GitHub
- git remote show origin ==> Confirmer en faisant "yes" si besoin 
- git push -u origin main

## Collaborer sur GitHub

- Pour inviter qq d'autre il faut aller sur le Setting sur mon repository
- Pour travailler sur le repository de qq d'autre, accepter l'invitation, ensuite assurer que je suis sur le bon dossier (faire le nécessaire sur le terminal)
- Sur le repository partagé, cliquer sur "code" et copier l'url SSH
- Faire git clone url_SSH

### Pull

- git pull ==> pour récupérer les travaux des autres

### Push

- Faire la modif
- git add
- git commit
- git push 
- Si jamais il y a un conflit et push rejeté, il faut faire un pull d'abord, choisir le stratégie (git config pull.rebase false, ctrl s + ctrl x), refaire un pull et ensuite push
