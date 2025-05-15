# Manipulation de chaînes de caractères en Java

## Bases des chaînes

```java
String s = "hello";
s.length();                // Longueur de la chaîne : 5
s.charAt(0);               // Premier caractère : 'h'
s.charAt(s.length() - 1);  // Dernier caractère : 'o'
s.substring(1, 4);         // Sous-chaîne de l'indice 1 à 3 : "ell"
s.indexOf("l");            // Position du premier 'l' : 2
s.lastIndexOf("l");        // Position du dernier 'l' : 3
```

## Transformations de chaînes

```java
s.toUpperCase();           // Met en majuscules : "HELLO"
s.toLowerCase();           // Met en minuscules : "hello"
s.trim();                  // Supprime les espaces au début et à la fin
s.replace("l", "p");       // Remplace tous les 'l' par 'p' : "heppo"
s.contains("el");          // Vérifie si "el" est présent : true
s.startsWith("he");        // Commence par "he" ? true
s.endsWith("lo");          // Finit par "lo" ? true
```

## Découper et assembler des chaînes

```java
String[] parts = "a,b,c".split(",");      // Découpe en tableau : ["a", "b", "c"]
String joined = String.join("-", parts);  // Assemble avec "-" : "a-b-c"
```

## StringBuilder pour une concaténation efficace

```java
StringBuilder sb = new StringBuilder();
sb.append("hello").append(" ").append("world");
String result = sb.toString();  // result = "hello world"
```

## Conversion entre String et char[]

```java
char[] chars = s.toCharArray();           // chars = ['h', 'e', 'l', 'l', 'o']
String fromChars = new String(chars);     // fromChars = "hello"
```

## Suppression d'espaces et nettoyage

```java
String messy = "  hello  ";
String clean = messy.trim();              // clean = "hello"
String noSpaces = messy.replace(" ", ""); // noSpaces = "hello"
String noAllSpaces = messy.replaceAll("\\s+", ""); // noAllSpaces = "hello"
```

## Comparaison de chaînes

```java
"abc".equals("abc");           // true (sensible à la casse)
"abc".equalsIgnoreCase("ABC"); // true (insensible à la casse)
```

## Formattage de chaînes

```java
String name = "Bob";
int age = 30;
String formatted = String.format("%s a %d ans", name, age); // formatted = "Bob a 30 ans"
```

## Astuces fréquentes Codewars

```java
// Vérifier si une chaîne est vide ou ne contient que des espaces
s.isEmpty();                  // true si s == ""
s.isBlank();                  // true si s == "" ou ne contient que des espaces (Java 11+)

// Répéter une chaîne (Java 11+)
"abc".repeat(3);              // "abcabcabc"

// Remplacer avec regex (expressions régulières)
String digits = "a1b2c3".replaceAll("\\D", ""); // digits = "123" (supprime tout sauf chiffres)

// Découper avec regex
String[] words = "a b   c".split("\\s+"); // words = ["a", "b", "c"]

// Extraire un caractère sous forme de String
String first = s.substring(0, 1);         // first = "h"

// Inverser une chaîne
String reversed = new StringBuilder(s).reverse().toString(); // reversed = "olleh"
```
