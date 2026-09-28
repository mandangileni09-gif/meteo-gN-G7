1. Quel équipement ajoute l'horodatage à une mesure ? Pourquoi pas l'Arduino ?
C'est la passerelle qui ajoute l'horodatage. L'Arduino Uno n'a pas d'horloge temps réel

2. Pourquoi les horodatages sont-ils enregistrés en heure UTC plutôt qu'en heure locale ?
L'UTC est une référence unique, sans changement d'heure. En heure locale, le passage heure d'été à heure d'hiver crée une heure en double ou manquante.

3. Que fait la passerelle si l'API ne répond pas ? Quel risque cela couvre-t-il ?
Elle conserve les mesures en local et les renvoie plus tard, quand l'API est de nouveau joignable. Cela couvre le risque de perte de données lors d'une panne de l'API.

4. Pourquoi une station ne peut-elle pas joindre le VLAN UTILISATEURS ?
Une station n'a aucun besoin de communiquer avec les postes utilisateurs : elle n'envoie ses mesures qu'au serveur HTTP 80 et HTTPS 443.

5. Votre groupe partage une Raspberry avec un autre groupe. Citez trois éléments qui vous en isolent.


6. Quelle différence faites-vous entre une réplication et une sauvegarde ?
La réplication maintient une copie de la base à jour presque en continu sur une autre machine