# rocketchat

## Explication des services

| Services  | Snap Service name | Systemd Service Name|
|-----------|-------------------|
| MongoDB    | rocketchat-mongo  | snap.rocketchat-server.rocketchat-mongo  
| Caddy      | rocketchat-caddy| snap.rocketchat-server.rocketchat.caddy
Rocket.Chat | rocketchat-server | snap.rocketchat-server.rocketchat-server             |

##Les Log
sudo snap logs -f rocketchat-server.rocketchat-server
sudo snap logs -f rocketchat-server.rocketchat-mongo
sudo snap logs -f rocketchat-server.rocketchat-caddy


## Les dossiers francais
* Vos fichiers instantanés réels pour chaque version de Rocket.Chat sont copier dans : /var/lib/snapd/snaps et il est monté en read-only mode

* Votre répertoire commun Snap est : var/snap/rocketchat-server/coman/ ; les téléchargements de fichiers sur le disque et la base de données sont stockés ici.

* Votre répertoire de données Snap est /var/snap/rocketchat-server/<versionS ; il s'agit d'un dossier versionné.
* Vous pouvez accèder au répertoire actuel des données Snap à l'adresse /var/snap/rocketchat-server/current.

## Les dossiers anglais
* Your actual snap files for each version of Rocket.Chat are copied to: /var/lib/snapd/snaps and they are mounted in read-only mode.
* Your snap common directory is: /var/snap/rocketchat-server/common/; file uploads to disk and the database are stored here.
* Your snap data directory is /var/snap/rocketchat-server/<version>; this is a versioned folder.
  You can access the current snap data directory at /var/snap/rocketchat-server/current.


:/snap/rocketchat-server/1597$ mongo sh

/var/snap/rocketchat-server/current/mongod.conf.

![config 2.png](config 2.png)

# Ajout de mon ip
![mongodb.confpng](mongodb.confpng)

Sa a merder
sudo service snap.rocketchat-server.rocketchat-mongo restart

Si on ajoute une ip sa plante mais la 0.0.0.0 sa accept


Start typing here...