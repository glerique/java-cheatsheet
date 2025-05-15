# Listes Java

- **Importation :**
    ```java
    import java.util.*;
    ```

- **Création d'une liste :**
    ```java
    List<Integer> liste = new ArrayList<>();
    liste.add(1); // liste = [1]
    liste.add(2); // liste = [1, 2]
    liste.add(3); // liste = [1, 2, 3]
    List<String> mots = Arrays.asList("a", "b", "c"); // mots = ["a", "b", "c"]
    ```

- **Opérations courantes :**
    ```java
    liste.get(0);        // 1 (Accéder par index)
    liste.set(1, 42);    // liste = [1, 42, 3] (Modifier la valeur à un index)
    liste.remove(2);     // liste = [1, 42] (Supprimer par index)
    liste.contains(42);  // true (Vérifier la présence d'une valeur)
    liste.indexOf(42);   // 1 (Obtenir l'index d'un élément)
    liste.size();        // 2 (Taille de la liste)
    liste.isEmpty();     // false (Vérifier si vide)
    liste.clear();       // liste = [] (Tout supprimer)
    ```

- **Boucles et parcours :**
    ```java
    for (int n : liste) { /* ... */ } // Parcours classique
    liste.forEach(System.out::println); // Parcours avec lambda
    ```

- **Conversion entre tableaux et listes :**
    ```java
    Integer[] tableau = liste.toArray(new Integer[0]); // tableau = [1, 42]
    List<Integer> nouvelleListe = Arrays.asList(tableau); // Taille fixe, nouvelleListe = [1, 42]
    List<Integer> listeModifiable = new ArrayList<>(Arrays.asList(tableau)); // listeModifiable = [1, 42]
    ```

- **Autres opérations utiles :**
    ```java
    Collections.sort(listeModifiable); // Tri croissant, listeModifiable = [1, 42]
    Collections.reverse(listeModifiable); // Inverse l'ordre, listeModifiable = [42, 1]
    Collections.shuffle(listeModifiable); // Mélange aléatoirement
    List<Integer> sub = listeModifiable.subList(0, 1); // sub = [42]
    ```

- **Conversion String ↔️ List<Character> :**
    ```java
    String s = "abc";
    List<Character> chars = new ArrayList<>();
    for (char c : s.toCharArray()) chars.add(c); // chars = ['a', 'b', 'c']
    ```

