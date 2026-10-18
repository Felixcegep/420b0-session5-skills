# Gabarit relation avec attributs

```java
@Entity
public class Ligne {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @ManyToOne
    private Parent parent;

    @ManyToOne
    private Produit produit;

    private Integer quantite;
}
```

À utiliser lorsqu'une relation entre deux entités possède ses propres données.
