# 20 LOG CH code avant passage en logger

``` java
public class Main {
    public static void main(String[] args) {
        var client = getClient();
        System.out.println("Fin d'exécution");

    }

    private static Person getClient ()
    {
        System.out.println("Debut de client");
        var person = new Person("Donsin","Alain",30);
        System.out.println("Debut de client");
        return person;
    }
    record Person (String Nom, String Prenom, int age) {};
}
```

Dependance orp.apache.logging.lo4j.loj4j.core:2.20.0