# Gabarit — normalisation

## 0. Relation de départ

`R(A, B, C, D, ...)`

## 1. Clé candidate

Clé : `( ... )`

## 2. Dépendances fonctionnelles

- `X -> Y`
- `...`

## 3. 1FN

Question : chaque attribut contient-il une valeur atomique et non un groupe répétitif?

Correction si nécessaire : ...

## 4. 2FN

Question : un attribut non-clé dépend-il seulement d'une **partie** d'une clé composée?

Dépendance problématique : `... -> ...`

Décomposition :
- `R1(...)`
- `R2(...)`

## 5. 3FN

Question : existe-t-il `clé -> attribut non-clé -> autre attribut non-clé`?

Dépendance transitive : `... -> ... -> ...`

Décomposition :
- `R1(...)`
- `R2(...)`

## 6. Résultat final

Lister les relations finales et leurs clés.
