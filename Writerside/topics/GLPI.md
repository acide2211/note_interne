# GLPI

Prise de note version actuelle 9.5.4

GLPI constants
GLPI_ROOT: /var/www/html/glpi
GLPI_CONFIG_DIR: /var/www/html/glpi/config
GLPI_VAR_DIR: /var/www/html/glpi/files
GLPI_MARKETPLACE_DIR: /var/www/html/glpi/marketplace
GLPI_USE_CSRF_CHECK: 1
GLPI_CSRF_EXPIRES: 7200
GLPI_CSRF_MAX_TOKENS: 100
GLPI_USE_IDOR_CHECK: 1
GLPI_IDOR_EXPIRES: 7200
GLPI_ALLOW_IFRAME_IN_RICH_TEXT:
GLPI_TELEMETRY_URI: https://telemetry.glpi-project.org
GLPI_INSTALL_MODE: TARBALL
GLPI_NETWORK_MAIL: glpi@teclib.com
GLPI_NETWORK_SERVICES: https://services.glpi-network.com
GLPI_MARKETPLACE_PRERELEASES:
GLPI_USER_AGENT_EXTRA_COMMENTS:
GLPI_AJAX_DASHBOARD: 1
GLPI_CALDAV_IMPORT_STATE: 0
GLPI_DEMO_MODE: 0
GLPI_FORCE_EMPTY_SQL_MODE: 1
GLPI_DOC_DIR: /var/www/html/glpi/files
GLPI_CACHE_DIR: /var/www/html/glpi/files/_cache
GLPI_CRON_DIR: /var/www/html/glpi/files/_cron
GLPI_DUMP_DIR: /var/www/html/glpi/files/_dumps
GLPI_GRAPH_DIR: /var/www/html/glpi/files/_graphs
GLPI_LOCAL_I18N_DIR: /var/www/html/glpi/files/_locales
GLPI_LOCK_DIR: /var/www/html/glpi/files/_lock
GLPI_LOG_DIR: /var/www/html/glpi/files/_log
GLPI_PICTURE_DIR: /var/www/html/glpi/files/_pictures
GLPI_PLUGIN_DOC_DIR: /var/www/html/glpi/files/_plugins
GLPI_RSS_DIR: /var/www/html/glpi/files/_rss
GLPI_SESSION_DIR: /var/www/html/glpi/files/_sessions
GLPI_TMP_DIR: /var/www/html/glpi/files/_tmp
GLPI_UPLOAD_DIR: /var/www/html/glpi/files/_uploads
GLPI_NETWORK_REGISTRATION_API_URL: https://services.glpi-network.com/api/registration/
GLPI_MARKETPLACE_PLUGINS_API_URI: https://services.glpi-network.com/api/glpi-plugins/
GLPI_I18N_DIR: /var/www/html/glpi/locales
GLPI_VERSION: 9.5.4
GLPI_SCHEMA_VERSION: 9.5.4
GLPI_MIN_PHP: 7.2.0
GLPI_YEAR: 2021
#Librairie 

Informations sur le système, l'installation et la configuration
Vérifier si une nouvelle version est disponible
[code]

GLPI 9.5.4 ( => /var/www/html/glpi)
Installation mode: TARBALL

Server

Operating system: Linux esxvm31110.chbah.org 4.15.0-163-generic #171-Ubuntu SMP Fri Nov 5 11:55:11 UTC 2021 x86_64
PHP 7.2.24-0ubuntu0.18.04.10 apache2handler (Core, PDO, Phar, Reflection, SPL, SimpleXML, Zend OPcache, apache2handler, apc,
apcu, bz2, calendar, ctype, curl, date, dom, exif, fileinfo, filter, ftp, gd, gettext, hash, iconv, imap, intl, json, ldap,
libxml, mbstring, mysqli, mysqlnd, openssl, pcre, pdo_mysql, posix, readline, session, shmop, sockets, sodium, standard,
sysvmsg, sysvsem, sysvshm, tokenizer, wddx, xml, xmlreader, xmlrpc, xmlwriter, xsl, zip, zlib)
Setup: max_execution_time="60" memory_limit="128M" post_max_size="8M" safe_mode="" session.save_handler="files"
upload_max_filesize="2M"
Software: Apache/2.4.29 (Ubuntu) (Apache/2.4.29 (Ubuntu) Server at glpi.chbah.org Port 80)
Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36
Server Software: (Ubuntu)
Server Version: 5.7.36-0ubuntu0.18.04.1
Server SQL Mode:
Parameters: root@localhost/glpi
Host info: Localhost via UNIX socket

