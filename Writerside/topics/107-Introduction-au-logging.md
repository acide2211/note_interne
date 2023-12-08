# 107 Introduction au logging

#Introduction au logging

Depuis le début du cours, tous les affichagesans la console sont effectués dans la console n tulisant l'instruction System.out.println(). Cette approche est assez limitée et il est possible de faire mieux grâce aux librairies **logegin**

##Qu'est-ce que le logging?

Le **logging// constiste à ajouter des traitements dans les applications pour permettre l'émission et le stockage de message suite à des évènements.

Une **Api de logging** fait généralement intervenir trois composants principaux :
*  Logger: invoqué pour émettre grâce au frameword un message généralement avec un **niveau de gravité** associé.
* *  Formatter : utilisé pour formater un contenu du message
*  Appender: utilisé pour envoyer le message à une cible de stockage: console, fichier, base de données, email, etc.
Les **niveau de gravité** permettent de filtrer les messages à envoyer dans les apenders. En configurant le **niveau de gravité** voulu au lancement d'une application, il est possible 'envoyer ou non des messages à l'exécution en fonction de leur propre niveau de gravité.
**Important : Pour le développement d'une application, il est très recommandé de se basser uniquement sur une API de loggin. Il faut donc éviter d'utiliser les instructions System.out.println() et printStackTrace() (méthode des execptions).
##LOG4J

Pour mettre en place du logging dans ce cours, nous nous basons sur la librairie LO4J

Nous l'utilisons car elle est simple à mettre en oeuvre en plus et qu'elle a toutes les fonctionnalités dont nous avons besoin. De plus, elle est très répendue et populaire.

Note: La mise en place d'autre librairies de logging est très similaire à celle de Log4J. Il n'est donc pas difficile d'apprendre à utiliser une autre librairie s'il y a besoin

##Dependance

Pour utiliser la librairie, nous défissons la dépendance suivante dans un projet Gradle : 

```java
dependencies {
    implementation("org.apache.logging.log4j:log4j-core:2.20.0")
}
```



