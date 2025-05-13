# Type Conversions in Java

## String ↔️ Number Conversions
```java
// Converting String to a number
String numStr = "42";
int num = Integer.parseInt(numStr);

// Converting number back to String
String backToStr = Integer.toString(num);
```

## Array Conversions
```java
// Integer array
int[] array = {1, 2, 3};

// String array
String[] strArray = {"a", "b", "c"};

// String to char array
char[] charArray = "hello".toCharArray();

// Char array to String
String str = new String(charArray);
```

## Boxing/Unboxing
```java
// Boxing: primitive → wrapper
Integer boxed = Integer.valueOf(5);

// Unboxing: wrapper → primitive
int unboxed = boxed.intValue();
```S