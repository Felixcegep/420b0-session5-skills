# Gabarit formulaire avec signaux

```ts
model = signal<Ressource>({
  id: 0,
  nom: ''
});

ressourceForm = form(this.model, (schema) => {
  required(schema.nom, { message: 'Le champ est requis' });
});

onSubmit(event: Event) {
  event.preventDefault();
  submit(this.ressourceForm, async () => {
    // appel service
  });
}
```
