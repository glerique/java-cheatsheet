# Les Boucles en Java

## Boucle for

```java
// Boucle classique avec compteur
for (int i = 0; i < 5; i++) {
    System.out.println("i = " + i); // Affiche: i = 0, i = 1, i = 2, i = 3, i = 4
}

// Parcourir un tableau avec for
int[] tab = {10, 20, 30};
for (int i = 0; i < tab.length; i++) {
    System.out.println(tab[i]); // Affiche: 10, 20, 30
}

// Boucle avec pas personnalisé
for (int i = 0; i <= 10; i += 2) {
    System.out.println(i); // Affiche: 0, 2, 4, 6, 8, 10
}

// Boucle for à l'envers (décroissant)
for (int i = 5; i > 0; i--) {
    System.out.println(i); // Affiche: 5, 4, 3, 2, 1
}
```

## Boucle foreach

```java
// Parcourir un tableau avec foreach
int[] tab = {10, 20, 30};
for (int val : tab) {
    System.out.println(val); // Affiche: 10, 20, 30
}

// Parcourir une liste avec foreach
List<String> mots = Arrays.asList("a", "b", "c");
for (String mot : mots) {
    System.out.println(mot); // Affiche: a, b, c
}
```

## Boucle while

```java
// Boucle while classique
int i = 0;
while (i < 5) {
    System.out.println("i = " + i); // Affiche: i = 0, ..., i = 4
    i++;
}

// Boucle while avec condition de sortie
int n = 10;
while (n > 0) {
    n--;
    if (n == 5) break; // Sort de la boucle quand n == 5
}
```

## Boucle do...while

```java
// Boucle do...while (s'exécute au moins une fois)
int j = 0;
do {
    System.out.println(j); // Affiche: 0, 1, 2, 3, 4
    j++;
} while (j < 5);
```

## Contrôle de boucle

```java
// Utilisation de continue et break
for (int i = 0; i < 5; i++) {
    if (i == 2) continue; // Passe à l'itération suivante quand i == 2
    if (i == 4) break;    // Sort de la boucle quand i == 4
    System.out.println(i); // Affiche: 0, 1, 3
}
```

