# Conversions de types en Java

## Conversion String ↔️ Nombre

```java
// Convertir une chaîne en entier
String numStr = "42";
int num = Integer.parseInt(numStr);

// Convertir un entier en chaîne
String backToStr = Integer.toString(num);
```

## Conversion de tableaux

```java
// Tableau d'entiers
int[] array = {1, 2, 3};

// Tableau de chaînes
String[] strArray = {"a", "b", "c"};

// Chaîne vers tableau de caractères
char[] charArray = "hello".toCharArray();

// Tableau de caractères vers chaîne
String str = new String(charArray);
```