# GLPI Installation

sudo apt install apache2

Pour info
<VirtualHost *:80>
    ServerName glpi.localhost

    DocumentRoot /var/www/glpi/public

    # If you want to place GLPI in a subfolder of your site (e.g. your virtual host is serving multiple applications),
    # you can use an Alias directive. If you do this, the DocumentRoot directive MUST NOT target the GLPI directory itself.
    # Alias "/glpi" "/var/www/glpi/public"

    <Directory /var/www/glpi/public>
        Require all granted

        RewriteEngine On

        # Redirect all requests to GLPI router, unless file exists.
        RewriteCond %{REQUEST_FILENAME} !-f
        RewriteRule ^(.*)$ index.php [QSA,L]
    </Directory>
</VirtualHost>


On pourrais passer de php 8 à 9 voir 10 mais un a un
bUser root  
dbPassword GLPI
https /// IP /glpi
mysql -u root -p wordpress < wordpress.sql

php Attention
sudo add-apt-repository ppa:ondrej/php
sudo apt-get install -y php8.2sud

Crée le fichier apache config

apachectl configtest


configurer le fichier dans le sites available.
Puis checl-k la configuration avec apachectl
activer le site sudo a2ensite glpi.cong
service apache2 
reloadhttps://ubunlog.com/fr/php-8-0-instalar-lenguaje-en-ubuntu/?utm_source=dlvr.it&utm_medium=facebook

# Nouvelle installatiin
Login alain
Pwd : alain

sudo apt update && apt upgrade
sudo add-apt-repository ppa:ondrej/php //Peut etre inutile
sudo apt install apache2
sudo apt install mysql-server
sudo apt install libapache2-mod-php7.2
sudo add-apt-repository ppa:ondrej/php //Pour forcer php 7

PHP 7 Pro
sudo apt-get install software-properties-common python-software-properties;
sudo add-apt-repository -y ppa:ondrej/php;
sudo apt-get update;

#Mysql DB
dbhos = localhost
dbuser  root
dbpassword toscane
dbdefault glpi