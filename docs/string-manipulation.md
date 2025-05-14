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
String result = sb.toString();  // "hello world"
```
