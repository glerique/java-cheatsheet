# Opérations sur les tableaux en Java

## Import des utilitaires

```java
import java.util.Arrays;
import java.util.Collections;
import java.util.Comparator;
```

## Tri (Sorting)

```java
// Trier un tableau d'entiers en ordre croissant
int[] arr = {3, 1, 2};
Arrays.sort(arr); // arr = [1, 2, 3]

// Trier un tableau d'entiers en ordre décroissant (Java 8+)
int[] arrDesc = {3, 1, 2};
Arrays.sort(arrDesc);
for (int i = 0; i < arrDesc.length / 2; i++) {
    int tmp = arrDesc[i];
    arrDesc[i] = arrDesc[arrDesc.length - 1 - i];
    arrDesc[arrDesc.length - 1 - i] = tmp;
}
// arrDesc = [3, 2, 1]

// Trier un tableau d'objets (ex : Integer[]) en ordre décroissant
Integer[] objArray = {3, 1, 2};
Arrays.sort(objArray, Collections.reverseOrder()); // objArray = [3, 2, 1]

// Tri personnalisé (ex : décroissant pour Integer[])
Arrays.sort(objArray, (a, b) -> b - a); // objArray = [3, 2, 1]

// Tri personnalisé avec Comparator (ex : par longueur de String)
String[] words = {"bb", "a", "ccc"};
Arrays.sort(words, Comparator.comparingInt(String::length)); // words = ["a", "bb", "ccc"]

// Tri d'un tableau de String en ordre alphabétique inverse
String[] alpha = {"b", "a", "c"};
Arrays.sort(alpha, Collections.reverseOrder()); // alpha = ["c", "b", "a"]
```

## Remplissage (Filling)

```java
// Remplir tout le tableau avec la valeur 0
int[] arr = new int[5];
Arrays.fill(arr, 0); // arr = [0, 0, 0, 0, 0]

// Remplir une partie du tableau
Arrays.fill(arr, 1, 4, 7); // arr = [0, 7, 7, 7, 0]
```

## Copie et sous-tableaux

```java
// Copier un tableau
int[] arr2 = Arrays.copyOf(arr, arr.length); // arr2 = copie de arr

// Copier une partie du tableau
int[] sub = Arrays.copyOfRange(arr, 1, 4); // sub = [7, 7, 7]
```

## Recherche

```java
// Recherche d'une valeur (tableau trié)
int[] sorted = {1, 2, 3, 4};
int idx = Arrays.binarySearch(sorted, 3); // idx = 2 (position de 3)
```

## Autres opérations utiles

```java
// Comparer deux tableaux (égalité des éléments)
int[] arr1 = {1, 2, 3};
int[] arr2 = {1, 2, 3};
boolean egaux = Arrays.equals(arr1, arr2); // egaux = true

// Afficher le contenu d'un tableau sous forme de chaîne
System.out.println(Arrays.toString(arr1)); // affiche: [1, 2, 3]

// Remplacer tous les éléments selon une règle (Java 8+)
int[] nums = {1, 2, 3};
Arrays.setAll(nums, i -> nums[i] * 2); // nums = [2, 4, 6]
```

## Conversion tableau ↔️ List

```java
// Array vers List (non modifiable)
String[] strArray = {"a", "b"};
List<String> list = Arrays.asList(strArray); // list = ["a", "b"]

// List vers Array
String[] arr3 = list.toArray(new String[0]); // arr3 = ["a", "b"]
```