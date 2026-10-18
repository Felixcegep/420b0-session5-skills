# Gabarit Paho MQTT

```python
import json
from datetime import datetime, timezone
import paho.mqtt.client as mqtt

BROKER = "localhost"
PORT = 1883
TOPIC = "projet/capteur"

client = mqtt.Client(client_id="client-unique")
client.connect(BROKER, PORT, 60)
client.loop_start()

payload = {
    "valeur": 0,
    "horodatage": datetime.now(timezone.utc).isoformat()
}
client.publish(TOPIC, json.dumps(payload))
```

Adapter la version de l'API Paho aux dépendances réellement utilisées dans le projet.