PHP version is at least 7.2.0 - Perfect!PHP version is at least 7.2.0 - Perfect!
Sessions support is available - Perfect!Sessions support is available - Perfect!
Allocated memory > 64 Mio - Perfect!Allocated memory > 64 Mio - Perfect!
mysqli extension is installedmysqli extension is installed
ctype extension is installedctype extension is installed
fileinfo extension is installedfileinfo extension is installed
json extension is installedjson extension is installed
mbstring extension is installedmbstring extension is installed
iconv extension is installediconv extension is installed
zlib extension is installedzlib extension is installed
curl extension is installedcurl extension is installed
gd extension is installedgd extension is installed
simplexml extension is installedsimplexml extension is installed
intl extension is installedintl extension is installed
ldap extension is installedldap extension is installed
apcu extension is installedapcu extension is installed
Zend OPcache extension is installedZend OPcache extension is installed
xmlrpc extension is installedxmlrpc extension is installed
CAS extension is installedCAS extension is installed
exif extension is installedexif extension is installed
zip extension is installedzip extension is installed
bz2 extension is installedbz2 extension is installed
sodium extension is installedsodium extension is installed
Database version seems correct (5.7.36) - Perfect!Database version seems correct (5.7.36) - Perfect!
Timezones seems loaded in databaseTimezones seems loaded in database
The log file has been created successfully.The log file has been created successfully.
Write access to /var/www/html/glpi/files/_cache has been validated.Write access to /var/www/html/glpi/files/_cache has been validated.
Write access to /var/www/html/glpi/config has been validated.Write access to /var/www/html/glpi/config has been validated.
Write access to /var/www/html/glpi/files/_cron has been validated.Write access to /var/www/html/glpi/files/_cron has been validated.
Write access to /var/www/html/glpi/files has been validated.Write access to /var/www/html/glpi/files has been validated.
Write access to /var/www/html/glpi/files/_dumps has been validated.Write access to /var/www/html/glpi/files/_dumps has been validated.
Write access to /var/www/html/glpi/files/_graphs has been validated.Write access to /var/www/html/glpi/files/_graphs has been validated.
Write access to /var/www/html/glpi/files/_lock has been validated.Write access to /var/www/html/glpi/files/_lock has been validated.
Write access to /var/www/html/glpi/files/_pictures has been validated.Write access to /var/www/html/glpi/files/_pictures has been validated.
Write access to /var/www/html/glpi/files/_plugins has been validated.Write access to /var/www/html/glpi/files/_plugins has been validated.
Write access to /var/www/html/glpi/files/_rss has been validated.Write access to /var/www/html/glpi/files/_rss has been validated.
Write access to /var/www/html/glpi/files/_sessions has been validated.Write access to /var/www/html/glpi/files/_sessions has been validated.
Write access to /var/www/html/glpi/files/_tmp has been validated.Write access to /var/www/html/glpi/files/_tmp has been validated.
Write access to /var/www/html/glpi/files/_uploads has been validated.Write access to /var/www/html/glpi/files/_uploads has been validated.
Write access to /var/www/html/glpi/marketplace has been validated.Write access to /var/www/html/glpi/marketplace has been validated.
Web access to the files directory should not be allowed Check the .htaccess file and the web server configuration.Web access to the files directory should not be allowed
Check the .htaccess file and the web server configuration.

