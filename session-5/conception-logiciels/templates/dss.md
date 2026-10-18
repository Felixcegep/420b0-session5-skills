# Gabarit — DSS textuel

Acteur → Système : `evenementSysteme(parametresMetier)`

Système → Acteur : résultat / information affichée

Répéter selon le scénario.

## Exemple générique

Enseignant → Système : `selectionnerCours(cours)`

Système → Enseignant : plans-cadres applicables

Enseignant → Système : `choisirPlanCadre(planCadre)`

Système → Enseignant : informations du plan de cours initialisées

## Règle

Le DSS ne montre pas :
- UI interne;
- Controller;
- Service;
- Repository;
- Base de données;
- entités internes qui se passent des messages.

Ces éléments appartiennent à un niveau de conception interne différent.
