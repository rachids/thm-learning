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

## `dig`

### DNS

En faisant une requête, l'ordi contacte un DNS qui lui retourne une IP afin d'établir la communication.

#### Recursive DNS Server

Lorsque le DNS ne trouve pas l'IP associé il délégue au _recursive DNS server_ 
Ces serveurs maintiennent un cache.

#### Root Name Server

Si le recursive DNS server n'a pas trouvé non plus, alors la demande est déléguée au _root name server_.
Son rôle est de rediriger la requête vers le "next level down", en premier lieu : le Top Level Domain.

#### Top Level Domain Server

Chaque serveur est dédié à un nom de domaine en particulier _(ex: `.com`, `.ca`, `.fr`, etc)_
Il conserve les informations du "next level down", le Authoritative Name Server.

#### Authoritative Name Server

L'Authoritative Name Server consigne les enregistrements DNS des domaines. 
Ce sont les infos que l'on renseigne sur nos domaines, ex:
`rachids.ca.             0       IN      A       109.234.164.40`
Quand la requête atteint ce serveur, il lui répond par l'adresse IP associée au domaine de la requête et ainsi l'ordinateur peut établir la communication.
