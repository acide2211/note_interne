# NextCloud

https://docs.nextcloud.com/server/latest/admin_manual/installation/example_ubuntu.html


sudo apt update && sudo apt upgrade
sudo apt install apache2 mariadb-server libapache2-mod-php php-gd php-mysql \
php-curl php-mbstring php-intl php-gmp php-bcmath php-xml php-imagick php-zip


## Creation de la db
sudo mysql

CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
CREATE DATABASE IF NOT EXISTS nextcloud CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
GRANT ALL PRIVILEGES ON nextcloud.* TO 'username'@'localhost';
FLUSH PRIVILEGES;

sudo mysql

CREATE USER 'nextcloud'@'localhost' IDENTIFIED BY 'nextcloud';
CREATE DATABASE IF NOT EXISTS nextcloud CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
GRANT ALL PRIVILEGES ON nextcloud.* TO 'nextcloud'@'localhost';
FLUSH PRIVILEGES;

## Installation de l'image next cloud
Telecharger le fichier
https://nextcloud.com/changelog/

__De Base __
```bash
wget https://download.nextcloud.com/server/releases/nextcloud-x.y.z.tar.bz2.asc
wget https://nextcloud.com/nextcloud.asc
gpg --import nextcloud.asc
gpg --verify nextcloud-x.y.z.tar.bz2.asc nextcloud-x.y.z.tar.bz2
```
__Realiser pour la derniere version __
```bash
wget https://download.nextcloud.com/server/releases/nextcloud-28.0.0.tar.bz2.asc
wget https://nextcloud.com/nextcloud.asc
gpg --import nextcloud.asc
gpg --verify nextcloud-28.0.0.tar.bz2.asc nextcloud-28.0.0.tar.bz2
```

Dezzipper l'archive
```bash
tar -xjvf nextcloud-28.0.0.tar.bz2
```

Copier vers notre dossier sirz web
```bash
sudo cp -r nextcloud /var/www
```

Changer le propriétaire du fichier pour que apache puisse utiliser
```bash
sudo chown -R www-data:www-data /var/www/nextcloud
```

Configuration apache

<VirtualHost *:80>
  DocumentRoot /var/www/html/nextcloud/
  ServerName  your.server.com

  <Directory /var/www/html/nextcloud/>
    Require all granted
    AllowOverride All
    Options FollowSymLinks MultiViews

    <IfModule mod_dav.c>
      Dav off
    </IfModule>

  </Directory>
</VirtualHost>

### Installer reellement premiere version

<VirtualHost *:80>
        # The ServerName directive sets the request scheme, hostname and port that
        # the server uses to identify itself. This is used when creating
        # redirection URLs. In the context of virtual hosts, the ServerName
        # specifies what hostname must appear in the request's Host: header to
        # match this virtual host. For the default virtual host (this file) this
        # value is not decisive as it is used as a last resort host regardless.
        # However, you must set it for any further virtual host explicitly.
        #ServerName www.example.com

        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html/nextcloud

        <Directory /var/www/html/nextcloud/>
                Require all granted
                AllowOverride All
                 Options FollowSymLinks MultiViews

                 <IfModule mod_dav.c>
                        Dav off
                </IfModule>

        </Directory>


        # Available loglevels: trace8, ..., trace1, debug, info, notice, warn,
        # error, crit, alert, emerg.
        # It is also possible to configure the loglevel for particular
        # modules, e.g.
        #LogLevel info ssl:warn

        ErrorLog ${APACHE_LOG_DIR}/nextcloud_error.log
        CustomLog ${APACHE_LOG_DIR}/nexcloutaccess.log combined

        # For most configuration files from conf-available/, which are
        # enabled or disabled at a global level, it is possible to
        # include a line for only one particular virtual host. For example the
        # following line enables the CGI configuration for this host only
        # after it has been globally disabled with "a2disconf".
        #Include conf-available/serve-cgi-bin.conf
</VirtualHost>

Activation du site
```bash
a2sensite 001-nextcloud.conf
systemctl reload apache2
systemctl status apache2

```

Le site n'arrivais jamais malgre l'adresse le dossier n'était pas dans le bon répertoire
Alain
Donsin01