GLPI constants

GLPI_ROOT: /var/www/html/glpi
GLPI_CONFIG_DIR: /var/www/html/glpi/config
GLPI_VAR_DIR: /var/www/html/glpi/files
GLPI_MARKETPLACE_DIR: /var/www/html/glpi/marketplace
GLPI_USE_CSRF_CHECK: 1
GLPI_CSRF_EXPIRES: 7200
GLPI_CSRF_MAX_TOKENS: 100
GLPI_USE_IDOR_CHECK: 1
GLPI_IDOR_EXPIRES: 7200
GLPI_ALLOW_IFRAME_IN_RICH_TEXT:
GLPI_TELEMETRY_URI: https://telemetry.glpi-project.org
GLPI_INSTALL_MODE: TARBALL
GLPI_NETWORK_MAIL: glpi@teclib.com
GLPI_NETWORK_SERVICES: https://services.glpi-network.com
GLPI_MARKETPLACE_PRERELEASES:
GLPI_USER_AGENT_EXTRA_COMMENTS:
GLPI_AJAX_DASHBOARD: 1
GLPI_CALDAV_IMPORT_STATE: 0
GLPI_DEMO_MODE: 0
GLPI_FORCE_EMPTY_SQL_MODE: 1
GLPI_DOC_DIR: /var/www/html/glpi/files
GLPI_CACHE_DIR: /var/www/html/glpi/files/_cache
GLPI_CRON_DIR: /var/www/html/glpi/files/_cron
GLPI_DUMP_DIR: /var/www/html/glpi/files/_dumps
GLPI_GRAPH_DIR: /var/www/html/glpi/files/_graphs
GLPI_LOCAL_I18N_DIR: /var/www/html/glpi/files/_locales
GLPI_LOCK_DIR: /var/www/html/glpi/files/_lock
GLPI_LOG_DIR: /var/www/html/glpi/files/_log
GLPI_PICTURE_DIR: /var/www/html/glpi/files/_pictures
GLPI_PLUGIN_DOC_DIR: /var/www/html/glpi/files/_plugins
GLPI_RSS_DIR: /var/www/html/glpi/files/_rss
GLPI_SESSION_DIR: /var/www/html/glpi/files/_sessions
GLPI_TMP_DIR: /var/www/html/glpi/files/_tmp
GLPI_UPLOAD_DIR: /var/www/html/glpi/files/_uploads
GLPI_NETWORK_REGISTRATION_API_URL: https://services.glpi-network.com/api/registration/
GLPI_MARKETPLACE_PLUGINS_API_URI: https://services.glpi-network.com/api/glpi-plugins/
GLPI_I18N_DIR: /var/www/html/glpi/locales
GLPI_VERSION: 9.5.4
GLPI_SCHEMA_VERSION: 9.5.4
GLPI_MIN_PHP: 7.2.0
GLPI_YEAR: 2021

Libraries

