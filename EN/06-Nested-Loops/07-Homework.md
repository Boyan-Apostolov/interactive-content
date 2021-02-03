# Homework

[slide hideTitle]
# Problem: Building

[vimeo-video]
[stream language="EN" videoId="488090883/a7c270a8f6" default /]
[stream language="RO" videoId="488090883/a7c270a8f6"  /]
[/video-vimeo]

# Solution

[vimeo-video]
[stream language="EN" videoId="488090919/8b4c1a9e61" default /]
[stream language="RO" videoId="488090919/8b4c1a9e61"  /]
[/video-vimeo]

[code-task title="Building" taskId="pb-js-nested-loops-Building" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function building(floors, rooms) {
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
function adapter(input, code) {
  let a = Number(input[0]);
  let b = Number(input[1]);
  return code(a, b);
}
```
[/code-adapter]
[task-description]
# Description
Write a program, which:

Prints information about a building: 
* The building can hold: **apartments (odd numbered floors)**, **offices (even numbered floors)** and **(on the last floor) Large Apartments** 
* Apartments are indexed with: `A{buildingNum}{apartmentNum}`
* Offices: `O{floorNum}{officeNum}`
* Large apartments: `L{buildingNum}{apartmentNum}`
* The numbers always start from 0

# Example
| **Input** | **Output** |
| --- | --- |
|6, 4| L60 L61 L62 L63|
|| A50 A51 A52 A53|
||O40 O41 O42 O43 |
||A30 A31 A32 A33 |
||O20 O21 O22 O23 |
|| A10 A11 A12 A13|

[/task-description]
[tests]
[test]
[input]
1
7
[/input]
[output]
L10 L11 L12 L13 L14 L15 L16
[/output]
[/test]
[test]
[input]
0
0
[/input]
[output]

[/output]
[/test]
[test]
[input]
2
5
[/input]
[output]
L20 L21 L22 L23 L24
A10 A11 A12 A13 A14
[/output]
[/test]
[test]
[input]
10
10
[/input]
[output]
L100 L101 L102 L103 L104 L105 L106 L107 L108 L109
A90 A91 A92 A93 A94 A95 A96 A97 A98 A99
O80 O81 O82 O83 O84 O85 O86 O87 O88 O89
A70 A71 A72 A73 A74 A75 A76 A77 A78 A79
O60 O61 O62 O63 O64 O65 O66 O67 O68 O69
A50 A51 A52 A53 A54 A55 A56 A57 A58 A59
O40 O41 O42 O43 O44 O45 O46 O47 O48 O49
A30 A31 A32 A33 A34 A35 A36 A37 A38 A39
O20 O21 O22 O23 O24 O25 O26 O27 O28 O29
A10 A11 A12 A13 A14 A15 A16 A17 A18 A19
[/output]
[/test]
[test]
[input]
5
5
[/input]
[output]
L50 L51 L52 L53 L54
O40 O41 O42 O43 O44
A30 A31 A32 A33 A34
O20 O21 O22 O23 O24
A10 A11 A12 A13 A14
[/output]
[/test]
[test]
[input]
1
1
[/input]
[output]
L10
[/output]
[/test]
[test]
[input]
6
7
[/input]
[output]
L60 L61 L62 L63 L64 L65 L66
A50 A51 A52 A53 A54 A55 A56
O40 O41 O42 O43 O44 O45 O46
A30 A31 A32 A33 A34 A35 A36
O20 O21 O22 O23 O24 O25 O26
A10 A11 A12 A13 A14 A15 A16
[/output]
[/test]
[test]
[input]
8
2
[/input]
[output]
L80 L81
A70 A71
O60 O61
A50 A51
O40 O41
A30 A31
O20 O21
A10 A11
[/output]
[/test]
[test]
[input]
9
0
[/input]
[output]

[/output]
[/test]
[test]
[input]
7
3
[/input]
[output]
L70 L71 L72
O60 O61 O62
A50 A51 A52
O40 O41 O42
A30 A31 A32
O20 O21 O22
A10 A11 A12
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Passwords

[vimeo-video]
[stream language="EN" videoId="488091064/8c0b8dc12c" default /]
[stream language="RO" videoId="488091064/8c0b8dc12c"  /]
[/video-vimeo]

# Solution

[vimeo-video]
[stream language="EN" videoId="488091095/c49f5f03e5" default /]
[stream language="RO" videoId="488091095/c49f5f03e5"  /]
[/video-vimeo]

[code-task title="Passwords" taskId="pb-js-nested-loops-Passwords" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function passwords(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program, which:
* Reads an integer - **n**
* Generates custom passwords, which meet the following conditions:
* The **first** part is an **even** number and should not be greater than **n**
* The **second** part is an **odd** number and should not be greater than **n**
* The **last part** is the **product** of the first two

# Example
| **Input** | **Output** |
| --- | --- |
|6| 212 236 2510 414 4312 4520 616 6318 6530 |

[/task-description]
[tests]
[test]
[input]
8
[/input]
[output]
212 236 2510 2714 414 4312 4520 4728 616 6318 6530 6742 818 8324 8540 8756
[/output]
[/test]
[test]
[input]
9
[/input]
[output]
212 236 2510 2714 2918 414 4312 4520 4728 4936 616 6318 6530 6742 6954 818 8324 8540 8756 8972
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
212 236 2510 2714 2918 414 4312 4520 4728 4936 616 6318 6530 6742 6954 818 8324 8540 8756 8972 10110 10330 10550 10770 10990
[/output]
[/test]
[test]
[input]
3
[/input]
[output]
212 236
[/output]
[/test]
[test]
[input]
2
[/input]
[output]
212
[/output]
[/test]
[test]
[input]
9
[/input]
[output]
212 236 2510 2714 2918 414 4312 4520 4728 4936 616 6318 6530 6742 6954 818 8324 8540 8756 8972
[/output]
[/test]
[test]
[input]
15
[/input]
[output]
212 236 2510 2714 2918 21122 21326 21530 414 4312 4520 4728 4936 41144 41352 41560 616 6318 6530 6742 6954 61166 61378 61590 818 8324 8540 8756 8972 81188 813104 815120 10110 10330 10550 10770 10990 1011110 1013130 1015150 12112 12336 12560 12784 129108 1211132 1213156 1215180 14114 14342 14570 14798 149126 1411154 1413182 1415210
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Magic Number
[code-task title="Magic Number" taskId="pb-js-nested-loops-magic-number" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function magicNumber(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program, which:
* Reads a **number - n**, from the console
* Finds all **3-digit numbers** for which the product of the multiplication of their separate digits is equal to `n` 

# Example
| **Input** | **Output** |
| --- | --- |
|3| 113 |
|| 131 |
|| 311 |
 
[/task-description]
[tests]
[test]
[input]
4
[/input]
[output]
114
122
141
212
221
411
[/output]
[/test]
[test]
[input]
5
[/input]
[output]
115
151
511
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
118
124
142
181
214
222
241
412
421
811
[/output]
[/test]
[test]
[input]
9
[/input]
[output]
119
133
191
313
331
911
[/output]
[/test]
[test]
[input]
12
[/input]
[output]
126
134
143
162
216
223
232
261
314
322
341
413
431
612
621
[/output]
[/test]
[test]
[input]
4
[/input]
[output]
114
122
141
212
221
411
[/output]
[/test]
[test]
[input]
14
[/input]
[output]
127
172
217
271
712
721
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Travelling
[code-task title="Travelling" taskId="pb-js-nested-loops-travelling" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function travelling(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program, which:

* Reads a **destination** and a **required budget** to visit it 
* Continues taking numbers - amounts of money, until it is **enough** to take the trip 
* If we receive the command `End` the program ends

# Example
| **Input** | **Output** |
| --- | --- |
|`['Philippines', '1000', '550', '450', 'End']` | Going to Philippines! |

[/task-description]
[tests]
[test open]
[input]
Greece
1000
200
200
300
100
150
240
Spain
1200
300
500
193
423
End
[/input]
[output]
Going to Greece!
Going to Spain!
[/output]
[/test]
[test open]
[input]
France
2000
300
300
200
400
190
258
360
Portugal
1450
400
400
200
300
300
Egypt
1900
1000
280
300
500
End
[/input]
[output]
Going to France!
Going to Portugal!
Going to Egypt!
[/output]
[/test]
[test]
[input]
Bulgaria
500
200
100
300
Austria
700
200
200
200
200
End
[/input]
[output]
Going to Bulgaria!
Going to Austria!
[/output]
[/test]
[test]
[input]
Maldives
2500
1000
340
50
50
50
50
700
700
End
[/input]
[output]
Going to Maldives!
[/output]
[/test]
[test]
[input]
Africa
3000
1000
5000
America
2000
2500
China
4000
2000
1800
1800
End
[/input]
[output]
Going to Africa!
Going to America!
Going to China!
[/output]
[/test]
[test]
[input]
Estonia
1000
300
200
200
300
Peru
3000
2000
1000
Uganda
1000
1000
UAE
5000
3000
4000
Germany
2000
2000
Portugal
2050
3000
Portugal
2050
3000
Portugal
2050
3000
Portugal
2050
3000
Portugal
2050
3000
End
[/input]
[output]
Going to Estonia!
Going to Peru!
Going to Uganda!
Going to UAE!
Going to Germany!
Going to Portugal!
Going to Portugal!
Going to Portugal!
Going to Portugal!
Going to Portugal!
[/output]
[/test]
[test]
[input]
End
[/input]
[output]

[/output]
[/test]
[test]
[input]
France
3000
50
50
50
50
50
50
50
50
50
50
50
250
100
106
280
400
400
50
400
600
End
[/input]
[output]
Going to France!
[/output]
[/test]
[test]
[input]
Russia
15000
4500
300
300
3000
2000
4500
5000
Japan
1500.600
67.60
26.4052345
250.78
450.78945
578.76
98.60
260.84
End
[/input]
[output]
Going to Russia!
Going to Japan!
[/output]
[/test]
[test]
[input]
South Africa
2000
1000
1000
Egypt
300
150
100
20
20
20
End
[/input]
[output]
Going to South Africa!
Going to Egypt!
[/output]
[/test]
[test]
[input]
Zambia
3700.250
450.300
450.20414
600.43
640.23
824.50
1200.46
End
[/input]
[output]
Going to Zambia!
[/output]
[/test]
[test]
[input]
Albania
350.23414
45.24
23.124
123.144
145.23556
45.2345
End
[/input]
[output]
Going to Albania!
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Prime Numbers
[code-task title="Prime Numbers" taskId="pb-js-nested-prime-numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function primeNumbers(firstNumber, secondNumber) {
    // Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => {
  return code (Number(input[0]), Number(input[1]))
}
```
[/code-adapter]
[task-description]
# Description
Write a program, which:

* Reads **two numbers** from the console
* Prints the **prime** number in that **range**

# Example
| **Input** | **Output** |
| --- | --- |
|1, 50| 1 2 3 5 7 11 13 17 19 23 29 31 37 41 43 47 |

[/task-description]
[tests]
[test]
[input]
1
4
[/input]
[output]
1 2 3
[/output]
[/test]
[test]
[input]
600
900
[/input]
[output]
601 607 613 617 619 631 641 643 647 653 659 661 673 677 683 691 701 709 719 727 733 739 743 751 757 761 769 773 787 797 809 811 821 823 827 829 839 853 857 859 863 877 881 883 887
[/output]
[/test]
[test]
[input]
55
70
[/input]
[output]
59 61 67
[/output]
[/test]
[test]
[input]
11
13
[/input]
[output]
11 13
[/output]
[/test]
[test]
[input]
88
100
[/input]
[output]
89 97
[/output]
[/test]
[test]
[input]
23
27
[/input]
[output]
23
[/output]
[/test]
[test]
[input]
1
9
[/input]
[output]
1 2 3 5 7
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Unique PIN Codes
[code-task title="Unique PIN Codes" taskId="pb-js-nested-loops-unique-pin-codes" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function uniquePinCodes(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program, which:

* Reads **3 digits** - n1, n2 and n3
* Generates **unique 3 digit PIN Codes**, which meet the following **conditions**:
* The **first** digit should not be greater than n1
* The **second** digit should not be greater than n2
* The **third** digit should not be greater than n3
* The **first** and the **third** digit must be even
* The second digit must be a **prime number** in the range \[2…7\]

# Example
| **Input** | **Output** |
| --- | --- |
|3| 222 |
|5| 224 |
|5| 232 |
|| 234 |
|| 252 |
|| 254 |

[/task-description]
[tests]
[test]
[input]
8
2
8
[/input]
[output]
222
224
226
228
422
424
426
428
622
624
626
628
822
824
826
828
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Letter Combinations
[code-task title="Letter Combinations" taskId="pb-js-nested-loops-letter-combinations" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function letterCombinations(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program, which:

* Prints **letter combinations** and the **number** of generated combinations

* You will receive the **range of letters** on the first and second line

* On the third line, you will receive a **letter**, which you must **ignore** - do not print combinations with it

# Example
| **Input** | **Output** |
| --- | --- |
|a| aaa aac aca acc caa cac cca ccc 8 |
|c|  |
|b|  |


[/task-description]
[tests]
[test]
[input]
a
c
b
[/input]
[output]
aaa aac aca acc caa cac cca ccc 8
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Happy Numbers
[code-task title="Happy Numbers" taskId="pb-js-nested-loops-Happy-numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function happyNumbers(input) {
    // Write your code here
}
```
[/code-editor]
[task-description]
# Description
Write a program, which:

Generates all **4 digit numbers** with digits less than n and prints them out if: 

* When you split the number in two pairs and add the first digit to the second one of each pair- the result equals `n` 

* When you add the first two, the result is divisible by n without a remainde

# Example
| **Input** | **Output** |
| --- | --- |
|3| 1212 1221 2112 2121 |
||  |
||  |

[/task-description]
[tests]
[test]
[input]
3
[/input]
[output]
1212 1221 2112 2121
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

