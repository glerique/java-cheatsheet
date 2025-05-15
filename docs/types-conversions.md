# Conversions de types en Java

## Conversion String ↔️ Nombre

```java
// Convertir une chaîne en entier
String numStr = "42";
int num = Integer.parseInt(numStr); // num = 42

// Convertir une chaîne en double/float
double d = Double.parseDouble("3.14"); // d = 3.14
float f = Float.parseFloat("2.71");    // f = 2.71f

// Convertir un entier en chaîne
String backToStr = Integer.toString(num); // backToStr = "42"

// Convertir un double/float en chaîne
String dStr = Double.toString(d);   // dStr = "3.14"
String fStr = Float.toString(f);    // fStr = "2.71"

// Casting entre types numériques
int i = (int) 3.99;      // i = 3
double d2 = (double) 42; // d2 = 42.0
```

## Conversion String ↔️ boolean

```java
// String vers boolean
boolean b = Boolean.parseBoolean("true"); // b = true

// boolean vers String
String boolStr = Boolean.toString(b); // boolStr = "true"
```

## Conversion char ↔️ String

```java
// char vers String
char c = 'a';
String s = Character.toString(c); // s = "a"

// String vers char (premier caractère)
char c2 = s.charAt(0); // c2 = 'a'
```

## Conversion de tableaux

```java
// Tableau d'entiers
int[] array = {1, 2, 3}; // array = [1, 2, 3]

// Tableau de chaînes
String[] strArray = {"a", "b", "c"}; // strArray = ["a", "b", "c"]

// Chaîne vers tableau de caractères
char[] charArray = "hello".toCharArray(); // charArray = ['h', 'e', 'l', 'l', 'o']

// Tableau de caractères vers chaîne
String str = new String(charArray); // str = "hello"
```

## Conversion List ↔️ Array

```java
import java.util.Arrays;
import java.util.List;

// Array vers List
String[] arr = {"a", "b"};
List<String> list = Arrays.asList(arr); // list = ["a", "b"]

// List vers Array
String[] arr2 = list.toArray(new String[0]); // arr2 = ["a", "b"]
```

## Boxing / Unboxing

```java
// Boxing : int vers Integer
Integer boxed = Integer.valueOf(5); // boxed = 5

// Unboxing : Integer vers int
int unboxed = boxed.intValue(); // unboxed = 5
```