# Problem: Family Trip
[slide hideTitle]
# Family Trip
[code-task title="Family Trip" taskId="pb-java-exam-family-trip" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```java
import java.util.Scanner;

public class Program {
  public static void main(String[] args) {
    // Write code here
  }
}
```
[/code-editor]
[task-description]
## Description
The Smiths are planning their family trip. 

Your task is to create a program that calculates whether their budget will be sufficient, knowing how many nights they have planned to stay, what the price per night is and what percentage of their budget must be spent on additional costs.

Keep in mind that if they stay longer than 7 nights, the price per night should be reduced by 5%.

## Input
You will receive **4 lines of input**:
- The budget that they have - **a real number** in range [1.00 ... 10000.00] 
- The number of nights - **an integer** in range [0 ... 1000] 
- The price per night - **a real number** in range [1.00 ... 500.00] 
- The additional cost percentage - **an integer** in range [0 ... 100] 

## Output
The output depends on whether the budget is sufficient or not:
- If the budget **is sufficient**:
	- "**The Smiths will be left with** \{**money left after the trip**\} **dollars after the vacation.**"
- If the budget is **does not suffice**:
	- "\{**money needed**\} **dollars needed.**"

The sum must be formatted to the second digit after the decimal point.

## Example
| **Input** | **Output** |
| --- | --- |
| 800.50 | The Smiths will be left with 24.49 dollars after the vacation. |
| 8 | |
| 100 | |
| 2 | |

### Comments
- 8 nights > 7, therefore there is a 5% discount on the price per night, which is 100$
- 5% of 100 is 5 -> 100 - 5 = 95$ per night after the discount, 8 * 95$ = 760$
- 2% of the budget is spent on additional costs. 2% from 800.50 is 16.01$
- 760 + 16.01 = 776.01 <= 800.50, therefore they have enough money and after the trip they return keeping 800.50 - 776.01 = 24.49$
 
[/task-description]
[code-io /]
[tests]
[test open]
[input]
800.50
8
100
2
[/input]
[output]
The Smiths will be left with 24.49 dollars after the vacation.
[/output]
[/test]
[test]
[input]
504.20
10
54.20
20
[/input]
[output]
111.54 dollars needed.
[/output]
[/test]
[test]
[input]
845
9
50
18
[/input]
[output]
The Smiths will be left with 265.40 dollars after the vacation.
[/output]
[/test]
[test]
[input]
100
4
25
1
[/input]
[output]
1.00 dollars needed.
[/output]
[/test]
[test]
[input]
566
9
10
30
[/input]
[output]
The Smiths will be left with 310.70 dollars after the vacation.
[/output]
[/test]
[test]
[input]
100
15
40
5
[/input]
[output]
475.00 dollars needed.
[/output]
[/test]
[test]
[input]
800
10
10
60
[/input]
[output]
The Smiths will be left with 225.00 dollars after the vacation.
[/output]
[/test]
[test]
[input]
500
20
40
26
[/input]
[output]
390.00 dollars needed.
[/output]
[/test]
[test]
[input]
100
2
20
10
[/input]
[output]
The Smiths will be left with 50.00 dollars after the vacation.
[/output]
[/test]
[test]
[input]
95
10
10
0
[/input]
[output]
The Smiths will be left with 0.00 dollars after the vacation.
[/output]
[/test]
[test]
[input]
50
5
9
10
[/input]
[output]
The Smiths will be left with 0.00 dollars after the vacation.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
