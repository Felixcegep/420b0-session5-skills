# Checklists rapides

## Exigence

- [ ] Une seule idée principale
- [ ] Compréhensible sans contexte caché
- [ ] Observable/testable
- [ ] Pas d'ambiguïté importante
- [ ] Pas de solution technique imposée sans nécessité
- [ ] Classée correctement fonctionnelle/non fonctionnelle
- [ ] Liée à un besoin ou un cas d'utilisation

## Cas d'utilisation

- [ ] Nom orienté objectif
- [ ] Acteur principal externe au système
- [ ] Déclencheur clair
- [ ] Préconditions pertinentes
- [ ] Scénario principal complet
- [ ] Chaque étape alterne logiquement acteur/système lorsque pertinent
- [ ] Exceptions/variantes importantes présentes
- [ ] Postconditions vérifiables
- [ ] Si essentiel : aucun clic/bouton/technologie inutile

## Modèle du domaine

- [ ] Concepts métier, pas classes techniques
- [ ] Attributs métier pertinents
- [ ] Associations nommées ou sémantiquement claires
- [ ] Multiplicités justifiées
- [ ] Pas de méthodes CRUD
- [ ] Pas de FK utilisées à la place d'associations
- [ ] Plusieurs-à-plusieurs traitées au bon niveau conceptuel
- [ ] Concepts nécessaires aux cas d'utilisation présents

## DSS

- [ ] Acteur externe présent
- [ ] Système vu comme boîte noire
- [ ] Messages dérivés du cas d'utilisation
- [ ] Ordre chronologique correct
- [ ] Paramètres métier utiles seulement
- [ ] Aucun contrôleur/service/repository/DB interne

## Normalisation

- [ ] Clé(s) candidate(s) identifiée(s)
- [ ] Dépendances fonctionnelles identifiées
- [ ] 1FN vérifiée
- [ ] Dépendances partielles retirées pour 2FN
- [ ] Dépendances transitives retirées pour 3FN
- [ ] Décomposition sans perte de sens évident

## Maquette

- [ ] Correspond à un cas d'utilisation réel
- [ ] Action principale claire
- [ ] Navigation cohérente
- [ ] Statut/feedback visible
- [ ] Erreurs prévenues ou expliquées
- [ ] Hiérarchie visuelle claire
- [ ] Texte lisible
- [ ] Contrôles cohérents
- [ ] Accessibilité de base considérée