htmlawed/htmlawed version 1.2.5 in (/var/www/html/glpi/vendor/htmlawed/htmlawed)
phpmailer/phpmailer version 6.1.6 in (/var/www/html/glpi/vendor/phpmailer/phpmailer/src)
simplepie/simplepie version 1.5.6 in (/var/www/html/glpi/vendor/simplepie/simplepie/library)
tecnickcom/tcpdf version 6.3.5 in (/var/www/html/glpi/vendor/tecnickcom/tcpdf)
michelf/php-markdown in (/var/www/html/glpi/vendor/michelf/php-markdown/Michelf)
true/punycode in (/var/www/html/glpi/vendor/true/punycode/src)
iamcal/lib_autolink in (/var/www/html/glpi/vendor/iamcal/lib_autolink)
sabre/dav in (/var/www/html/glpi/vendor/sabre/dav/lib/DAV)
sabre/http in (/var/www/html/glpi/vendor/sabre/http/lib)
sabre/uri in (/var/www/html/glpi/vendor/sabre/uri/lib)
sabre/vobject in (/var/www/html/glpi/vendor/sabre/vobject/lib)
laminas/laminas-cache in (/var/www/html/glpi/vendor/laminas/laminas-cache/src)
laminas/laminas-i18n in (/var/www/html/glpi/vendor/laminas/laminas-i18n/src)
laminas/laminas-serializer in (/var/www/html/glpi/vendor/laminas/laminas-serializer/src)
monolog/monolog in (/var/www/html/glpi/vendor/monolog/monolog/src/Monolog)
sebastian/diff in (/var/www/html/glpi/vendor/sebastian/diff/src)
elvanto/litemoji in (/var/www/html/glpi/vendor/elvanto/litemoji/src)
symfony/console in (/var/www/html/glpi/vendor/symfony/console)
scssphp/scssphp in (/var/www/html/glpi/vendor/scssphp/scssphp/src)
laminas/laminas-mail in (/var/www/html/glpi/vendor/laminas/laminas-mail/src/Protocol)
laminas/laminas-mime in (/var/www/html/glpi/vendor/laminas/laminas-mime/src)
rlanvin/php-rrule in (/var/www/html/glpi/vendor/rlanvin/php-rrule/src)
blueimp/jquery-file-upload in (/var/www/html/glpi/vendor/blueimp/jquery-file-upload/server/php)
ramsey/uuid in (/var/www/html/glpi/vendor/ramsey/uuid/src)
psr/log in (/var/www/html/glpi/vendor/psr/log/Psr/Log)
psr/simple-cache in (/var/www/html/glpi/vendor/psr/simple-cache/src)
mexitek/phpcolors in (/var/www/html/glpi/vendor/mexitek/phpcolors/src/Mexitek/PHPColors)
guzzlehttp/guzzle in (/var/www/html/glpi/vendor/guzzlehttp/guzzle/src)
guzzlehttp/psr7 in (/var/www/html/glpi/vendor/guzzlehttp/psr7/src)
wapmorgan/unified-archive in (/var/www/html/glpi/vendor/wapmorgan/unified-archive/src)
paragonie/sodium_compat in (/var/www/html/glpi/vendor/paragonie/sodium_compat/src)
phpCas version 1.3.3 in (/usr/share/php)
#LAPD


Informations sur le système, l'installation et la configuration
Vérifier si une nouvelle version est disponible
[code]

GLPI 9.5.4 ( => /var/www/html/glpi)
Installation mode: TARBALL

Server

Operating system: Linux esxvm31110.chbah.org 4.15.0-163-generic #171-Ubuntu SMP Fri Nov 5 11:55:11 UTC 2021 x86_64
PHP 7.2.24-0ubuntu0.18.04.10 apache2handler (Core, PDO, Phar, Reflection, SPL, SimpleXML, Zend OPcache, apache2handler, apc,
apcu, bz2, calendar, ctype, curl, date, dom, exif, fileinfo, filter, ftp, gd, gettext, hash, iconv, imap, intl, json, ldap,
libxml, mbstring, mysqli, mysqlnd, openssl, pcre, pdo_mysql, posix, readline, session, shmop, sockets, sodium, standard,
sysvmsg, sysvsem, sysvshm, tokenizer, wddx, xml, xmlreader, xmlrpc, xmlwriter, xsl, zip, zlib)
Setup: max_execution_time="60" memory_limit="128M" post_max_size="8M" safe_mode="" session.save_handler="files"
upload_max_filesize="2M"
Software: Apache/2.4.29 (Ubuntu) (Apache/2.4.29 (Ubuntu) Server at glpi.chbah.org Port 80)
Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36
Server Software: (Ubuntu)
Server Version: 5.7.36-0ubuntu0.18.04.1
Server SQL Mode:
Parameters: root@localhost/glpi
Host info: Localhost via UNIX socket

