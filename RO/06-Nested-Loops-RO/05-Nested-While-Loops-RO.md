[slide hideTitle]

# Bucle Imbricate  While
Utilizarea buclelor imbricate  `while` este foarte similară cu cea a buclelor imbricate `for`.

Aceasta este sintaxa în Java:
```java
while (condition) {
  // Outer Loop 
  while (condition) {
    // Inner Loop
    
    // Statements
  }
}
```

# Exemplu

```java live
int i = 0;
int n = 5;
while (i < n) {
  System.out.printf("Value of i: %d%n", i);
  int j = 1;
  i++;

  while (j < n) {
    System.out.printf("  Value of j: %d%n", j);
    j++;
  }
}
```
[/slide]

[slide hideTitle]
# Problemă: Triangle of Stars with While
[code-task title="Triangle of Stars with While" taskId="java-basics-nested-loops-Triangle-of-Stars-with-While" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
# Descriere
Scrieți un program care:

* Citește **înălțimea** unui triunghi din consolă
* Imprimă un **triunghi din stele**
# Exemplu

| **Date de intrare** |**Date de ieșire**|
| ----- | ----- |
| 5 | \* |
|| \*\* |
|| \*\*\* |
|| \*\*\*\* |
|| \*\*\*\*\* |

[/task-description]
[tests]
[test]
[input]
4
[/input]
[output]
*
**
***
****
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Soluție: Triangle of Stars with While
[code-task title="Triangle of Stars with While" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Descriere
Scrieți un program care:

* Citește **înălțimea** unui triunghi din consolă
* Imprimă un **triunghi din stele**
# Exemplu

| **Date de intrare** |**Date de ieșire**|
| ----- | ----- |
| 5 | \* |
|| \*\* |
|| \*\*\* |
|| \*\*\*\* |
|| \*\*\*\*\* |

[/task-description]
[tests]
[test]
[input]
4
[/input]
[output]
*
**
***
****
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]

# Example: Combining while and for Loops

interactive-programming-basics-with-java-nested-loops-33-nesting-while-and-for-loops + 

interactive-programming-basics-with-java-nested-loops-34-problem-and-solution-sum-digits-calcuulator


[/slide]