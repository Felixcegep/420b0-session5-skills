# Guide rapide JSP/Spring

## Flux MVC
requête HTTP → Controller → Service → Repository → BD
                         ↓
                       Model → JSP

## API
requête HTTP → RestController → Service → Repository → BD
                     ↓
                 DTO / JSON

## Choix des annotations
- `@Controller` : vue MVC.
- `@RestController` : données, généralement JSON.
- `@RequestParam` : paramètre de requête/formulaire simple.
- `@PathVariable` : valeur dans l'URL.
- `@ModelAttribute` : liaison d'un objet de formulaire.
- `@RequestBody` : objet provenant d'un corps HTTP JSON.
- `@Transactional` : opération métier qui doit rester atomique lors de modifications coordonnées.
