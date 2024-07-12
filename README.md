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

## Workflow Git et GitHub de base 

- Faire une modif en local
- git add readme.md
- git commit -m "message de commit"
- git push origin main ==> pousser les modifs locales vers GitHub

