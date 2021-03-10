[slide hideTitle]
# More Complex Conditions

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/03-conditional-statements-advanced/EN/interactive-programming-basics-with-java-conditional-statements-advanced-16-18-logical-operators-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Let us take a look at how we can create more **complex logical conditions** in programming. 

We can use the following logical operators:
* **"AND"** (`&&`)
* **"OR"** (`||`)
* **Negation** (`!`) 
* **Parentheses** (`()`)

# Logical "AND", "OR" and "NOT"
This is a short example that demonstrates the usage of logical **"AND"**, logical **"OR"** and logical **"NOT"**:
```java
Scanner scanner = new Scanner(System.in);
String animal = scanner.nextLine();
int speed = Integer.parseInt(scanner.nextLine());

if ((animal == "horse" || animal == "donkey") && (speed > 40)) {
    System.out.println("Galloping");
} else if ((animal == "shark" || animal == "dolphin") && (speed > 45)) {
    System.out.println("Swimming fast");
} else if (!(speed > 30 || animal == "turtle")) {
    System.out.println("Moving slow");
}
```

Let us explain the logical **AND** (`&&`), the logical **OR** (`||`), and the logical **NOT** (`!`) in the next few sections, along with examples and exercises.
[/slide]

[slide hideTitle]
# The Logical AND Operator

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/03-conditional-statements-advanced/EN/interactive-programming-basics-with-java-conditional-statements-advanced-19-logical-and-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

As we saw, in some tasks we have to perform **more than one check at once**. 

The logical **AND** (operator `&&`) means a some conditions have to be **fulfilled simultaneously**. 

We can use the logical **AND** to simplify our code and avoid unnecesary constructions such as nesting too many conditional statements.

The following table visualizes the outcome of all possible combinations when using this operator:

| Operand1 | Operand2 | AND |
|---|---|---|---|
| true | true | true |
| true | false | false |
| false | true | false |
| false | false | false |

## How Does the `&&` Operator Work?

The `&&` operator accepts **two Boolean** (conditional) statements, which have a `true` or a `false` value, and returns a boolean value.

Using it instead of a couple of nested `if` blocks, makes the code **more legible**, **ordered** and **easy** to maintain. 

There is a particular exectution flow when using more than one logical operator.

As we saw, the logical **AND** returns `true` **only** when both its operands are `true`.

So a sequence of logical **AND** comparisons returns `false` as a result if one of the boolean variables is `false` and `true` if all variables hold `true` values.

## Example
```java live
boolean a = true;
boolean b = true;
boolean c = false;
boolean d = true;
boolean result = a && b && c && d;
System.out.println(result);
```

The program will run in the **following** way: 
- **It starts** from `a`, **reads** it and accepts that it has a `true` value, after which it **checks** `b`
- After it has **processed** that `a` and `b` both return `true`, **it checks the next** argument
- The program reads the value of `c`, which is `false`
- After the program accepts that the argument `c` has a `false` value, it exits the expression, returning a `false` value
- The evaluation of `d` will be **skipped** 

## Example: Point in a Rectangle
Write a piece of code which checks whether a point with `x`, `y` coordinates is placed **inside a rectangle** `{x1, y1}` – `{x2, y2}`. 

[image assetsSrc="03.Point-in-rectangle-01.png" /]

The input data is read from the console and consists of 6 lines: 
- the numbers: `x1`, `y1`, `x2`, `y2`, `x`, `y` (it is guaranteed that `x1 < x2` and `y1 < y2`).

## Sample Input and Output
|Input|Output|
|-----|------|
|2|Inside|
|-3||
|12||
|3||
|8||
|-1||

## Solution
A point is internal for a given polygon, if the following four conditions are applied at the same time:
-  The point is placed to the right from the left side of the rectangle
-  The point is placed to the left from the right side of the rectangle
-  The point is placed downwards from the upper side of the rectangle
-  The point is placed upwards from the down side of the rectangle

```java live
double x1 = 2;
double y1 = -3;
double x2 = 12;
double y2 = 3;

double x = 8;
double y = -1;

if (x >= x1 && x <= x2 && y >= y1 && y <= y2) {
    System.out.println("Inside");
} else {
    System.out.println("Outside");
}
```
[/slide]

[slide hideTitle]
# Problem with Solution: Bonus Points

interactive-programming-basics-with-java-conditional-statements-advanced-19-logical-and-problem-bonus-points

