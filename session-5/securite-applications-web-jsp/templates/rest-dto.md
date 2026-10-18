# Gabarit REST + DTO

```java
@RestController
@RequestMapping("/api/ressources")
public class RessourceRestController {
    private final RessourceService service;

    @GetMapping
    public List<RessourceDTO> findAll() {
        return service.findAllDto();
    }
}
```

DTO de sortie : expose uniquement les champs utiles au client.  
Request DTO : représente les données acceptées en entrée.
