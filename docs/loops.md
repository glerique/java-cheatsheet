# Les Boucles en Java

## Boucle for

```java
// Boucle classique avec compteur
for (int i = 0; i < 5; i++) {
    System.out.println("i = " + i); // Affiche 0 à 4
}

// Parcourir un tableau avec for
int[] tab = {10, 20, 30};
for (int i = 0; i < tab.length; i++) {
    System.out.println(tab[i]);
}

// Boucle avec pas personnalisé
for (int i = 0; i <= 10; i += 2) {
    System.out.println(i); // Affiche 0, 2, 4, 6, 8, 10
}
``` 

## Boucle foreach

```java
// Parcourir un tableau avec foreach
int[] tab = {10, 20, 30};
for (int val : tab) {
    System.out.println(val);
}
```

## Boucle while

```java
// Boucle while classique
int i = 0;
while (i < 5) {
    System.out.println("i = " + i);
    i++;
}
``` 

