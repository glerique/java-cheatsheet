# Opérations mathématiques en Java

## Opérations de base

```java
// Obtenir le maximum entre deux valeurs
int max = Math.max(5, 10);      // Retourne 10

// Obtenir le minimum entre deux valeurs
int min = Math.min(5, 10);      // Retourne 5

// Valeur absolue (toujours positive)
int abs = Math.abs(-5);         // Retourne 5

// Puissance (x à la puissance y)
double pow = Math.pow(2, 3);    // Retourne 8.0 (2³)

// Racine carrée
double sqrt = Math.sqrt(16);    // Retourne 4.0

// Arrondi à l'entier le plus proche
long round = Math.round(3.7);   // Retourne 4

// Arrondi à l'entier inférieur
double floor = Math.floor(3.7); // Retourne 3.0

// Arrondi à l'entier supérieur
double ceil = Math.ceil(3.2);   // Retourne 4.0
```

## Nombres aléatoires

```java
// Génère un nombre décimal aléatoire entre 0.0 (inclus) et 1.0 (exclu)
double random = Math.random();

// Génère un entier aléatoire entre 0 et 99 inclus
int randomInt = (int)(Math.random() * 100);
```

## Constantes mathématiques

```java
// La constante Pi (π)
double pi = Math.PI;  // 3.141592653589793

// La constante e (base des logarithmes naturels)
double e = Math.E;    // 2.718281828459045
```