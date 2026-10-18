# Gabarit MVC

```java
@Controller
@RequestMapping("/ressources")
public class RessourceController {
    private final RessourceService service;

    public RessourceController(RessourceService service) {
        this.service = service;
    }

    @GetMapping
    public String index(Model model) {
        model.addAttribute("ressources", service.findAll());
        return "ressources/index";
    }
}
```

Le contrôleur orchestre; la logique métier va dans le service.
