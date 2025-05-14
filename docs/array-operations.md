# Opérations sur les tableaux en Java

## Import des utilitaires

```java
import java.util.Arrays;
import java.util.Collections;
```

## Tri (Sorting)

```java
// Trier un tableau d'entiers en ordre croissant
Arrays.sort(arr);

// Trier un tableau d'objets (ex : Integer[]) en ordre décroissant
Arrays.sort(objArray, Collections.reverseOrder());

// Tri personnalisé (ex : décroissant pour Integer[])
Arrays.sort(objArray, (a, b) -> b - a);
```

## Remplissage (Filling)

```java
// Remplir tout le tableau avec la valeur 0
Arrays.fill(arr, 0);
```

## Autres opérations utiles

```java
// Comparer deux tableaux (égalité des éléments)
boolean egaux = Arrays.equals(arr1, arr2);

// Afficher le contenu d'un tableau sous forme de chaîne
System.out.println(Arrays.toString(arr));
```