[code-task title="Bonus Points" taskId="java-basics-logical-operators-bonus-points" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
# Description
Create a program that receives a number as input, and adds another number to it, according to the following rules:

  * If the input number is between **0** and **3**, adds **5**
  * If the input number is between **4** and **6**, adds **15**
  * If the input number is between **7** and **9**, adds **20**
# Example

| Input | Output |
| --- | --- |
| 4 | 19 |

[/task-description]
[tests]
[test]
[input]
4
[/input]
[output]
19
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
28
[/output]
[/test]
[test]
[input]
1
[/input]
[output]
6
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]



[slide hideTitle]
## Logical OR Operator

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/03-conditional-statements-advanced/EN/interactive-programming-basics-with-java-conditional-statements-advanced-21-logical-or-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

The logical **OR** (operator `||`) means that **at least one** of a few conditions is fulfilled. 

Similar to the operator `&&`, the logical **OR** accepts a few arguments of **bool** (conditional) type and returns `true` or `false`. 

We can easily guess that we **obtain** a value `true` every time when at least one of the arguments has a `true` value. 

| Operand1 | Operand2 | OR |
|---|---|---|---|
| true | true | true |
| true | false | true |
| false | true | true |
| false | false | false |

At school the teacher says: "John or Peter should clean the board". To fulfill this condition (to clean the board), it is possible either just for John to clean it, or just for Peter to clean it, or both of them to do it.

# How Does the `||` Operator Work?
We have already learned what the logical **OR** represents. But how is it actually being achieved? 

Just like with the logical **"AND"**, the program **checks** from left to right **the arguments** that are given. 

In order to obtain `true` from the expression, it is necessary for **just one** argument to have a `true` value. 

Respectively, the checking **continues** until an **argument** with **such** value is met or until the arguments **are over**.

Here is one **example** of the `||` operator in action:

```java live
boolean a = false;
boolean b = true;
boolean c = false;
boolean d = true;
boolean result = a || b || c || d;
System.out.println(result);
```

The programs **checks** `a`, accepts that it has a value `false` and continues. 

Reaching `b`, it understands that it has a `true` value and the whole **expression** is calculated as `true`, without having to check `c` or `d`, because their values **wouldn't change** the result of the expression.
[/slide]

[slide hideTitle]
# Problem with Solution: Food or Drink

interactive-programming-basics-with-java-conditional-statements-advanced-21-logical-or-problem-food-or-drink

[code-task title="Food or Drink" taskId="java-basics-logical-opators-food-ot-drink" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
# Description
Write a program, which:
  * Reads single line and print "***drink***", "***food***" or "***unknown***"
  * Foods: curry, noodles, sushi, spaghetti 
  * Drinks: tea, water, coffee
  * Everything else is unknown
# Example
## Input
- curry
## Output
- food
## Input
- flower
## Output
- unknown
[/task-description]
[tests]
[test]
[input]
curry
[/input]
[output]
food
[/output]
[/test]
[test]
[input]
tea
[/input]
[output]
drink
[/output]
[/test]
[test]
[input]
something
[/input]
[output]
unknown
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]
[/slide]




[slide hideTitle]
# Logical NOT Operator

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/03-conditional-statements-advanced/EN/interactive-programming-basics-with-java-conditional-statements-advanced-23-logical-not-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Logical negation (operator **!**) means a given condition is **not fulfilled**.

| a | !a |
|---|---|
| true | false |

The operator `!` accepts as an **argument** a bool variable and **returns** its value.

# Example: Invalid Number
A given **number is valid** if it is in the range **\[100 … 200\]** or it is **0**. Do a validation for an **invalid** number.

For example, `75` and `220` are **invalid**, but `150` is **valid**.

```java live
int num = 75;

boolean inRange = (num >= 100 && num <= 200) || num == 0;
if (!inRange) {
    System.out.println("invalid");
}
```
[/slide]

[slide hideTitle]
# The Parenthesis  Operator

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/03-conditional-statements-advanced/EN/interactive-programming-basics-with-java-conditional-statements-advanced-23-logical-not-demo-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Like the rest of the operators in programming, the operators `&&` and `||` have a priority, as in the case `&&` is with higher priority than `||`. 

The operator `()` serves for **changing the priority of operators** and is being calculated first, just like in maths. 

Using parentheses also gives the code better readability and is considered a good practice.

Example of checking whether a variable belongs to certain ranges:
```java 
if (x < 0) || ((x >= 5) && (x <= 10)) || (x > 20) {
    // Commands
}
```
[/slide]