PHP version is at least 7.2.0 - Perfect!PHP version is at least 7.2.0 - Perfect!
Sessions support is available - Perfect!Sessions support is available - Perfect!
Allocated memory > 64 Mio - Perfect!Allocated memory > 64 Mio - Perfect!
mysqli extension is installedmysqli extension is installed
ctype extension is installedctype extension is installed
fileinfo extension is installedfileinfo extension is installed
json extension is installedjson extension is installed
mbstring extension is installedmbstring extension is installed
iconv extension is installediconv extension is installed
zlib extension is installedzlib extension is installed
curl extension is installedcurl extension is installed
gd extension is installedgd extension is installed
simplexml extension is installedsimplexml extension is installed
intl extension is installedintl extension is installed
ldap extension is installedldap extension is installed
apcu extension is installedapcu extension is installed
Zend OPcache extension is installedZend OPcache extension is installed
xmlrpc extension is installedxmlrpc extension is installed
CAS extension is installedCAS extension is installed
exif extension is installedexif extension is installed
zip extension is installedzip extension is installed
bz2 extension is installedbz2 extension is installed
sodium extension is installedsodium extension is installed
Database version seems correct (5.7.36) - Perfect!Database version seems correct (5.7.36) - Perfect!
Timezones seems loaded in databaseTimezones seems loaded in database
The log file has been created successfully.The log file has been created successfully.
Write access to /var/www/html/glpi/files/_cache has been validated.Write access to /var/www/html/glpi/files/_cache has been validated.
Write access to /var/www/html/glpi/config has been validated.Write access to /var/www/html/glpi/config has been validated.
Write access to /var/www/html/glpi/files/_cron has been validated.Write access to /var/www/html/glpi/files/_cron has been validated.
Write access to /var/www/html/glpi/files has been validated.Write access to /var/www/html/glpi/files has been validated.
Write access to /var/www/html/glpi/files/_dumps has been validated.Write access to /var/www/html/glpi/files/_dumps has been validated.
Write access to /var/www/html/glpi/files/_graphs has been validated.Write access to /var/www/html/glpi/files/_graphs has been validated.
Write access to /var/www/html/glpi/files/_lock has been validated.Write access to /var/www/html/glpi/files/_lock has been validated.
Write access to /var/www/html/glpi/files/_pictures has been validated.Write access to /var/www/html/glpi/files/_pictures has been validated.
Write access to /var/www/html/glpi/files/_plugins has been validated.Write access to /var/www/html/glpi/files/_plugins has been validated.
Write access to /var/www/html/glpi/files/_rss has been validated.Write access to /var/www/html/glpi/files/_rss has been validated.
Write access to /var/www/html/glpi/files/_sessions has been validated.Write access to /var/www/html/glpi/files/_sessions has been validated.
Write access to /var/www/html/glpi/files/_tmp has been validated.Write access to /var/www/html/glpi/files/_tmp has been validated.
Write access to /var/www/html/glpi/files/_uploads has been validated.Write access to /var/www/html/glpi/files/_uploads has been validated.
Write access to /var/www/html/glpi/marketplace has been validated.Write access to /var/www/html/glpi/marketplace has been validated.
Web access to the files directory should not be allowed Check the .htaccess file and the web server configuration.Web access to the files directory should not be allowed
Check the .htaccess file and the web server configuration.

GLPI constants

