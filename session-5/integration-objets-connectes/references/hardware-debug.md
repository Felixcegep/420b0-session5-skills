# Débogage matériel

## GPIO busy
- chercher les processus Python actifs;
- vérifier les services qui utilisent la broche;
- arrêter proprement l'ancien processus;
- éviter de lancer deux copies du même programme.

## I2C
- SDA/SCL correctement câblés;
- masse commune;
- I2C activé;
- périphérique visible sur le bus;
- adresse cohérente avec la bibliothèque.

## Actionneurs
Un GPIO est une broche logique, pas une alimentation pour moteur. Pour une pompe ou moteur, penser étage de puissance, masse commune, alimentation adaptée et protection contre les charges inductives.
