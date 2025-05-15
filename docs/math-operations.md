# Opérations mathématiques en Java

## Opérations de base

```java
// Obtenir le maximum entre deux valeurs
int max = Math.max(5, 10);      // max = 10

// Obtenir le minimum entre deux valeurs
int min = Math.min(5, 10);      // min = 5

// Valeur absolue (toujours positive)
int abs = Math.abs(-5);         // abs = 5
float absF = Math.abs(-3.5f);   // absF = 3.5f
long absL = Math.abs(-10L);     // absL = 10L
double absDouble = Math.abs(-2.5); // absDouble = 2.5

// Puissance (x à la puissance y)
double pow = Math.pow(2, 3);    // pow = 8.0 (2³)

// Racine carrée et cubique
double sqrt = Math.sqrt(16);    // sqrt = 4.0
double cbrt = Math.cbrt(27);    // cbrt = 3.0

// Logarithmes
double ln = Math.log(Math.E);      // ln = 1.0 (logarithme naturel)
double log10 = Math.log10(100);    // log10 = 2.0 (logarithme décimal)

// Exponentielle
double exp = Math.exp(1);          // exp = 2.718281828459045

// Sinus, cosinus, tangente (en radians)
double sin = Math.sin(Math.PI / 2); // sin = 1.0
double cos = Math.cos(0);           // cos = 1.0
double tan = Math.tan(Math.PI / 4); // tan = 1.0

// Conversion degrés ↔ radians
double rad = Math.toRadians(180);   // rad = 3.141592653589793
double deg = Math.toDegrees(Math.PI); // deg = 180.0

// Racine de la somme des carrés (hypoténuse)
double hypot = Math.hypot(3, 4);    // hypot = 5.0

// Signe d'un nombre
double sign = Math.signum(-42);     // sign = -1.0

// Clamp (Java 21+)
int clamped = Math.clamp(15, 0, 10); // clamped = 10
// Avant Java 21 :
int clampedOld = Math.max(0, Math.min(15, 10)); // clampedOld = 10

// Arrondi à l'entier le plus proche
long round = Math.round(3.7);   // round = 4

// Arrondi à l'entier inférieur
double floor = Math.floor(3.7); // floor = 3.0

// Arrondi à l'entier supérieur
double ceil = Math.ceil(3.2);   // ceil = 4.0

// Arrondi vers zéro (tronque la partie décimale)
int trunc = (int) 3.9;          // trunc = 3
```

## Nombres aléatoires

```java
// Génère un nombre décimal aléatoire entre 0.0 (inclus) et 1.0 (exclu)
double random = Math.random(); // ex: 0.532...

// Génère un entier aléatoire entre 0 et 99 inclus
int randomInt = (int)(Math.random() * 100); // ex: 42

// Générer un entier aléatoire dans un intervalle [min, max] inclus
int min = 5, max = 10;
int randInRange = min + (int)(Math.random() * (max - min + 1)); // ex: 7

// Générer un nombre aléatoire négatif ou positif
int randSign = Math.random() < 0.5 ? -1 : 1; // randSign = -1 ou 1

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