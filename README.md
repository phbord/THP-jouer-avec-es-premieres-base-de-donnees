# README

__Outils__
- Diagramme ERD : [https://online.visual-paradigm.com/](https://online.visual-paradigm.com/)
- Client SQLite : [https://sqlitebrowser.org/](https://sqlitebrowser.org/)


## 1. INTRODUCTION
3 exercices
## 2. BLOGGING
### 2.1 Architecture
- plusieurs *user* avec un nom
- Chaque *user* peut créer plusieurs *article*
- chaque *article* est forcément créé par un *user*
- Un *article* peut appartenir à plusieurs *category*
- chaque *category* peuvent avoir plusieurs *article*
  - Chaque *category* a un titre
- Une *catégorie* peut appartenir à plusieurs *tag*
- chaque *tag* a un titre et une couleur

### 2.2 Tables
- `user`
- `article`
- `category`
- `tag`

### 2.3 Concept
Il doit y avoir différents :
- `tables`
- `attributs`
- `jointures`

## 3. SITES ET BASES DE DONNEES

### 3.1. MOOCademy
- plusieurs *cours*
- chaque *cours* a un *titre* et une *description*
- chaque *cours* a plusieurs *leçons*
  - qui ont un *titre* et un *body*

### 3.2. The Hacking Pinterest
- plusieurs *pins*
- chaque pin contient l'*URL* d'une image (sur le net)
- possibilité de *commenter* les *pins* (mais pas les commentaires)

### 3.3. The Hacking News
- créer un message board
- les *utilisateurs* peuvent poster des *liens*
- les autres *utilisateurs* peuvent *commenter*
  - les *liens* soumis
  - ou les *commentaires*
- comment faire en sorte qu'un *commentaire* sache où il se trouve dans la *hiérarchie* ?

### 3.4. The Hacking Class
- plusieurs *élèves* peuvent s'inscrire à un seul *cours*
- un *cours* pourra avoir plusieurs *élèves*

## 4. FAIRE DES REQUETES EN BASES
- récupérer le fichier de BDD `chinook.db`
- la requête doit se faire en une seule ligne de SQL
- et ne doit pas s'appuyer sur d'autres requêtes

### 4.1 Requêtes
- Récupérer tous les albums
- Récupérer tous les albums dont le titre contient "Great" (indice)
- Donner le nombre total d'albums contenus dans la base (sans regarder les id bien sûr)
- Supprimer tous les albums dont le nom contient "music"
- Récupérer tous les albums écrits par AC/DC
- Récupérer tous les titres des albums de AC/DC
- Récupérer la liste des titres de l'album "Let There Be Rock"
- Afficher le prix de cet album ainsi que sa durée totale
- Afficher le coût de l'intégralité de la discographie de "Deep Purple"
- Créer l'album de ton artiste favori en base, en renseignant correctement les trois tables albums, artists et tracks

## 5. CONCEVOIR DES BASES DE DONNEES DE SITES, Vol. 2
- créer les bases de données que tu as conçues, en utilisant SQLite3

## 6. RENDU ATTENDU
- fichier *.txt* (ou *.md*) ou diagramme *ERD* avec la structure de chaque BDD
  - Blog
  - MOOCacademy
  - Hackinterest
  - Hacking News
  - Hacking Class
- fichier *.txt* (ou *.md*) contenant les requêtes *SQL* qui permettent d'obtenir les infos demandées
  - => __BDD musicale__
- fichier .sqlite contenant la BDD de chaque appli