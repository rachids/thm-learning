# Intro. Networking

## OSI

### Les différentes couches

- **Application:** le moyen pour les apps. de transmettre des données _(un genre d'API?)_
- **Présentation:** ramasse les données transmises par la couche Applicative, et les reformate dans un format standardisé, encrypte, compresse, etc.
- **Session:** est encharge de communiquer avec l'ordi. distant, de maintenir la communication, et de rendre cette communication unique
- **Transport:** détermine le protocole de communication et divise la données en petites pièces _(segment pour TCP, datagram pour UDP)_
- - TCP: favorisé pour la précision des données _(transfert de fichier, chargement page web)_
- - UDP: favorisé pour la vitesse
- **Réseau:** prend l'adresse IP et cherche la meilleure route pour s'y connecter
- **Liaison de données:** se concentre sur l'adresse physique de l'ordinateur (adresse MAC) et s'assure que les données n'ont pas été corrompues
- **Physique:** converti les signaux électriques en données binaires et inversement

> Astuce pour retenir:
> `A Peine Serré, Tu Rends Le Portefeuille`
> En savoir plus sur: https://jeretiens.net/couches-du-modele-osi/
