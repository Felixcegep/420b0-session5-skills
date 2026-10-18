# Gabarit tâches périodiques

```python
import asyncio

async def capteur_rapide():
    while True:
        # lire + publier
        await asyncio.sleep(60)

async def capteur_lent():
    while True:
        # lire + publier
        await asyncio.sleep(600)

async def main():
    await asyncio.gather(
        capteur_rapide(),
        capteur_lent(),
    )

asyncio.run(main())
```

Une tâche = une responsabilité/périodicité lorsque cela rend les exigences plus faciles à tracer.
