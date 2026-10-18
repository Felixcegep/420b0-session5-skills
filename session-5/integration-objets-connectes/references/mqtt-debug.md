# Débogage MQTT

## Checklist rapide
1. Broker démarré?
2. Bonne IP/hostname?
3. Port accessible?
4. Publisher connecté?
5. Subscriber connecté?
6. Topics identiques?
7. Payload valide?
8. Boucle réseau active?

## Outils Mosquitto
Subscriber :
```bash
mosquitto_sub -h <broker> -p 1883 -t 'mon/topic' -v
```

Tous les sous-topics d'un préfixe :
```bash
mosquitto_sub -h <broker> -p 1883 -t 'mon/#' -v
```

Publication de test :
```bash
mosquitto_pub -h <broker> -p 1883 -t 'mon/topic' -m '{"valeur":42}'
```

## Paho MQTT
Le client doit laisser la boucle réseau tourner. Avec un programme qui exécute d'autres tâches, `loop_start()` est souvent pratique; avec un client dédié, `loop_forever()` peut suffire.

Toujours distinguer : erreur de connexion, publication non envoyée, mauvais topic et subscriber absent.
