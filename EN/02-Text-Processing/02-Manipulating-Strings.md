[slide hideTitle]
# Concatenating

There are **two** ways to concatenate a `String`:

- Using `+` or `+=` operators

```java live
String text = "Hello" + ", " + "SoftUni";

text += "!";

System.out.println(text); // "Hello, SoftUni!"
```

- Using `concat()` method

```java live
String greet = "Hello, ";

String name = "SoftUni!";

String result = greet.concat(name);

System.out.println(result); // "Hello, SoftUni!"
```

[/slide]

[slide hideTitle]

# Substring

As the name suggests, `substring` extracts only a **part** of a `String`.

- `substring(int startIndex)` - Returns a **new String** containing the substring of the given string from specified **startIndex** (**inclusive**)

```java live
String text = "My name is John";

String extractWord = text.substring(11);

System.out.println(extractWord); // John
```

- `substring(int startIndex, int endIndex)` - Returns **new String** containing the substring of the given string from specified **startIndex** (inclusive) to **endIndex** (exclusive)


```java live
String fullName = "John Doe";

String firstName = fullName.substring(0, 4);

System.out.println(firstName); // John
```

[/slide]

[slide hideTitle]

# Searching

It is possible to search for the first or last occurences of a pattern in a string:

- `indexOf()` - Returns the **first match index**, if there is **no match** returns **-1**

```java live 
String fruits = "banana, apple, kiwi, banana, apple";

System.out.println(fruits.indexOf("banana"));    // 0

System.out.println(fruits.indexOf("orange"));    // -1
```

- `lastIndexOf()` - Finds the last occurrence

```java live
String fruits = "banana, apple, kiwi, banana, apple";

System.out.println(fruits.lastIndexOf("banana")); // 21

System.out.println(fruits.lastIndexOf("orange")); // -1
```
[/slide]

[slide hideTitle]

# Splitting

A `String` could be split by **one** or **multiple** criteria, using the `split()` method.
 
- Splitting a string by a given **pattern**

```java live
String text
 = "I had coffee, pancakes, berries and a banana for breakfast.";
String[] words = text.split(", ");

System.out.println(words[0]);
System.out.println(words[1]);
System.out.println(words[2]);
```

- Splitting by **multiple separators**

```java live

String text = "Hello, I am John.";

// splits text by comma, whitespace or dot
String[] words = text.split("[, .]+");

System.out.println(String.join(", ",words));
```

[/slide]

[slide hideTitle]

# Replacing

Java also makes it possible to make **replacements** in a String.

- `replace(match, replacement)` - **Replaces all occurrences** and returns a **new String** (Strings are immutable)

```java live
String text = "I have three bananas, three oranges, three apples.";

String replacedText = text.replace("three", "five");

System.out.println(replacedText);
```

[/slide]

