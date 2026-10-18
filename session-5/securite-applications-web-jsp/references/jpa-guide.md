# JPA — aide-mémoire

## One-to-many
La clé étrangère se trouve normalement du côté `ManyToOne`.

## Many-to-many simple
`@JoinTable` peut suffire si la table de relation ne contient que les clés des deux entités.

## Many-to-many avec données
Créer une entité de relation si elle porte des données comme `quantite`, `date`, `prix`, `statut`.

Exemple panier : si la relation Panier ↔ Produit porte `quantite`, utiliser une entité telle que `PanierProduit` avec deux `@ManyToOne` plutôt qu'un simple `@ManyToMany`.

## Cascades
La cascade représente une relation de cycle de vie, pas un raccourci à ajouter partout.
