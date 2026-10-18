# Aide-mémoire — Conception de logiciels 420-5A4

Ce fichier résume les contrôles les plus utiles. Pour une règle exacte, utiliser le GitBook comme source de vérité.

## 1. Exigences

### Exigence fonctionnelle
Décrit **ce que le système doit permettre ou faire** pour répondre à un besoin.

Bon réflexe : la formulation doit permettre d'imaginer un test d'acceptation.

À vérifier :
- une idée principale par exigence;
- acteur ou contexte compréhensible;
- comportement observable;
- pas de mots ambigus (« rapide », « facile », « adéquat ») sans critère;
- pas de détail d'interface inutile;
- cohérence avec le périmètre du système.

### Exigence non fonctionnelle
Décrit une **qualité, contrainte ou condition** applicable au système : performance, sécurité, accessibilité, compatibilité, fiabilité, etc.

Une bonne exigence non fonctionnelle doit idéalement être mesurable.

Exemple faible : « Le système doit être rapide. »
Exemple meilleur : « La recherche doit afficher les résultats en moins de 2 secondes pour 95 % des requêtes dans les conditions de charge définies. »

## 2. Cas d'utilisation

Un cas d'utilisation décrit un objectif atteint par un acteur grâce au système.

### Cas essentiel
Rester indépendant de l'interface et de la technologie.

Préférer :
- « L'enseignant indique la session. »
- « Le système présente les plans-cadres applicables. »

Éviter :
- « L'enseignant clique sur le bouton bleu Session. »
- « Angular envoie une requête POST. »

### Cas détaillé
Selon le gabarit du cours, il peut inclure :
- nom;
- acteur principal;
- objectif;
- déclencheur;
- préconditions;
- postconditions;
- scénario principal;
- variantes / exceptions.

Chaque étape du scénario principal doit faire avancer l'objectif.

## 3. Modèle du domaine

Le modèle du domaine représente les **concepts importants du métier** et leurs relations.

À rechercher :
- concepts nommés par des noms métier;
- attributs qui décrivent ces concepts;
- associations significatives;
- multiplicités justifiées par les règles métier.

À éviter :
- contrôleurs;
- services;
- repositories;
- méthodes CRUD;
- types techniques inutiles;
- clés étrangères utilisées comme substitut d'une association UML.

### Plusieurs-à-plusieurs
En UML conceptuel, une association `* ↔ *` peut être correcte.

Créer un concept d'association lorsqu'il existe une information ou une identité propre à la relation. Exemple générique : une **Inscription** entre Étudiant et Cours peut porter une date, une note ou un statut.

Dans un schéma relationnel, cette relation devient généralement une table associative. Ne pas confondre les deux niveaux.

## 4. DSS — Diagramme de séquence système

But : montrer les interactions entre acteur(s) et **le système vu de l'extérieur** pour un scénario.

Structure minimale :
- acteur;
- système;
- messages dans l'ordre temporel;
- retours importants au besoin.

Le DSS vient normalement des événements du scénario de cas d'utilisation.

Mauvais signe : voir `Controller`, `Service`, `Repository`, `Database` ou plusieurs objets internes dans un DSS système.

## 5. Modèle de données et normalisation

### 1FN
- chaque cellule contient une valeur atomique;
- pas de liste répétée dans une colonne;
- pas de groupe de colonnes répétitives du type `telephone1`, `telephone2`, `telephone3` si ces valeurs représentent le même concept multivalué.

### 2FN
- être en 1FN;
- chaque attribut non-clé dépend de **toute** la clé candidate pertinente.

Le problème apparaît surtout avec une clé composée.

Exemple :
`INSCRIPTION(NoEtudiant, NoCours, NomCours, Note)`
clé `(NoEtudiant, NoCours)`.
`NomCours` dépend seulement de `NoCours` → dépendance partielle → pas 2FN.

### 3FN
- être en 2FN;
- un attribut non-clé ne doit pas dépendre d'un autre attribut non-clé.

Exemple :
`ETUDIANT(NoEtudiant, NoProgramme, NomProgramme)`
`NoEtudiant -> NoProgramme -> NomProgramme`.
`NomProgramme` dépend transitivement de la clé → séparer PROGRAMME.

## 6. Maquettes

Une bonne maquette doit soutenir les tâches décrites dans les cas d'utilisation.

Questions de contrôle :
- L'utilisateur sait-il où il est?
- Le statut courant est-il visible?
- Les actions principales sont-elles évidentes?
- Les actions dangereuses demandent-elles confirmation si nécessaire?
- Les erreurs sont-elles expliquées près du problème?
- Les champs et libellés sont-ils compréhensibles?
- L'interface évite-t-elle les étapes inutiles?
- La navigation reste-t-elle cohérente d'un écran à l'autre?

## 7. Traçabilité

Toujours chercher les liens :

`Exigence → Cas d'utilisation → Concepts du domaine → DSS → Maquette → Données`

Un élément sans lien avec un besoin peut être superflu.
Un besoin sans élément de conception correspondant peut être incomplet.
