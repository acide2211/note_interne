# GLPI
GLPI2
sudo apt update
sudo apt install apache2
sudo apt install mariadb-servers
sudo apt install php
sudo apt install apache2 mariadb-server php php-mysql php-gd php-ldap php-xml php-mbstring php-curl php-zip php-intl php-json php-apcu

sudo mysql_secure_installation
sudo mysql -u root -p
glpi
// glpiuser

dbhos = localhost
dbuser  root
dbpassword toscane
dbdefault glpi

CREATE DATABASE glpi CHARACTER SET utf8 COLLATE utf8_general_ci;
CREATE USER 'glpiuser'@'localhost' IDENTIFIED BY 'votre_mot_de_passe'; glpi
GRANT ALL PRIVILEGES ON glpi.* TO 'glpiuser'@'localhost';
FLUSH PRIVILEGES;
EXIT;

//Version avec php 7
wget https://github.com/glpi-project/glpi/releases/download/9.4.0/glpi-9.4.0.tgz

tar -zxvf glpi-9.4.0.tgz
sudo mv glpi /var/www/html/

//Version avec  php compatible
wget https://github.com/glpi-project/glpi/releases/download/9.5.0/glpi-9.5.0.tgz
tar -zxvf glpi-9.5.0.tgz
sudo mv glpi /var/www/html/

// Derniere version 10.0.10

sudo nano /etc/apache2/sites-available/glpi.conf
wget https://github.com/glpi-project/glpi/releases/download/10.0.10/glpi-10.0.10.tgz

tar -zxvf glpi-10.0.10.tgz
sudo mv glpi /var/www/html/

cd /etc/apache2/sites-availlable
sudo cp 000-default.conf glpi.conf


<VirtualHost *:80>
    ServerAdmin webmaster@example.com
    DocumentRoot /var/www/html/glpi
    ServerName your_domain_or_IP
    <Directory /var/www/html/glpi>
        Options FollowSymlinks
        AllowOverride All
        Require all granted
    </Directory>
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

<VirtualHost *:80>
    ServerAdmin webmaster@example.com
    DocumentRoot /var/www/html/glpi
    ServerName your_domain_or_IP
    <Directory /var/www/html/glpi>
        Options FollowSymlinks
        AllowOverride All
        Require all granted
    </Directory>
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

sudo a2ensite glpi.conf
sudo systemctl restart apache2

http://your_domain_or_IP/glpi

Site en ligne

// Importer la db

mysql -u glpiuser -p glpi < sauvergarde_ad.sql

Hello,
This is a new install on Ubuntu 18.04 LTS and GLPI 9.5.4.  When I try to access the webserver at x.x.x.x/glpi/install.php I get a 404 not found error. These are the instructions that I used to install. Any help would be appreciated.

Step 1:Update Ubuntu
As usual, ensure your packages list is up to date.

sudo apt update
You can also upgrade installed packages by running the following command.

sudo apt -y upgrade
Step 2: Install MariaDB database server
GLPI requires a relational database to store its data. Let’s install MariaDB on Ubuntu 18.04 by using our guide:

How to Install MariaDB on Ubuntu 18.04

After the installation, Login to your database as root user.

$ mysql -u root -p
Create a database and user for GLPI.

CREATE DATABASE glpi;
CREATE USER 'glpi'@'localhost' IDENTIFIED BY 'StrongDBPassword';
GRANT ALL PRIVILEGES ON glpi.* TO 'glpi'@'localhost';
FLUSH PRIVILEGES;
exit;
Step 2: Install PHP and Apache
We need to have Apache web server and PHP installed for GLPI to run and be accessed from a web interface.

sudo apt-get -y install php php-{curl,gd,imagick,intl,apcu,recode,memcache,imap,mysql,cas,ldap,tidy,pear,xmlrpc,pspell,gettext,mbstring,json,iconv,xml,gd,xsl}
Then install Apache and its PHP module.

sudo apt-get -y install apache2 libapache2-mod-php
Step 3: Download and Install GLPI
Download the latest stable release of GLPI. It follows a semantic versioning scheme, on 3 digits, where the first one is the major release, the second the minor and the third the fix release.



Uncompress the downloaded the archive

tar xvf glpi-$VER.tgz
Move the created glpi folder to the /srv directory.

sudo mv glpi /srv/
Give Apache user ownership of the directory

sudo chown -R www-data:www-data /srv/glpi/
Step 4: Finish GLPI installation


Start typing here...