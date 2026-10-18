# Guide d'architecture — Synthèse

## Côté client
`component` : interaction et présentation.  
`service` : appels API / logique partagée.  
`signal` : état réactif.  
`route` : navigation et paramètres.

## Côté serveur
`controller` : contrat HTTP.  
`repository` : accès aux données.  
`entity/model` : persistance.  
`DTO` : contrat JSON public.

## Debug full-stack
1. DevTools Network : requête envoyée?
2. URL/méthode/body corrects?
3. API reçoit la route?
4. contrôleur appelle la bonne dépendance?
5. requête BD retourne quoi?
6. statut + JSON de réponse?
7. service Angular reçoit quoi?
8. signal/vue se met à jour?
