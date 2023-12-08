# 68 -Interfaces fonctionnelles et expressions Lambda
Afin d'introduire la **programmation fonctionnelle**, deux concepts ont été introduit en Java 8 : Les interfacas fonctionnelles et les expressions lambda.
Les spécifications des expressions lambda sont définies dans la __JSR 335 (Project Lambda)__

Les expressions lambda sont aussi nommées **closures** ou **fonctions anonylmes**:
leur but principal est de permettre de passer en paramètre un ensemble de traitements. Pour faire simple, il sera possible de définir le comportement d'une fonction dynamquement lors de l'appel de celle-ci.

Rappel : Les **classe anonymes** permettent également d'obtenir ce type de comportements. Cependant, la syntaxe de celles-ci est très lourde ç écrire. On va voir que les expressions lambda permettent d'écriture du code beaucoup plus court et lisible.


##Interfaces fonctionnelles.

Une interface fonctionnelle se définit de la manière suivantes:

<code-block>
@FunctionalInterface  
public interface CallBack{  
    void affichageCallBack();
}  
</code-block>


L'implémentation de la méthode affichageCallback se fait dynamiquement en utilisant des expressions lamda après coup ( voir exemple dans la section ci-après).

Ces interfaces particulières ont les contraintes suivantes :
* Une seule méthode doit être définie : ce sera la "la méthode cible" utilisée pour les expressions lambda.
* La méthode définie ne peut pas avoir d'implémentation par défaut. On ne peut donc pas utiliser le mot-clé défault.

##Expression Lambda

En utilisant l'interface fonctionnelle définie ci-dessous, on peut alors définir une expressions lambda de cette manière.
<code-block>
CallBack callBack = () -> System.out.println("Texte affiché à l'appel de la méthode affichageCallback");
callBack.affichageCallback();
</code-block>

Il est également possible de définir une expression lambda sur plusieurs lignes en l'entourant de { } :


<code-block>
CallBack callBack = () -> System.out.println("Texte affiché à l'appel de la méthode affichageCallback");
callBack.affichageCallback();
</code-block>

Il est également possible de définir une expression lambda sur plusieurs lignes en l'entourant de {}

<code-block>
CallBack callBack =() -> {
var hello = "Hello";
var world = "Word";
System.out.println(hello+world));
}
</code-block>

##Lambda avec arguments

Il est possible de définir des arguments d'entrées la méthode de l'interface fonstionnelle et de les passer en entrée de la lambda de la manière suivante:

```java
public class Main{
public static void main (String []args){
 CallBack callBack = (String chaine, String chaine
) -> System.out.println(chaine + chaine);
callBack.afficherCallback("Jelloe,"World");
}

@FunctionalInterface
public interface CallBack{
void affichageCallback(String chaine, String chaine);
}
```

##Réferences de méthodes

Exemple d'utilisation :
```java
public class Main {
    public static void main(String[] args) {

        CallBack callBack = System.out::println;

    }

    @FunctionalInterface
    public interface CallBack {
        void afficherNom(String nom);
    }
}
```
Quand le paramètre d'entrée d'une lambda est utilisé directement au sein dune autre méthode, il est alors possible de faire appel à la **référence de la méthodes** en utilisant les :: . Sans **référence de méthodes**, on a alors la lambda suivante :

```Java
CallBack callBack = nom -> System.out.println(nom);
```
Les deux codes se comportent de la même manière. Les références de méthodes sont un **sucre syntaxique.**

##Comparaison avec les classes anonymes.

Voici le code qui montre pour le même comportement la différence de code entre les expresssions lambda et les **classe anonymes :**

```Java
//Exemple avec lambda
CallBack callBack = () -> System.out.println("callback lambda");
callBack.affichageCallback();

//Exxemple avec classe anonyme
CallBack callBackAnonyme = new CallBack() {
@Override
public void affichageCallBack(){
System.out.println("callback class anonyme");
}
};
callBackAnonyme.affichageCallback();
```
On voit bien que le code de l'expression lambda tient sur moins de ligne et qu'il est beaucooup plus clair.