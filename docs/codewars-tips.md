# Astuces fréquentes pour Codewars en Java

## Manipulation de chaînes

```java
// Vérifier si une chaîne est vide ou ne contient que des espaces
s.isEmpty();                  // true si s == ""
s.isBlank();                  // true si s == "" ou ne contient que des espaces (Java 11+)

// Répéter une chaîne (Java 11+)
"abc".repeat(3);              // "abcabcabc"

// Remplacer tout sauf les chiffres (regex)
String digits = "a1b2c3".replaceAll("\\D", ""); // digits = "123"

// Découper une chaîne sur plusieurs espaces ou séparateurs
String[] words = "a b   c".split("\\s+"); // words = ["a", "b", "c"]

// Inverser une chaîne
String reversed = new StringBuilder("hello").reverse().toString(); // reversed = "olleh"
```

## Tableaux et listes

```java
// Créer un tableau d'entiers à partir d'une liste
List<Integer> list = Arrays.asList(1, 2, 3);
int[] arr = list.stream().mapToInt(Integer::intValue).toArray(); // arr = [1, 2, 3]

// Créer une liste à partir d'un tableau
int[] arr2 = {4, 5, 6};
List<Integer> list2 = Arrays.stream(arr2).boxed().collect(Collectors.toList()); // list2 = [4, 5, 6]

// Trier un tableau en ordre décroissant
Integer[] nums = {3, 1, 2};
Arrays.sort(nums, Collections.reverseOrder()); // nums = [3, 2, 1]
```

## Streams et lambdas (Java 8+)

```java
// Somme des éléments d'un tableau
int[] arr = {1, 2, 3};
int sum = Arrays.stream(arr).sum(); // sum = 6

// Filtrer et compter les éléments pairs
long count = Arrays.stream(arr).filter(x -> x % 2 == 0).count(); // count = 1

// Transformer une liste de chaînes en majuscules
List<String> mots = Arrays.asList("a", "b", "c");
List<String> upper = mots.stream().map(String::toUpperCase).collect(Collectors.toList()); // upper = ["A", "B", "C"]
```

## Math et conversions rapides

```java
// Générer un entier aléatoire entre 0 et 9 inclus
int rand = (int)(Math.random() * 10); // ex: 7

// Limiter une valeur entre min et max (avant Java 21)
int val = 15, min = 0, max = 10;
int clamped = Math.max(min, Math.min(val, max)); // clamped = 10

// Arrondi à l'entier le plus proche
int rounded = (int)Math.round(3.6); // rounded = 4

// Conversion String <-> int
int n = Integer.parseInt("42"); // n = 42
String s = Integer.toString(42); // s = "42"
```

## Pièges fréquents

```java
// Attention à l'égalité des chaînes
"abc" == "abc"; // false (ne pas utiliser == pour comparer des chaînes)
"abc".equals("abc"); // true

// Attention aux IndexOutOfBoundsException
int[] arr = {1, 2, 3};
// arr[3]; // Exception ! Les indices vont de 0 à 2

// Attention à la casse dans les comparaisons
"Hello".equals("hello"); // false
"Hello".equalsIgnoreCase("hello"); // true
```

## Templates utiles

```java
// Fonction utilitaire pour inverser un tableau d'entiers
public static int[] reverse(int[] arr) {
    for (int i = 0; i < arr.length / 2; i++) {
        int tmp = arr[i];
        arr[i] = arr[arr.length - 1 - i];
        arr[arr.length - 1 - i] = tmp;
    }
    return arr;
}
```