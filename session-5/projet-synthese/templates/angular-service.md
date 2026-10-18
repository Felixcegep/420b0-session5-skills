# Gabarit service Angular

```ts
@Injectable({ providedIn: 'root' })
export class RessourceService {
  private http = inject(HttpClient);
  private apiUrl = `${environment.apiUrl}/ressources`;

  getAll() {
    return this.http.get<Ressource[]>(this.apiUrl);
  }
}
```

Adapter à `httpResource` ou aux patterns précis déjà utilisés dans le projet si le cours/projet les privilégie.
