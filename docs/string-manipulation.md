## String Manipulation

### String Basics
```java
String s = "hello";
s.length();                // 5
s.charAt(0);               // 'h'
s.substring(1, 4);         // "ell"
s.indexOf("l");            // 2 (first occurrence)
s.lastIndexOf("l");        // 3 (last occurrence)
```

### String Transformations
```java
s.toUpperCase();           // "HELLO"
s.toLowerCase();           // "hello"
s.trim();                  // removes whitespace from both ends
s.replace("l", "p");       // "heppo"
s.contains("el");          // true
s.startsWith("he");        // true
s.endsWith("lo");          // true
```

### String Splitting and Joining
```java
String[] parts = "a,b,c".split(",");  // ["a", "b", "c"]
String joined = String.join("-", parts); // "a-b-c"
```

### StringBuilder for Efficient String Concatenation
```java
StringBuilder sb = new StringBuilder();
sb.append("hello").append(" ").append("world");
String result = sb.toString();  // "hello world"
```