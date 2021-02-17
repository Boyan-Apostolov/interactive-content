# Built-in API Classes

[slide hideTitle]
# Built-in Classes in Java

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-8-9-built-in-api-classes-in-java-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Java provides **ready-to-use** classes, which are organized inside **Packages**. 

These classes provide **predefined methods** and **fields** that help to save time and effort in writing code and repeating it.

Some of these methods are:

- `java.util.Scanner` 

- `java.utils.List` 

- `java.lang.Math` 

- `java.math.BigInteger`

Using **static** Java classes and their methods requires only calling the class name and the needed method:

```java
LocalDateTime today = LocalDateTime.now();
double cosine = Math.cos(Math.PI);
```

Using **non-static** Java classes and their methods requires creating object (instance) of the current class:

```java
Random rnd = new Random();
int randomNumber = rnd.nextInt(10);
```
[/slide]


[slide hideTitle]
# Math

`Math` class methods are **static** and help performing the **numeric operations** and commonly used **mathematical functions** like:

- Rounding

- Comparing

- Square root

- Cube root

- Exponential

- Logarithm

- Trigonometric operations

`Math` methods include:

- `abs(a)` - Returns the absolute value of the passed parameter `a`

```java live
int a = Math.abs(5);
int b = Math.abs(-10);
System.out.println(a);
System.out.println(b);
```

- `ceil(a)` - Rounds a floating point value `a` up to the nearest integer value, returned as a `double`

```java live
double ceil = Math.ceil(8.357);
System.out.println(ceil);
```

- `floor(a)` - Rounds a floating point value `a` down to the nearest integer value, returned as a `double`

```java live
double floor = Math.floor(8.357);
System.out.println(floor);
```

- `max(a, b)` - Returns the largest of two values passed as parameter

```java live
int max = Math.max(5, 10);
System.out.println(max);
```

- `min(a, b)` - Returns the smallest of two values passed as parameter

```java live
int min = Math.min(5, 10);
System.out.println(min);
```

- `round(a)` - Rounds a float or double to the nearest integer using normal math round rules (either up or down)

```java live
double roundedDown = Math.round(29.459);
double roundedUp = Math.round(29.549);
System.out.println(roundedDown);
System.out.println(roundedUp);
```

- `pow(a, b)` - Returns the value of the first parameter `a` raised to the power of the second parameter `b`

```java live
double number = Math.pow(3,2);
System.out.println(number);
```

- `sqrt(a)` - Calculates the square root of the given parameter `a`

```java live
double number = Math.sqrt(9);
System.out.println(number);
```

- `toDegrees(a)` - Converts an angle in radians to degrees

```java live
double degrees = Math.toDegrees(3.141592653589793);
System.out.println(degrees);
```

- `toRadians(a)` - Reverse of `toDegrees`, converts an angle in degrees to radians

```java live
double radians = Math.toRadians(180);
System.out.println(radians);
```

- Trigonometric Functions - Calculate the value of angles in radians `sin(a)` `cos(a)` `tan(a)`
[/slide]


[slide hideTitle]
# Random

The class `java.util.Random` is used to generate random numbers of types **integer**, **float**, **double**, **long**. 

It can also generate a random boolean type and return a result between `true` or `false`.

Random class methods are **not-static**.

The following code is an example of how to create a `Random` **instance**:

```java
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Random random = new Random();
    }
}
```

These are some of the `Random` methods:

- `nextInt()` - Returns the next pseudorandom `int` value from random number sequence. 

```java live
Random random = new Random();
int number = random.nextInt();
System.out.println(number);
```

- `nextInt(n)` - Returns the next pseudorandom `int` value in the range from 0 to 9 both inclusive

```java live
Random random = new Random();
int numOne = random.nextInt(10);
int numTwo = random.nextInt(10);
System.out.println(numOne);
System.out.println(numTwo);
```

- `nextDouble()` - Returns the next pseudorandom `double` value in the range from 0.0 to 1.0

```java live 
Random random = new Random();
double numOne = random.nextDouble();
double numTwo = random.nextDouble();
System.out.println(numOne);
System.out.println(numTwo);
```

- `nextBoolean()` - Returns the next pseudorandom `boolean` value, which can either be `true` or `false`

```java live
Random random = new Random();
boolean isValid = random.nextBoolean();
System.out.println(isValid);
```

[/slide]

[slide hideTitle]
# Problem with Solution: Randomize Words

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-10-problem-and-solution-randomize-words-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Randomize Words" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Random;
import java.util.Scanner;