GLPI_ROOT: /var/www/html/glpi
GLPI_CONFIG_DIR: /var/www/html/glpi/config
GLPI_VAR_DIR: /var/www/html/glpi/files
GLPI_MARKETPLACE_DIR: /var/www/html/glpi/marketplace
GLPI_USE_CSRF_CHECK: 1
GLPI_CSRF_EXPIRES: 7200
GLPI_CSRF_MAX_TOKENS: 100
GLPI_USE_IDOR_CHECK: 1
GLPI_IDOR_EXPIRES: 7200
GLPI_ALLOW_IFRAME_IN_RICH_TEXT:
GLPI_TELEMETRY_URI: https://telemetry.glpi-project.org
GLPI_INSTALL_MODE: TARBALL
GLPI_NETWORK_MAIL: glpi@teclib.com
GLPI_NETWORK_SERVICES: https://services.glpi-network.com
GLPI_MARKETPLACE_PRERELEASES:
GLPI_USER_AGENT_EXTRA_COMMENTS:
GLPI_AJAX_DASHBOARD: 1
GLPI_CALDAV_IMPORT_STATE: 0
GLPI_DEMO_MODE: 0
GLPI_FORCE_EMPTY_SQL_MODE: 1
GLPI_DOC_DIR: /var/www/html/glpi/files
GLPI_CACHE_DIR: /var/www/html/glpi/files/_cache
GLPI_CRON_DIR: /var/www/html/glpi/files/_cron
GLPI_DUMP_DIR: /var/www/html/glpi/files/_dumps
GLPI_GRAPH_DIR: /var/www/html/glpi/files/_graphs
GLPI_LOCAL_I18N_DIR: /var/www/html/glpi/files/_locales
GLPI_LOCK_DIR: /var/www/html/glpi/files/_lock
GLPI_LOG_DIR: /var/www/html/glpi/files/_log
GLPI_PICTURE_DIR: /var/www/html/glpi/files/_pictures
GLPI_PLUGIN_DOC_DIR: /var/www/html/glpi/files/_plugins
GLPI_RSS_DIR: /var/www/html/glpi/files/_rss
GLPI_SESSION_DIR: /var/www/html/glpi/files/_sessions
GLPI_TMP_DIR: /var/www/html/glpi/files/_tmp
GLPI_UPLOAD_DIR: /var/www/html/glpi/files/_uploads
GLPI_NETWORK_REGISTRATION_API_URL: https://services.glpi-network.com/api/registration/
GLPI_MARKETPLACE_PLUGINS_API_URI: https://services.glpi-network.com/api/glpi-plugins/
GLPI_I18N_DIR: /var/www/html/glpi/locales
GLPI_VERSION: 9.5.4
GLPI_SCHEMA_VERSION: 9.5.4
GLPI_MIN_PHP: 7.2.0
GLPI_YEAR: 2021

Libraries

