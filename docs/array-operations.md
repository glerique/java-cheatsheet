# Array Operations in Java

```java
import java.util.Arrays;
import java.util.Collections;

// Sorting
Arrays.sort(arr);                                   // Sort in ascending order
Arrays.sort(objArray, Collections.reverseOrder());  // For Integer[], not int[]
Arrays.sort(objArray, (a, b) -> b - a);             // Custom sort (descending)

// Filling
Arrays.fill(arr, 0);                                // Fill entire array with value 0

// Copying
int[] copy = Arrays.copyOf(arr, arr.length);        // Create a new 