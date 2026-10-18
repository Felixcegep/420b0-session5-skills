# Checklist — Sécurité client/serveur

## Client
- aucune clé/secrète sensible en dur;
- données non fiables validées;
- informations sensibles non exposées inutilement;
- erreurs sans fuite d'informations.

## Serveur
- authentification vérifiée côté serveur;
- autorisation vérifiée pour chaque ressource/action;
- requêtes paramétrées;
- validation côté serveur;
- secrets hors du code source;
- permissions minimales;
- erreurs et logs appropriés.

## Communication
- TLS lorsque requis;
- certificat validé;
- aucune donnée sensible envoyée en clair;
- intégrité et authenticité des échanges prises en compte.

## Rapport
- vulnérabilité;
- emplacement/preuve;
- risque/impact;
- sévérité justifiée;
- correction;
- test de validation après correction.