[slide hideTitle]
# Problem with Solution: Repeat strings
[code-task title="Repeat strings" taskId="Java-Fundamentals-Part-Two-String-Processing-Repeat-Strings" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that reads an **array of strings**.

Each string is repeated **n** times, where **n** is the **length of the string**.

## Examples
| **Input** | **Output** |
| --- | --- |
| hi abc add | hihiabcabcabcaddaddadd |


| **Input** | **Output** |
| --- | --- |
| work | workworkworkwork |


| **Input** | **Output** |
| --- | --- |
| ball | ballballballball |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
hi abc add
[/input]
[output]
hihiabcabcabcaddaddadd
[/output]
[/test]
[test open]
[input]
work
[/input]
[output]
workworkworkwork
[/output]
[/test]
[test open]
[input]
ball
[/input]
[output]
ballballballball
[/output]
[/test]
[test]
[input]
spot exempt
[/input]
[output]
spotspotspotspotexemptexemptexemptexemptexemptexempt
[/output]
[/test]
[test]
[input]
church lamp pier
[/input]
[output]
churchchurchchurchchurchchurchchurchlamplamplamplamppierpierpierpier
[/output]
[/test]
[test]
[input]
peace glide
[/input]
[output]
peacepeacepeacepeacepeaceglideglideglideglideglide
[/output]
[/test]
[test]
[input]
headquarters baseball
[/input]
[output]
headquartersheadquartersheadquartersheadquartersheadquartersheadquartersheadquartersheadquartersheadquartersheadquartersheadquartersheadquartersbaseballbaseballbaseballbaseballbaseballbaseballbaseballbaseball
[/output]
[/test]
[test]
[input]
linear
[/input]
[output]
linearlinearlinearlinearlinearlinear
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem with Solution: Substring
[code-task title="Substring" taskId="Java-Fundamentals-Part-Two-String-Processing-Substring" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
On the **first line** you will receive a **string**.

On the **second line** you will receive a **second string**.

Write a program that **removes all of the occurrences** of **the first string** in **the second** until there is no match.

At the end **print the remaining string**.

## Examples
| **Input** | **Output** |
| --- | --- |
| ice | kgb |
| kicegiciceeb |  |

# Hints
- **Read the input.**
- Find the **first index** where the key appears.
	- Use the built-in method `indexOf()` 
- **Remove the match**.
	- Use the built-in method `replace(String oldValue, String newValue)`
- **Repeat** it until the text **doesn't contain the key anymore**.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
ice
kicegiciceeb
[/input]
[output]
kgb
[/output]
[/test]
[test]
[input]
e
fixture
[/input]
[output]
fixtur
[/output]
[/test]
[test]
[input]
f
coffin
[/input]
[output]
coin
[/output]
[/test]
[test]
[input]
in
coffiinncoffin
[/input]
[output]
coffcoff
[/output]
[/test]
[test]
[input]
ice
pricekicegiciceeb
[/input]
[output]
prkgb
[/output]
[/test]
[test]
[input]
reg
rrregegegstration
[/input]
[output]
stration
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem with Solution: Text Filter
[code-task title="Text Filter" taskId="Java-Fundamentals-Part-Two-String-Processing-Text-Filter" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that takes a **text** and a **string of banned words**.

**All words included** in the **ban list** should be **replaced** with **asterisks** \"__\*__\", equal to the **word's length.**

The entries in the ban list will be separated by a **comma** and **space** ", ".

## Examples
| **Input** | **Output** |
| --- | --- |
| Linux, Windows | It is not \*\*\*\*\*, it is GNU/\*\*\*\*\*. \*\*\*\*\* is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/\*\*\*\*\*! Sincerely, a \*\*\*\*\*\*\* client |
| It is not Linux, it is GNU/Linux. Linux is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/Linux! Sincerely, a Windows client |  |


# Hints  
- **Read the input**.
- **Replace all ban words** in the text **with** **asterisk** \(__\*__\).
	- Use the **built-in method** `replace(banWord, replacement)`.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Linux, Windows
It is not Linux, it is GNU/Linux. Linux is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/Linux! Sincerely, a Windows client
[/input]
[output]
It is not \*\*\*\*\*, it is GNU/\*\*\*\*\*. \*\*\*\*\* is merely the kernel, while GNU adds the functionality. Therefore we owe it to them by calling the OS GNU/\*\*\*\*\*! Sincerely, a \*\*\*\*\*\*\* client
[/output]
[/test]
[test]
[input]
framework, structure, something
In general, a framework is a real or conceptual structure intended to serve as a support or guide for the building of something that expands the structure into something useful.
[/input]
[output]
In general, a \*\*\*\*\*\*\*\*\* is a real or conceptual \*\*\*\*\*\*\*\*\* intended to serve as a support or guide for the building of \*\*\*\*\*\*\*\*\* that expands the \*\*\*\*\*\*\*\*\* into \*\*\*\*\*\*\*\*\* useful.
[/output]
[/test]
[test]
[input]
computer, programming, set
In computer programming, an application programming interface (API) is a set of subroutine definitions, communication protocols, and tools for building software.
[/input]
[output]
In \*\*\*\*\*\*\*\* \*\*\*\*\*\*\*\*\*\*\*, an application \*\*\*\*\*\*\*\*\*\*\* interface (API) is a \*\*\* of subroutine definitions, communication protocols, and tools for building software.
[/output]
[/test]
[test]
[input]
view, engine
View engine gives the ability to render the HTML from your view to the browser. There are many view engines supported by ASP.NET MVC but the most widely used view engines are. Web form / ASPX view engine. Razor view engine.
[/input]
[output]
View \*\*\*\*\*\* gives the ability to render the HTML from your \*\*\*\* to the browser. There are many \*\*\*\* \*\*\*\*\*\*s supported by ASP.NET MVC but the most widely used \*\*\*\* \*\*\*\*\*\*s are. Web form / ASPX \*\*\*\* \*\*\*\*\*\*. Razor \*\*\*\* \*\*\*\*\*\*.
[/output]
[/test]
[test]
[input]
Controller, interface
Model View Controller (MVC) is a software architecture pattern, commonly used to implement user interfaces.
[/input]
[output]
Model View \*\*\*\*\*\*\*\*\*\* (MVC) is a software architecture pattern, commonly used to implement user \*\*\*\*\*\*\*\*\*s.
[/output]
[/test]
[test]
[input]
object, programming
object-relational mapping (ORM, O/RM, and O/R mapping tool) in computer science is a programming technique for converting data between incompatible type systems using object-oriented programming languages.
[/input]
[output]
\*\*\*\*\*\*-relational mapping (ORM, O/RM, and O/R mapping tool) in computer science is a \*\*\*\*\*\*\*\*\*\*\* technique for converting data between incompatible type systems using \*\*\*\*\*\*-oriented \*\*\*\*\*\*\*\*\*\*\* languages.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
