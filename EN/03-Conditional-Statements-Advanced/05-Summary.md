[slide hideTitle]
# Summary

# In this lesson we learned: 

interactive-programming-basics-with-java-conditional-statements-advanced-51-summary

- What are nested conditional statements

  * if-else inside another if-else


```java
if (condition1) {
    if (condition2) {
        // body; 
    } else {
        // body;
    }
}
```

- Logical Operators  

  * && , || , ! operators 

``` java
  if ((animal == "horse" || animal == "donkey") && (speed > 40)) {
    System.out.println("Run fast");
} else if ((animal == "shark" || animal == "dolphin") && (speed > 45)) {
    System.out.println("Swim fast");
} else if (!(speed > 30 || animal == "turtle")) {
    System.out.println("Move slow");
}
```

- Conditional Statement - **Switch-Case**

```java
switch (selector) {
  case value1:
    statements;
    break;
  case value2:
    statements;
    break;
}
```

  * Multiple Labels in **Switch-Case**

## In the next lesson we will learn:

- **Incrementing** and **Decrementing** Operators

- Repeating blocks of code

  * for-loops

- For loop with a **Step**

- Iterating over Characters using loops

- **Infinity** loops

  * How to avoid them


[/slide]