htmlawed/htmlawed version 1.2.5 in (/var/www/html/glpi/vendor/htmlawed/htmlawed)
phpmailer/phpmailer version 6.1.6 in (/var/www/html/glpi/vendor/phpmailer/phpmailer/src)
simplepie/simplepie version 1.5.6 in (/var/www/html/glpi/vendor/simplepie/simplepie/library)
tecnickcom/tcpdf version 6.3.5 in (/var/www/html/glpi/vendor/tecnickcom/tcpdf)
michelf/php-markdown in (/var/www/html/glpi/vendor/michelf/php-markdown/Michelf)
true/punycode in (/var/www/html/glpi/vendor/true/punycode/src)
iamcal/lib_autolink in (/var/www/html/glpi/vendor/iamcal/lib_autolink)
sabre/dav in (/var/www/html/glpi/vendor/sabre/dav/lib/DAV)
sabre/http in (/var/www/html/glpi/vendor/sabre/http/lib)
sabre/uri in (/var/www/html/glpi/vendor/sabre/uri/lib)
sabre/vobject in (/var/www/html/glpi/vendor/sabre/vobject/lib)
laminas/laminas-cache in (/var/www/html/glpi/vendor/laminas/laminas-cache/src)
laminas/laminas-i18n in (/var/www/html/glpi/vendor/laminas/laminas-i18n/src)
laminas/laminas-serializer in (/var/www/html/glpi/vendor/laminas/laminas-serializer/src)
monolog/monolog in (/var/www/html/glpi/vendor/monolog/monolog/src/Monolog)
sebastian/diff in (/var/www/html/glpi/vendor/sebastian/diff/src)
elvanto/litemoji in (/var/www/html/glpi/vendor/elvanto/litemoji/src)
symfony/console in (/var/www/html/glpi/vendor/symfony/console)
scssphp/scssphp in (/var/www/html/glpi/vendor/scssphp/scssphp/src)
laminas/laminas-mail in (/var/www/html/glpi/vendor/laminas/laminas-mail/src/Protocol)
laminas/laminas-mime in (/var/www/html/glpi/vendor/laminas/laminas-mime/src)
rlanvin/php-rrule in (/var/www/html/glpi/vendor/rlanvin/php-rrule/src)
blueimp/jquery-file-upload in (/var/www/html/glpi/vendor/blueimp/jquery-file-upload/server/php)
ramsey/uuid in (/var/www/html/glpi/vendor/ramsey/uuid/src)
psr/log in (/var/www/html/glpi/vendor/psr/log/Psr/Log)
psr/simple-cache in (/var/www/html/glpi/vendor/psr/simple-cache/src)
mexitek/phpcolors in (/var/www/html/glpi/vendor/mexitek/phpcolors/src/Mexitek/PHPColors)
guzzlehttp/guzzle in (/var/www/html/glpi/vendor/guzzlehttp/guzzle/src)
guzzlehttp/psr7 in (/var/www/html/glpi/vendor/guzzlehttp/psr7/src)
wapmorgan/unified-archive in (/var/www/html/glpi/vendor/wapmorgan/unified-archive/src)
paragonie/sodium_compat in (/var/www/html/glpi/vendor/paragonie/sodium_compat/src)
phpCas version 1.3.3 in (/usr/share/php)

LDAP directories

Server: '128.30.30.101', Port: '389', BaseDN: 'OU=Membres CHBA,OU=Utilisateurs du Domaine,DC=CHBAH,DC=ORG', Connection filter:
'(&(objectClass=user)(memberof=CN=g_Users_GLPI,OU=Membres CHBA,OU=Utilisateurs du Domaine,DC=CHBAH,DC=ORG))', RootDN:
'cn=AppWeb_ldap,ou=Admin LDAP,ou=Utilisateurs du Domaine,dc=CHBAH,dc=ORG', Use TLS: none


#MAIL
Name: 'support@chbah.org' Active: Yes
Server: '{mail.chbah.org:993/imap/ssl/novalidate-cert/debug}' Login: 'support@chbah.org' Password: Yes
#Pluging list

	archires             Name: Architectures réseau           Version: 2.3        State: Not installed
	pdf                  Name: Impression pdf                 Version: 1.4.0      State: Installed / not activated
	ocsinventoryng       Name: OCS Inventory NG               Version: 1.3.3      State: Installed / not activated

#Mysql DB
dbhos = localhost
dbuser  root
dbpassword toscane
dbdefault glpi

mysql -u root -p glpi
select user,host from mysql.user;
mysqldump -u [utilisateur] -p[mdp] nom_de_la_base > sauvegarde.sql;
mysqldump -u root -p glpi > sauvegarde_ad.sql


Linux Alain Donsin01
glpi 95.

tar -cvf glip.tar /var/www/glip

https://pellenalexandre.wordpress.com/2018/02/19/serveur-glpi/
sudo apt update -y && upgrade -y

apt-get install php
apt-get install apache2
apt-get install mysql-serveur
Master password root
mysql> CREATE DATABASE glpi; #Création de la base de donnée "glpi"
mysql> CREATE USER 'glpi'@'localhost'; #Création de l'utilisateur "glpi"
mysql> GRANT ALL PRIVILEGES ON glpi.* TO 'glpi'@'localhost' IDENTIFIED BY 'password'; #Dont des privileges à l'utilisateur "glpi" sur la bdd "glpi"
mysql> FLUSH PRIVILEGES;


sudo apt-get install open-vm-tools-desktop

