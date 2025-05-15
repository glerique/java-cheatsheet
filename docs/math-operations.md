# Opérations mathématiques en Java

## Opérations de base

```java
// Obtenir le maximum entre deux valeurs
int max = Math.max(5, 10);      // max = 10

// Obtenir le minimum entre deux valeurs
int min = Math.min(5, 10);      // min = 5

// Valeur absolue (toujours positive)
int abs = Math.abs(-5);         // abs = 5

// Puissance (x à la puissance y)
double pow = Math.pow(2, 3);    // pow = 8.0 (2³)

// Racine carrée
double sqrt = Math.sqrt(16);    // sqrt = 4.0

// Arrondi à l'entier le plus proche
long round = Math.round(3.7);   // round = 4

// Arrondi à l'entier inférieur
double floor = Math.floor(3.7); // floor = 3.0

// Arrondi à l'entier supérieur
double ceil = Math.ceil(3.2);   // ceil = 4.0

// Valeur absolue pour double
double absDouble = Math.abs(-2.5); // absDouble = 2.5

// Racine cubique
double cbrt = Math.cbrt(27); // cbrt = 3.0

// Logarithme naturel
double ln = Math.log(Math.E); // ln = 1.0

// Logarithme décimal
double log10 = Math.log10(100); // log10 = 2.0

// Exponentielle
double exp = Math.exp(1); // exp = 2.718281828459045
```

## Nombres aléatoires

```java
// Génère un nombre décimal aléatoire entre 0.0 (inclus) et 1.0 (exclu)
double random = Math.random(); // ex: 0.532...

// Génère un entier aléatoire entre 0 et 99 inclus
int randomInt = (int)(Math.random() * 100); // ex: 42

// Avec Random (plus flexible)
import java.util.Random;
Random r = new Random();
int randInt = r.nextInt(100); // randInt entre 0 et 99
double randDouble = r.nextDouble(); // randDouble entre 0.0 et 1.0
```

## Constantes mathématiques

```java
// La constante Pi (π)
double pi = Math.PI;  // pi = 3.141592653589793

// La constante e (base des logarithmes naturels)
double e = Math.E;    // e = 2.718281828459045
```