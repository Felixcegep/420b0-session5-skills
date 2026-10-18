# Tests et CI

## Service Angular avec HTTP
- `provideHttpClient()`
- `provideHttpClientTesting()`
- injecter `HttpTestingController`
- `expectOne(url)`
- vérifier méthode HTTP
- `flush(...)`
- `verify()` après test

## Routage
`RouterTestingHarness` pour simuler la navigation et vérifier composant, paramètres et rendu.

## CI
Le fichier `.gitlab-ci.yml` doit être lu comme une suite de jobs. Lors d'un échec : job → commande → première vraie erreur.