public class RandomizeWords {
    public static void main(String[] args) {
       
    // Write your code here
}
```
[/code-editor]
[task-description]
## Description
You are given a **list of words in one line**.

**Randomize their order** and print **each word at a separate line**.

## Examples

| **Input** | **Output** | **Comments** |
| --- | --- | --- |
| Welcome to SoftUni and have fun learning programming | learning | The order of the words in the output will be different after each program execution. |
| | Welcome | |
| | SoftUni | |
| | and | |
| | fun | |
| | programming | |
| | have | |
| | to | |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
Welcome to SoftUni and have fun learning programming
[/input]
[output]
learning
Welcome
SoftUni
and
fun
programming
have
to
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# BigInteger

The `java.math.BigInteger` class provides **operations analogues** to all of Java's **primitive integer operations** and for **all relevant methods** from `java.lang.Math;`.

The `BigInteger` class helps dealing with **very large Integers**. 

BigInteger class methods are **non-static**.

This is how to declare a BigInteger: 

- `BigInteger num = BigInteger.valueOf(1234567890);` 
  - the number `1234567890` is a `long` variable (64 bits)

- `BigInteger num = new BigInteger("12345688901234567890");`
  - the number `12345688901234567890` is too large and cannot fit in 64bits, so the parameter is a **numeric String**

The `BigInteger` **fields** are:

- `BigInteger.ONE` - Constant one

- `BigInteger.ZERO` - Constant zero

- `BigInteger.TEN` - Constant ten

The `BigInteger` **methods** are:

- `abs()` - Returns the absolute value of current BigInteger

```java live
BigInteger number = BigInteger.valueOf(-123);
number = number.abs();
System.out.println(number);
```

- `add(value)` - Assigns **new value** to current BigInteger, performs **addition** (current + value)

```java live
BigInteger number = BigInteger.valueOf(123);
number = number.add(BigInteger.TEN);
System.out.println(number);
```

- `subtract(value)` - Assigns **new value** to current BigInteger, performs **subtraction** (current - value)

```java live
BigInteger number = BigInteger.valueOf(123);
number = number.subtract(BigInteger.TEN);
System.out.println(number);
```

- `multiply(value)` - Assigns **new value** to current BigInteger, performs **multiplication** (current * value)

```java live
BigInteger number = BigInteger.valueOf(123);
number = number.multiply(BigInteger.TEN);
System.out.println(number);
```

- `divide(value)` - Assigns **new value** to current BigInteger, performs **division** (current / value)

```java live
BigInteger number = BigInteger.valueOf(123);
number = number.divide(BigInteger.TEN);
System.out.println(number);
```

- `pow(value)` - Assigns **new value** to current BigInteger, performs **power raise** (current ^ value)

```java live
BigInteger number = BigInteger.valueOf(123);
number = number.pow(2);
System.out.println(number);
```

- `intValue()` - Converts to an `int`

- `doubleValue()` - Converts to a `double`

- `toString()` - Returns the decimal String representation

[/slide]

[slide hideTitle]
# Problem with Solution: Sum Big Numbers

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-problem-and-solution-sum-big-numbers-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Sum Big Numbers" taskId="java-fund-16-Objects-and-Classes-problem-5" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;
import java.math.BigInteger;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
You will receive two numbers **(0 to 10 ^ 50)**, print their sum.

## Examples

| **Input** | **Output** |
| --- | --- |
| 923847238931983192462832102 | 934573817465075391826664309019448 |
| 934572893617836459843471846187346 | |

| **Input** | **Output** |
| --- | --- |
| 4 | 104 | 
| 100 | | 



[/task-description]
[code-io /]
[tests]
[test open]
[input]
4
100
[/input]
[output]
104
[/output]
[/test]
[test open]
[input]
923847238931983192462832102
934572893617836459843471846187346
[/input]
[output]
934573817465075391826664309019448
[/output]
[/test]
[test]
[input]
1234567890
1234567890
[/input]
[output]
2469135780
[/output]
[/test]
[test]
[input]
129830419415091450143
3478410041470111511474904
[/input]
[output]
3478539871889526602925047
[/output]
[/test]
[test]
[input]
999999999999999999999999999999999999999
9999999999999999999999999999999999
[/input]
[output]
1000009999999999999999999999999999999998
[/output]
[/test]
[test]
[input]
00001
0000002
[/input]
[output]
3
[/output]
[/test]
[test]
[input]
982374328974238974913824792347
3127642874284682374
[/input]
[output]
982374328977366617788109474721
[/output]
[/test]
[test]
[input]
9999
1
[/input]
[output]
10000
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem with Solution: Big Factorial

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-12-problem-and-solution-big-factorial-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Big Factorial" taskId="java-fund-16-Objects-and-Classes-problem-6" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;
import java.math.BigInteger;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
You will receive N – number in range **\[0 – 1000]**.

Calculate **Factorial of N** and print the result.

## Examples

| **Input** | **Output** |
| --- | --- |
| 5 | 120 |

| **Input** | **Output** |
| --- | --- |
| 50 | 30414093201713378043612608166064768844377641568960512000000000000 |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
[/input]
[output]
120
[/output]
[/test]
[test open]
[input]
50
[/input]
[output]
30414093201713378043612608166064768844377641568960512000000000000
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
3628800
[/output]
[/test]
[test]
[input]
12
[/input]
[output]
479001600
[/output]
[/test]
[test]
[input]
88
[/input]
[output]
185482642257398439114796845645546284380220968949399346684421580986889562184028199319100141244804501828416633516851200000000000000000000
[/output]
[/test]
[test]
[input]
101
[/input]
[output]
9425947759838359420851623124482936749562312794702543768327889353416977599316221476503087861591808346911623490003549599583369706302603264000000000000000000000000
[/output]
[/test]
[test]
[input]
250
[/input]
[output]
3232856260909107732320814552024368470994843717673780666747942427112823747555111209488817915371028199450928507353189432926730931712808990822791030279071281921676527240189264733218041186261006832925365133678939089569935713530175040513178760077247933065402339006164825552248819436572586057399222641254832982204849137721776650641276858807153128978777672951913990844377478702589172973255150283241787320658188482062478582659808848825548800000000000000000000000000000000000000000000000000000000000000
[/output]
[/test]
[test]
[input]
333
[/input]
[output]
10334465434588059156093965538297516550622260041682062823432902469783188597914276568552700194849877929894375950252570477080418352732597658745665925604704669227133726477243854317836635130694123893711638533001980496229875665476598568821806170303765540489814402234159901540440432134155844542962445153646330595588291605924429211352279943471372817279938720974895260387784578239150931816946786416232516666251965421919651838044618050991294403546958930745419743836966520198735201123255884089263272829846640538826979843642885775791641575109178753509580001660392092396798648924375401024147883702298145910046889402880394195369984000000000000000000000000000000000000000000000000000000000000000000000000000000000
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

