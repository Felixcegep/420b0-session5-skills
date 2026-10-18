# Angular — guide rapide

## Génération
Utiliser Angular CLI (`ng generate`) lorsque possible pour rester cohérent avec la structure du projet.

## Parent/enfant
- entrée : `input<T>()`;
- sortie : `output<T>()`;
- événement capturé avec `$event` dans le parent.

## Formulaires
Le cours priorise les formulaires avec signaux : modèle `signal`, `form(...)`, `[formField]`, validation de schéma, `submit(...)`.

## Intercepteurs
Configurer via `provideHttpClient(withInterceptors([...]))`.
