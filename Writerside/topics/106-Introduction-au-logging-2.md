# 106 -Introduction au logging 2
Depuis le début du cours, tous les affichages dans la console sont effectues dans la console en utilisant l'instruction System.out.println(). Cette approche est asszz limitée et il est possible de faire mieux grâce au librairies de **logging**
##Qu'est-ce que le loggin?
Le **logging** constiste à ajouter des traitements dans les applications pour permettre l'émission de le stockage de messages suite à des évenements.</p>

Une **API de logging** fait généralement intervenr trois composants principaux :

Logger : invoqué pour émettre grâce au framework un message généralement avec un **niveau de gravité** associé.

* Formatter : utiliser pour formater le contenu du message
Appender : utilisé pour envoyer le message à une cible de stockage : console, fichier, base de données, email, etc
Les **niveau de gravité** permettent de filtrer les messages à envoyer dans les appenders. En configurant le <control>niveau de gravite</control> voulu au lancement dune application, il est possible d'envoyer ou non des messages à l'exécution en fonction de leur propre niveau de gravité.
**Important**: Pour le développement d'une application, il est très recommandé de se baser uniquement sur une API logging. Il faut donc évité d'utiliser les instructions System.out.println() et printStackTrace() (méthode des exception).
##Pour mettre en place du logging dans ce cours, nous nous bason sur la librarie LOJ4J.
Nous l'utilisons car elle est simle à mettre en oeuvre en plus et qu'elle a toutes les fonctionnalités dont nous avons besoin. De plus, elle est très répendue et populaire.
Note : La mise en place d'autre librairies de logging est très siilaire à celle de LOg4J. Il n'est donc pas difficile d'apprendre à utiliser une autre librairie s'il y a besoin.
##Dependances.
Pour utiliser la librairie, nous définissons la dépendance suivante dans un projet GRADle

```java
    dependencies {
    implementation("org.apache.logging.log4j:log4j-core:2.20.0")
    }
```
