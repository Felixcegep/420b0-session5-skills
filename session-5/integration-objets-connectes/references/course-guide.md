# Guide du cours — 420-5P0

## Axes à maîtriser
- Raspberry Pi / Linux et exécution de programmes Python.
- Capteurs et actionneurs.
- GPIO numériques.
- Bus de communication comme I2C lorsque requis par un capteur.
- Acquisition de données à plusieurs périodicités.
- Python et concurrence/asynchronisme.
- Architecture IoT distribuée.
- MQTT : broker, publisher, subscriber, topic, payload.
- Mosquitto et outils de test en ligne de commande.
- Paho MQTT côté Python.
- Sérialisation JSON et horodatage.
- Diagnostic intégré matériel + logiciel + réseau.

## Méthode mentale
Une valeur de capteur suit typiquement :

capteur → bibliothèque/driver → programme Python → transformation → message → broker MQTT → subscriber → affichage/stockage/décision.

Pour trouver un bug, tester la chaîne dans cet ordre plutôt que modifier plusieurs couches à la fois.

## Périodicités
Créer une tâche indépendante par responsabilité lorsque les intervalles sont différents. Une exigence « toutes les 1 min » doit être traçable vers le code qui attend ou planifie 60 s, et non cachée dans une boucle générale arbitraire.
