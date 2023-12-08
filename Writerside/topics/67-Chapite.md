# 67 - Introduction à la programmation fonctionnelle

#Introduction à la programmation fonctionnelle

##La programmation foncctionnelle

La __programmation fonctionnelle__ est un paradigme de la programmation
Dans un programme fonctionnel. Tous les éléments peuvent être ompris comme des **fonctions** et le code peut être exécuté par des **appells successifs de fonctions.**

Java permet d'apporcher la programmation fonctionnelle grâce aux interface fonctionnelles et aux expressions lamba. Leurs fonctionnement seront décrit dans le prochaine leçon.

Java n'est **pas purement** fonctionnel, il est possible de continuer à faire de l'impératif et e l'orienté objet en plus de la programmation fonctionnelle. Il faut le voir comme un outil supplémentaire pour résoudre plus facilement certains problèmes.

##Les expressions lambda.

Une expression lambda est une **fonction anonyme**: sa définition se faut sans déclaration explicite du type de retour, ne de modificatieurs d'accès ne de nom. C'est un raccourci syntacique qui permet de définir une méthode directement à l'endroit ou est utilisée.

Si vous vous rappeler de la leçon sur les **les classe anonimes** dans le chapitre de la **Programmation Orienté Objet**, il était déjà possible de définir des méthodes aux moment de leur utilisation. Cependant, la syntaxe pour utiliser ces classes anonymes est très lourde ce qui la rend notamment difficile à lire. Les expressions lambda nous permettent d'obtenir le même résultat mais de manière beaucoup plus simple et concise.

##Collections et API Stream.

Grâce aux expresions lambda, l'api stream a pu voir le jour avec la version 8 de java

Nous verrons dans les leçons dédiées qu'il est possible de réaliser un grand nombre d'opérations sur les collections de données grâce à cette API. Le principe est d'utiliser la programmation fonctionnelle autour de collections afin d'appliquer une multitude d'opérations en utilisant une syntace plus proche encore du langage humaine que ce que permet le language avec d'autre **paradigmes**

##Les principales caractèristiques de la programmation fonctionnelle.

Le paradigme de la programmation fonctionnelle repose sur des **concepts clés**:

* **Les fonctions pures**: ce sont des fonctions qui ne dépendent que de leurs propres paramètres. Ici, la valeur de retour reste la même, même si la fonction est exacutée à plusieurs reprises au cours du programme. Aucune interraction extérieure n'est permise.

* **Limmutabilité** : elle traduit le fait que les fonction ne changennt pas d'état, ce qui fait que'on peut les utiliser comme des constantes. Elle demerent intactes, et les variables son fixes.

* **L'écriture lazy** c'est un style d'écriture de code particulier qui permet de n'exécuter les expressions que lorsqu'elles sont indispensables. cela améliore grandement les performances de l'application.

* **La séparation et le traitement des données ** : ces termes désignent les manipulations de données, c'est-à-dire l'insertion et l'extraction de celles-ci. Vu que la manipulation de données implique un changement d'etat, ce qui est hors du principe de ce paradigme, la solution réside dans l'élaboration de plusieur fonctions pures en laissant celles-ci traiter eles-mêmes les données, puis en les passant dans une fonction impure pour les insertions ou  les extractions.

* **Les fonctions anonymes ** : ce sont des fonctions qui sont, comme leur nom l'indique, anonymes par définition. Ainsi, elles ne sont pas ésignées par un no et offremt une meilleurs lisiilité du ode.

* **La composition** : Il s'agit d'une construction et de l'utilisation de fonctions pour éléborer tout le programme. Ici, il y a un assemblage de fonctions qui en constutuent de nouvelles.  
  Nous verrons qu'en java, tous les concepts ne sont pas appliqués à la lettre. On s'en approche avec les expressions lambda, mais **ce n'est pas un langage purement *fonctionnelle. En effet, seuls les langages prement onctionnels peuvent vraiment respecter tous les critères mentionnées à la lettres

