[slide hideTitle]
# Integer types

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/01.Java-Fundamentals-Data-types-and-variables/EN/interactive-java-fundamentals-data-types-and-variables-12-15-integer-types-and-demo-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

**Integer types** store whole numbers, positive or negative (such as 123 or -456), without decimals.

**Byte**, **short**, **int**, and **long** are all integer data types. Choosing which one to use, depends on the numeric value it will need to store.

|Type| Default Value | Min Value | Max Value| Size |
|-----|------|-----|------|-----|
| byte | 0 | -128 | 127 | 8 bit |
| short | 0 | -32768 | 32767 | 16 bit |
| int | 0 | -2147483648 | 2147483647 | 32 bit |
| long | 0 | -9223372036854775808 | 9223372036854775807 | 64 bit |

[/slide]

[slide hideTitle]
# Example: Centuries

```java live
byte centuries = 20; 
short years = 2000; 
int days = 730484;
long hours = 17531616; 

System.out.printf("%d centuries = %d years = %d days = %d hours.", 
                                    centuries, years, days, hours)
//20 centuries = 2000 years = 730484 days = 17531616 hours.
```

We can use different integer types, depending on what we want to store in them. 

- The *byte** data type can be used for storing whole numbers from -128 to 127

**Byte** can be used instead to save memory when you are certain that the value will be within -128 to 127:

```java live
byte myNum = 100;
System.out.println(myNum);
```

- The **Short** data type can be used to store whole numbers from -32768 to 32767:

```java live
short myNum = 5000;
System.out.println(myNum);
```

- The **Int** data type can store whole numbers from -2147483648 to 2147483647

In general, the **int** data type is the preferred data type when we create variables with a numeric value.

```java live
int myNum = 100000;
System.out.println(myNum);
```

- **Long** data type can store whole numbers from -9223372036854775808  to 9223372036854775807

This is used when an int is not large enough to store the value.

Note that you should end the value with an "L":

```java live
long myNum = 15000000000L;
System.out.println(myNum);
```
[/slide]

[slide hideTitle]
# Integer Overflow

All integers have a range - a minimum and maximum value. This means that integers can overflow, resulting in incorrect values. 

Take a look at the below example.

```java
byte counter = 0;
for (int i = 0; i < 130; i++) {
  counter++;
  System.out.println(counter);
}

//1
//2
//…
//127
//-128
//-127
```

The counter variable starts from 0 and is incremented with each step of the for loop. Eventually when it reaches the maximum value of byte (127), it restarts again from the minimum value (-128). This is what we mean by **integer overflow** and it is precisely the reason why choosing your data type correctly is important. 

[/slide]

[slide hideTitle]
# Integer Literals

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/01.Java-Fundamentals-Data-types-and-variables/EN/interactive-java-fundamentals-data-types-and-variables-16-integer-literals-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Integer literals are numbers, which do not have a floating point part. **541** is a literal value by that definition. A

They can be represented in a few different ways, which are not as intuitive:

- **hexadecimal integer literals** - values beginning with **0x** and **OX** - **0xFE**, **0xA8F1**, **0xFFFFFFFF**

- **long integer literals** - values preceded by the letter **L** or **l** - **9876543L**, **0L**

```java live
int hexadecimal = 0xA8F1; //43249
long number = 1L; //1

System.out.println("hexadecimal: ", hexadecimal);
System.out.println("long: ", number);
```

[/slide]


[slide hideTitle]
# Problem with Solution: Convert Meters to Kilometers

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/01.Java-Fundamentals-Data-types-and-variables/EN/interactive-java-fundamentals-data-types-and-variables-17-problem-and-solution-convert-meters-to-kilometers-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Problem: Convert Meters to Kilometers" taskId="java-fund-data-types-lab-convert-meters-to-kilometers-problem" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your solution here
    }
}
```
[/code-editor]
[task-description]
## Description
You will be given an integer. It will be used to store a given distance in meters.

Create a program that converts meters to kilometers, formatted to the second decimal point.

## Examples
|**Input**|**Output**|
|-----|------|
| 1852 | 1.85 |
| 798 | 0.80 |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
1852
[/input]
[output]
1.85
[/output]
[/test]
[test open]
[input]
798
[/input]
[output]
0.80
[/output]
[/test]
[test]
[input]
5000
[/input]
[output]
5.00
[/output]
[/test]
[test]
[input]
825
[/input]
[output]
0.83
[/output]
[/test]
[test]
[input]
1254
[/input]
[output]
1.25
[/output]
[/test]
[test]
[input]
2450
[/input]
[output]
2.45
[/output]
[/test]
[test]
[input]
4589
[/input]
[output]
4.59
[/output]
[/test]
[/tests]
[/code-task]
[/slide]