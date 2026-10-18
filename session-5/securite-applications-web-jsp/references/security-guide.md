# Sécurité — démarche

## Authentification vs autorisation
- Authentification : qui est l'utilisateur?
- Autorisation : a-t-il le droit d'effectuer cette action?

## Ordre de diagnostic 403
1. utilisateur authentifié?
2. rôle/authority attendu?
3. route autorisée dans SecurityFilterChain?
4. méthode HTTP correcte?
5. CSRF en cause?
6. contrôle `@PreAuthorize` ou similaire?

## API tokens
Ne jamais considérer « JWT présent » comme suffisant : vérifier signature, expiration, claims utiles et autorisation côté serveur.
