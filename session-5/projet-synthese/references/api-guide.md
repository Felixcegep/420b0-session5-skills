# API ASP.NET — guide rapide

## Contrôleur
- `[ApiController]`
- `[Route("api/[controller]")]`
- `ControllerBase`
- action HTTP appropriée
- `ActionResult<T>` si plusieurs statuts possibles

## Codes communs
- lecture réussie : 200
- création : 201
- suppression sans contenu : 204
- inexistant : 404
- entrée invalide : 400

## DTO
Utiliser des DTO pour casser les cycles EF et définir un contrat client propre.
