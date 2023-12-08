# 108 - Configurer les loggers

##Configuration par logger

Il est possible de définir des niveau de configuration à un ou plusieurs loggers plutôt qu'à l'ensemble des loggers à la fois dans log4j2.properties:

```java
appender.console.type = Console
appender.console.name = consoleLogger
appender.console.layout.type = PatternLayout
appender.console.layout.pattenr = %d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n

loggers = com.dyma.app,com.other

logger.com.dyma.app.name= com.dyma.app
logger.com.dyma.app.level=error
logger.com.dyma.app.appenderRef.stout.ref=consoleLogger

logger.com.other.name=com.other
logger.com.other.level=debug
logger.com.other.appenderRef.stout.ref=consoleLogger
```

Ici, nous configurons les **loggers** par package. Cela nous permet de changer le **niveau de sévérité** de certaines classes seulement, ou même les appenders comme nous allons le voir maintenant.

##Configurer les appenders

Un appender permet de spécifier une cible de sortie pour les messages de log. Concrètement, cela permet de rediriger les **flux de sortie** de la librairie de **logging** au bon endroit.

Pour configurer des appenders, il est possible de le faire toujours dans le fichier log4j2.properties

```Java

appenders = console,file

appender.console.type = Console
appender.console.name = consoleLogger
appender.console.layout.type = PatternLayout
appender.console.layout.pattenr = %d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n

appender.file.type = File
appender.file.name = FileLogger
appender.file.fileName = ./app.debug.log
appender.file.layout.type = PattenrLAyout
appender.file.layout.pattenr = %d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n

logger.com.dyma.app.name=com.dyma.app
logger.com.dyma.app.level=error
logger.com.dyma.app.appenderRef.stdout.ref=consoleLogger

logger.com.other.name=com.other
logger.com.other.level=debug
logger.com.other.appenderRef.file.ref=FileLogger


```

Ici l'appender du logger com.other a été modifié pour être stocker dans le fichier app.debug.log

Les Formatters.

On peut également configurer le format des messages à aficher.