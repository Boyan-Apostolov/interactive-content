// sectionId: "Javascript-Programming-Basics-Conditional-Statements-Advanced-Homework

# Homework
[slide hideTitle]
# Problem: Fruit or Vegetable
[code-task title="Fruit or Vegetable" taskId="pb-js-Conditions-Advanced-Fruit-or-Vegetable" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function fruitOrVegetable(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program to check for fruit or vegetable:

* Read a single input line: an item from the greengrocery
* Fruits: banana, apple, kiwi, cherry, lemon, grapes
* Vegetables: cucumber, pepper, carrot, onion
* Print: `vegetable`, `fruit` or `unknown`

# Example
| **Input** | **Output** |
| --- | --- |
|lemon| fruit |
|carrot| vegetable |

[/task-description]
[tests]
[test]
[input]
lemon
[/input]
[output]
fruit
[/output]
[/test]
[test]
[input]
carrot
[/input]
[output]
vegetable
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Day of Week
[code-task title="Day of Week" taskId="pb-js-Conditions-Advanced-Day-of-Week" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function dayOfWeek(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program to print the day of the week as word: 

* Read and integer **n**: the **day of the week** in range `[1..7]`
* Print the name of the day (as word, in English) 
* Print `Error` if the number is not in the given range

# Example
| **Input** | **Output** |
| --- | --- |
|1| Monday |
|8| Error |

[/task-description]
[tests]
[test]
[input]
1
[/input]
[output]
Monday
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
Error
[/output]
[/test]
[test]
[input]
7
[/input]
[output]
Sunday
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Vowel or Consonant
[code-task title="Vowel or Consonant" taskId="pb-js-Conditions-Advanced-Vowel-or-Consonant" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function vowelOrConsonant(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program to check a letter for vowel or consonant:

* Read a **letter** from the English alphabet
* Print either `Vowel` or `Consonant`

# Example
  | **Input** | **Output** |
| --- | --- |
|a| Vowel |
|B| Consonant |

[/task-description]
[tests]
[test]
[input]
a
[/input]
[output]
Vowel
[/output]
[/test]
[test]
[input]
E
[/input]
[output]
Vowel
[/output]
[/test]
[test]
[input]
b
[/input]
[output]
Consonant
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem with Solution: Product of 3 Numbers
[video src="https://videos.softuni.org/hls/javascript-basics/03.Conditions-Advanced/problem1-product-of-3-numbers-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Product of 3 Numbers" taskId="pb-js-Conditions-Advanced-Product-of-3-numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function productOfThreeNumbers(firstNumber, secondNumber, thirdNumber) {
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => {
  return code (Number(input[0]), Number(input[1]), Number(input[2]));
}
```
[/code-adapter]
[task-description]
# Description
Calculate the sign of the product of 3 numbers:

* Read **3 floating-point** numbers
* Print the **sign** of the product of the entered 3 numbers: `positive`, `negative` or `zero`

Try to do this **without multiplying** the 3 numbers
# Example
  | **Input** | **Output** |
| --- | --- |
|2, 3, -1| negative |


[/task-description]
[tests]
[test open]
[input]
-2
3
1
[/input]
[output]
negative
[/output]
[/test]
[test]
[input]
-3
-4
5
[/input]
[output]
positive
[/output]
[/test]
[test]
[input]
2
-9
5
[/input]
[output]
negative
[/output]
[/test]
[test]
[input]
4
0
-10
[/input]
[output]
zero
[/output]
[/test]
[test]
[input]
5
2
2
[/input]
[output]
positive
[/output]
[/test]
[test]
[input]
-5
2
-2
[/input]
[output]
positive
[/output]
[/test]
[test]
[input]
1
2
0
[/input]
[output]
zero
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem with Solution: Sorted Numbers
[video src="https://videos.softuni.org/hls/javascript-basics/03.Conditions-Advanced/problem2-sorted-numbers-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Sorted Numbers" taskId="pb-js-Conditions-Advanced-Sorted-Numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function sortedNumbers(firstNumber, secondNumber, thirdNumber) {
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => {
  return code (Number(input[0]), Number(input[1]), Number(input[2]));
}
```
[/code-adapter]
[task-description]
# Description
Write a program, which checks for **sorted 3 numbers**:

* Read 3 real numbers
* Print `Ascending` if the numbers are in ascending order
* Print `Descending` if the numbers are in descending order
* Print `Not sorted` in any other case

# Example
| **Input** | **Output** |
| --- | --- |
|1, 2, 3| Ascending |
|3, 5, 2]| Not sorted |

[/task-description]
[tests]
[test open]
[input]
1
2
3
[/input]
[output]
Ascending
[/output]
[/test]
[test]
[input]
3
1
2
[/input]
[output]
Not sorted
[/output]
[/test]
[test]
[input]
3
2
1
[/input]
[output]
Descending
[/output]
[/test]
[test]
[input]
4
3
2
[/input]
[output]
Descending
[/output]
[/test]
[test]
[input]
2
3
4
[/input]
[output]
Ascending
[/output]
[/test]
[test]
[input]
4
5
3
[/input]
[output]
Not sorted
[/output]
[/test]
[test]
[input]
10
9
8
[/input]
[output]
Descending
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Vacation Expenses
[code-task title="Vacation Expenses" taskId="pb-js-Conditions-Advanced-Vacation-Expenses" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function vacationExpenses(season, building, days){
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => {
  return code (input[0], input[1], Number(input[2]));
}
```
[/code-adapter]
[task-description]
# Description
Write a program, which calculates vacation expenses:

* Read a season, an accommodation type and a count of the days 
* Print the total **expenses**, based on the price table bellow, formatted to the **2nd digit** after the decimal point

 | Season   | Hotel | Camping   | Discount|
| :---:       |    :----:   |   :---:     |   :---: |
|Spring|30|10|20\%|
|Summer|50|30|0\%|
|Autumn|20|15|30\%|
|Winter|40|10|10\%|

# Example
| **Input** | **Output** |
| --- | --- |
|'Winter', 'Hotel', 5| 180.00 |

[/task-description]
[tests]
[test open]
[input]
Winter
Hotel
5
[/input]
[output]
180.00
[/output]
[/test]
[test]
[input]
Winter
Camping
10
[/input]
[output]
90.00
[/output]
[/test]
[test]
[input]
Autumn
Camping
6
[/input]
[output]
63.00
[/output]
[/test]
[test]
[input]
Summer
Hotel
7
[/input]
[output]
350.00
[/output]
[/test]
[test]
[input]
Spring
Camping
8
[/input]
[output]
64.00
[/output]
[/test]
[test]
[input]
Summer
Hotel
9
[/input]
[output]
450.00
[/output]
[/test]
[test]
[input]
Autumn
Camping
10
[/input]
[output]
105.00
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Cinema
[code-task title="Cinema" taskId="pb-js-Conditions-Advanced-Cinema" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function cinema(typeOfMovie, rows, seatsPerRow) {
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => {
  return code (input[0], Number(input[1]), Number(input[2]));
}
```
[/code-adapter]
[task-description]
# Description
Calculate the **price** for all the tickets for a cinema movie:

* Reads the **type of the movie**, the **rows** and the **seats per row** in the cinema
* Prints the **total price** for all seats **formatted** to the 2nd digit after the decimal point

  | **Type** | **Price** |
| --- | --- |
|Premiere|12.00|
|Normal|7.50|
|Discount|5.00|

# Example
  | **Input** | **Output** |
| --- | --- |
|'Normal', 12, 9| 810.00 |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
Premiere
10
12
[/input]
[output]
1440.00
[/output]
[/test]
[test open]
[input]
Normal
21
13
[/input]
[output]
2047.50
[/output]
[/test]
[test open]
[input]
Discount
12
30
[/input]
[output]
1800.00 leva
[/output]
[/test]
[test]
[input]
Normal
88
44
[/input]
[output]
29040.00
[/output]
[/test]
[test]
[input]
Discount
43
15
[/input]
[output]
3225.00
[/output]
[/test]
[test]
[input]
Premiere
42
62
[/input]
[output]
31248.00
[/output]
[/test]
[test]
[input]
Discount
30
36
[/input]
[output]
5400.00
[/output]
[/test]
[test]
[input]
Premiere
94
17
[/input]
[output]
19176.00
[/output]
[/test]
[test]
[input]
Discount
34
7
[/input]
[output]
1190.00
[/output]
[/test]
[test]
[input]
Discount
93
21
[/input]
[output]
9765.00
[/output]
[/test]
[test]
[input]
Discount
54
46
[/input]
[output]
12420.00
[/output]
[/test]
[test]
[input]
Discount
34
93
[/input]
[output]
15810.00
[/output]
[/test]
[test]
[input]
Premiere
68
50
[/input]
[output]
40800.00
[/output]
[/test]
[test]
[input]
Normal
73
61
[/input]
[output]
33397.50
[/output]
[/test]
[test]
[input]
Normal
63
64
[/input]
[output]
30240.00
[/output]
[/test]
[test]
[input]
Normal
84
98
[/input]
[output]
61740.00
[/output]
[/test]
[test]
[input]
Normal
59
57
[/input]
[output]
25222.50
[/output]
[/test]
[test]
[input]
Premiere
32
54
[/input]
[output]
20736.00
[/output]
[/test]
[test]
[input]
Premiere
52
35
[/input]
[output]
21840.00
[/output]
[/test]
[test]
[input]
Normal
36
75
[/input]
[output]
20250.00
[/output]
[/test]
[test]
[input]
Normal
65
68
[/input]
[output]
33150.00
[/output]
[/test]
[test]
[input]
Premiere
59
35
[/input]
[output]
24780.00
[/output]
[/test]
[test]
[input]
Discount
78
9
[/input]
[output]
3510.00
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Operations with Numbers
[code-task title="Operations with Numbers" taskId="pb-js-Conditions-Advanced-Operation-With-Numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function operationswithNumbers(firstNumber, secondNumber, operation) {
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => {
  return code (Number(input[0]), Number(input[1]), input[2]);
}
```
[/code-adapter]
[task-description]
# Description
Write a program to apply an operator for given two numbers:

* Read two integers and a math operator from the console. 
* The math operator could be: `+`, `-`, `/`, `%` și `*`
* The output should be in the following **format**: `{N1} {operator} {N2} = {result}`

# Example
  | **Input** | **Output** |
| --- | --- |
|12, 10, '\+'| 12 + 10 = 22 |

[/task-description]
[tests]
[test open]
[input]
10
12
\+
[/input]
[output]
10 + 12 = 22
[/output]
[/test]
[test]
[input]
12
10
\-
[/input]
[output]
12 \- 10 = 2
[/output]
[/test]
[test]
[input]
10
12
\*
[/input]
[output]
10 \* 12 = 120
[/output]
[/test]
[test]
[input]
6
2
\/
[/input]
[output]
6 \/ 2 = 3
[/output]
[/test]
[test]
[input]
5
2
\%
[/input]
[output]
5 \% 2 = 1
[/output]
[/test]
[test]
[input]
2
2
\-
[/input]
[output]
2 \- 2 = 0
[/output]
[/test]
[test]
[input]
2
2
\+
[/input]
[output]
2 \+ 2 = 4
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: ATM
[code-task title="ATM" taskId="pb-js-Conditions-Advanced-ATM" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function atm(balance, withdraw, limit) {
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => {
  return code (Number(input[0]), Number(input[1]), Number(input[2]));
}
```
[/code-adapter]
[task-description]
# Description
Write a program to simulate an ATM withdrawal:

* Read: **balance**, **withdraw** and **limit**
* Print `The withdraw was successful.` if the balance is enough
* Print `The daily limit was exceeded.` if the limit is exceeded
* Print `Insufficient availability.` if the balance is not enough

# Example
  | **Input** | **Output** |
| --- | --- |
|420, 20, 25| The withdraw was successful. |

  | **Input** | **Output** |
| --- | --- |
|10, 50, 20| The daily limit was exceeded. |
|| Insufficient availability. |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
420
20
25
[/input]
[output]
The withdraw was successful.
[/output]
[/test]
[test]
[input]
10
50
20
[/input]
[output]
The daily limit was exceeded.
Insufficient availability.
[/output]
[/test]
[test]
[input]
10
4565
345
[/input]
[output]
The daily limit was exceeded.
Insufficient availability.
[/output]
[/test]
[test]
[input]
342
2
3
[/input]
[output]
The withdraw was successful.
[/output]
[/test]
[test]
[input]
10
50
20
[/input]
[output]
The daily limit was exceeded.
Insufficient availability.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Biggest of Five Numbers
[code-task title="Biggest of Five Numbers" taskId="pb-js-Conditions-Advanced-Biggest-of-Five-Numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function biggestOfFiveNumbers(numOne, numTwo, numThree, numFour, numFive) {
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => code(...input);
```
[/code-adapter]
[task-description]
# Description
Write a program to find the biggest among 5 numbers
* Read **5 integers**
* Print the **largest** number. 

  | **Input** | **Output** |
| --- | --- |
|\-1, \-2, \-3, \-4, \-5 | \-1 |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
-1
-2
-3
-4
-5
[/input]
[output]
-1
[/output]
[/test]
[test]
[input]
5
-2
-3
9
-8
[/input]
[output]
9
[/output]
[/test]
[test]
[input]
-1
4
3
-4
1
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
4
2
5
43
1
[/input]
[output]
43
[/output]
[/test]
[test]
[input]
234234
2345
56756
67867
3453
[/input]
[output]
234234
[/output]
[/test]
[test]
[input]
3452
54756
6786
3453
4
[/input]
[output]
54756
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

