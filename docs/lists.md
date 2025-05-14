# Listes Java

- **Importation :**
    ```java
    import java.util.*;
    ```

- **Création d'une liste :**
    ```java
    List<Integer> liste = new ArrayList<>();
    liste.add(1);
    liste.add(2);
    liste.add(3);
    ```

- **Opérations courantes :**
    ```java
    liste.get(0);        // Accéder par index
    liste.set(1, 42);    // Modifier la valeur à un index
    liste.remove(2);     // Supprimer par index
    liste.contains(42);  // Vérifier la présence d'une valeur
    liste.indexOf(42);   // Obtenir l'index d'un élément
    liste.size();        // Taille de la liste
    liste.isEmpty();     // Vérifier si vide
    liste.clear();       // Tout supprimer
    ```

- **Conversion entre tableaux et listes :**
    ```java
    Integer[] tableau = liste.toArray(new Integer[0]);
    List<Integer> nouvelleListe = Arrays.asList(tableau); // Taille fixe
    List<Integer> listeModifiable = new ArrayList<>(Arrays.asList(tableau));
    ```Java Lists

- **Importation :**
    ```java
    import java.util.*;
    ```

