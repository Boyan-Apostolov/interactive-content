# Overloading Methods

[slide hideTitle]

# Method Signature

In Java, a method signature is part of the method declaration.

It is the combination of the method name and the parameter list.

```Java
public static void print(String text) {
  System.out.println(text);
}
```

In this example, the signature elements are **print** and **String text**.

[/slide]

[slide hideTitle]
# Overloading Methods

Overloading methods is done by using the same name for multiple methods with different **signatures** \(method **name** and **parameters**\).

Instead of defining two methods that should do the same thing, it is better to overload one.

In the example below, we overload the **addTwoNumbers** method to work for both **int** and **double**:

```java live no-template
public class MyClass {
  static int addTwoNumbers(int x, int y) {
    return x + y;
  }

  static double addTwoNumbers(double x, double y) {
    return x + y;
  }

  public static void main(String[] args) {
    int myNum1 = addTwoNumbers(8, 5);
    double myNum2 = addTwoNumbers(4.3, 6.26);

    System.out.println("int: " + myNum1);

    System.out.println("double: " + myNum2);
  }
}
```

[/slide]

[slide hideTitle]
# Signature and Return Type

The method **signature** does not include the return type of the method.

A class cannot have two methods with the same signature.

If we try to declare two methods with the same signature we will get a compile-time error.

```Java
public static void print(String text) {
  System.out.println(text);
}

public static String print(String text) {
  return text;
}
// Compile-time error!
```
[/slide]

[slide hideTitle]
# Problem: Greater of Two Values
[code-task title="Problem: Greater of Two Values" taskId="java-fund-Methods-lab-Greater-of-Two-Values" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Description
You are given an input of two values of the same type.

The values can be of type **int**, **char**, or **String**.

Create a method called **getMax()** that returns the greater of the two values.

## Examples
|**Input**|**Output**|
| --- | --- | 
| int | 16 |
| 2 | |
| 16 | |

|**Input**|**Output**|
| --- | --- | 
| char | z |
| a | |
| z | |

|**Input**|**Output**|
| --- | --- |
| String | Manuel |
| Ann | |
| Manuel | |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
int
2
16
[/input]
[output]
16
[/output]
[/test]
[test]
[input]
char
a
z
[/input]
[output]
z
[/output]
[/test]
[test]
[input]
string
Ivan
Todor
[/input]
[output]
Todor
[/output]
[/test]
[test]
[input]
char
A
a
[/input]
[output]
a
[/output]
[/test]
[test]
[input]
int
123412
123
[/input]
[output]
123412
[/output]
[/test]
[test]
[input]
string
lorem ipsum
muspi merol
[/input]
[output]
muspi merol
[/output]
[/test]
[test]
[input]
string
Soft
Uni
[/input]
[output]
Uni
[/output]
[/test]
[test]
[input]
string
Programming Fundamentals
Software Technologies
[/input]
[output]
Software Technologies
[/output]
[/test]
[test]
[input]
char
1
2
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
string
123
234
[/input]
[output]
234
[/output]
[/test]
[test]
[input]
int
999999
888888
[/input]
[output]
999999
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Greater of Two Values
[code-task title="Solution: Greater of Two Values" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class GreaterOfTwoValues {
    public static void main(String[] args) {
        // Write your solution here
}
```
[/code-editor]
[task-description]
## Description
You are given an input of two values of the same type.

The values can be of type **int**, **char**, or **String**.

Create a method called **getMax()** that returns the greater of the two values.

## Examples
|**Input**|**Output**|
| --- | --- | 
| int | 16 |
| 2 | |
| 16 | |

|**Input**|**Output**|
| --- | --- | 
| char | z |
| a | |
| z | |

|**Input**|**Output**|
| --- | --- |
| String | Manuel |
| Ann | |
| Manuel | |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
int
2
16
[/input]
[output]
16
[/output]
[/test]
[test]
[input]
char
a
z
[/input]
[output]
z
[/output]
[/test]
[test]
[input]
string
Ivan
Todor
[/input]
[output]
Todor
[/output]
[/test]
[test]
[input]
char
A
a
[/input]
[output]
a
[/output]
[/test]
[test]
[input]
int
123412
123
[/input]
[output]
123412
[/output]
[/test]
[test]
[input]
string
lorem ipsum
muspi merol
[/input]
[output]
muspi merol
[/output]
[/test]
[test]
[input]
string
Soft
Uni
[/input]
[output]
Uni
[/output]
[/test]
[test]
[input]
string
Programming Fundamentals
Software Technologies
[/input]
[output]
Software Technologies
[/output]
[/test]
[test]
[input]
char
1
2
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
string
123
234
[/input]
[output]
234
[/output]
[/test]
[test]
[input]
int
999999
888888
[/input]
[output]
999999
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Multiply Evens by Odds
[code-task title="Problem: Multiply Evens by Odds" taskId="java-fund-Methods-lab-Multiply-Evens-by-Odds" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Description
Create a program that reads an **integer number** and **multiplies the sum of all its even digits** by **the sum of all its odd digits**:

## Examples
|**Input**|**Output**|**Comments**|
| --- | --- | --- |
| 12345 | 54 | 12345 has 2 even digits - 2 and 4. Even  |
| | | the even digits have sum of 6. |
| | | Also it has 3 odd digits - 1, 3 and 5.  |
| | | The odd digits have sum of 9. |
| | | Multiply 6 by 9 and you get 54. |


|**Input**|**Output**|
| --- | --- |
| -12345 | 54 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
12345
[/input]
[output]
54
[/output]
[/test]
[test]
[input]
-12345
[/input]
[output]
54
[/output]
[/test]
[test]
[input]
12211
[/input]
[output]
12
[/output]
[/test]
[test]
[input]
17
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
2222222
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
2222221
[/input]
[output]
12
[/output]
[/test]
[test]
[input]
12521234
[/input]
[output]
100
[/output]
[/test]
[test]
[input]
10000012
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
987654321
[/input]
[output]
500
[/output]
[/test]
[test]
[input]
-987654321
[/input]
[output]
500
[/output]
[/test]
[test]
[input]
-8811
[/input]
[output]
32
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Multiply Evens by Odds
[code-task title="Solution: Multiply Evens by Odds" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class MultiplyEvensByOdds {
    public static void main(String[] args) {
       // Write your solution here
}
```
[/code-editor]
[task-description]
## Description
Create a program that reads an **integer number** and **multiplies the sum of all its even digits** by **the sum of all its odd digits**:

## Examples
|**Input**|**Output**|**Comments**|
| --- | --- | --- |
| 12345 | 54 | 12345 has 2 even digits - 2 and 4. Even  |
| | | the even digits have sum of 6. |
| | | Also it has 3 odd digits - 1, 3 and 5.  |
| | | The odd digits have sum of 9. |
| | | Multiply 6 by 9 and you get 54. |


|**Input**|**Output**|
| --- | --- |
| -12345 | 54 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
12345
[/input]
[output]
54
[/output]
[/test]
[test]
[input]
-12345
[/input]
[output]
54
[/output]
[/test]
[test]
[input]
12211
[/input]
[output]
12
[/output]
[/test]
[test]
[input]
17
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
2222222
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
2222221
[/input]
[output]
12
[/output]
[/test]
[test]
[input]
12521234
[/input]
[output]
100
[/output]
[/test]
[test]
[input]
10000012
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
987654321
[/input]
[output]
500
[/output]
[/test]
[test]
[input]
-987654321
[/input]
[output]
500
[/output]
[/test]
[test]
[input]
-8811
[/input]
[output]
32
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
