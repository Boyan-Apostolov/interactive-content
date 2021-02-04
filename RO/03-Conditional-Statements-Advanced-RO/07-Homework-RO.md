# Homework
[slide hideTitle]
# Problem: Fruit or Vegetable
[code-task title="Fruit or Vegetable" taskId="pb-js-Conditions-Advanced-Fruit-or-Vegetable" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function fruitOrVegetable(input) {
    // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Descriere
Scrieți un program pentru a verifica fructele sau legumele:

* Citiți o singură linie de intrare: un articol din legume
* Fructe: banana, apple, kiwi, cherry, lemon, grapes
* Legume: cucumber, pepper, carrot, onion
* Imprimați: `vegetable`, `fruit` sau  `unknown`

# Exemplu
  | **Intrare** | **Ieșire** |
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
    // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Descriere
Scrieți un program pentru a imprima ziua săptămânii ca un cuvânt:

*Citire și număr întreg **n**: **ziua săptămânii** în intervalul `[1..7]`
*Tipăriți *numele zilei* (ca un cuvânt, în engleză)
*Imprimați `Error`, dacă numărul nu se află în intervalul dat


# Exemplu
  | **Intrare** | **Ieșire** |
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
    // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# # Descriere
Scrieți un program pentru a verifica o literă dacă este o vocală sau o consoană:

*Citiți o **literă** din alfabetul englez
*Imprimați  `Vowel` sau `Consonant`


# Exemplu
  | **Intrare** | **Ieșire** |
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
# Problem: Product of 3 Numbers
[vimeo-video]
[stream language="EN" videoId="486874673/6eb04e1bbf" default /]
[stream language="RO" videoId="486874673/6eb04e1bbf"  /]
[/video-vimeo]

[code-task title="Product of 3 Numbers" taskId="pb-js-Conditions-Advanced-Product-of-3-numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function productOfThreeNumbers(firstNumber, secondNumber, thirdNumber) {
    // Scrieți codul dvs. aici
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
# Descriere
Calculați semnul produsului de 3 numere:

* Citiți **3 numere în virgulă mobilă** 
* Imprimați semnul** produsului celor 3 numere introduse: `positive`, `negative` sau `zero`

Încercați să faceți acest lucru **fără a înmulți** cele 3 numere

# Exemplu
  | **Intrare** | **Ieșire** |
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
# Problem: Sorted Numbers
[vimeo-video]
[stream language="EN" videoId="486875734/a16fef14e3" default /]
[stream language="RO" videoId="486875734/a16fef14e3"  /]
[/video-vimeo]

[code-task title="Sorted Numbers" taskId="pb-js-Conditions-Advanced-Sorted-Numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function sortedNumbers(firstNumber, secondNumber, thirdNumber) {
    // Scrieți codul dvs. aici
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
# Descriere
Scrieți un program, care verifică **3 numere sortate**:

* Citiți 3 numere reale
* Tipăriți `Ascending` dacă numerele sunt în ordine crescătoare
* Tipăriți `Descending` dacă numerele sunt în ordine descrescătoare
* Imprimați `Not sorted` în orice alt caz


# Exemplu
  | **Intrare** | **Ieșire** |
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
    // Scrieți codul dvs. aici
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
# Descriere
Scrieți un program, care calculează cheltuielile de vacanță:

* Citiți sezonul, tipul de cazare și  numărul de zile
* Imprimați **cheltuielile** totale pe baza tabelului de prețuri de mai jos, formatat la **a doua cifră** după punctul zecimal


 | Season   | Hotel | Camping   | Discount|
| :---:       |    :----:   |   :---:     |   :---: |
|Spring|30|10|20\%|
|Summer|50|30|0\%|
|Autumn|20|15|30\%|
|Winter|40|10|10\%|

# Exemplu
  | **Intrare** | **Ieșire** |
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
    // Scrieți codul dvs. aici
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
Calculați **prețul** pentru toate biletele pentru un film cinematografic:

*Citiți **tipul filmului**, **rândurile** și **locurile pe rând** din cinematograf
*Tipăriți **prețul total** pentru toate locurile **formatate** la a doua cifră după punctul zecimal


  | **Type** | **Price** |
| --- | --- |
|Premiere|12.00|
|Normal|7.50|
|Discount|5.00|

# Exemplu
  | **Intrare** | **Ieșire** |
| --- | --- |
|Normal| 810.00 |
|12|  |
|9|  |

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
    // Scrieți codul dvs. aici
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
Scrieți un program pentru a aplica un operator pentru două numere date:

* Citiți doi numere întregi și operatorul matematic de pe consolă. 
* Operatorul aritmetic ar putea fi: `+`, `-`, `/`, `%` și `*`
* IRezultatul trebuie să fie în următorul **format**: `{N1} {operator} {N2} = {result}`

# Exemplu
  | **Intrare** | **Ieșire** |
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
    // Scrieți codul dvs. aici
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
# Descriere
Scrieți un program pentru a simula o retragere de numerar de la bancomat

* Citiți: **balance**, **withdraw** și **limit**
* Imprimați `The withdraw was successful.` Dacă soldul este suficient
* Imprimați `The daily limit was exceeded.` Dacă limita este depășită
* Imprimați `Insufficient availability.` dacă soldul nu este sufficient

# Exemplu
  | **Intrare** | **Ieșire** |
| --- | --- |
|420, 20, 25| The withdraw was successful. |


  | **Intrare** | **Ieșire** |
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
    // Scrieți codul dvs. aici
}
```
[/code-editor]
[code-adapter]
```
(input, code) => code(...input);
```
[/code-adapter]
[task-description]
# Descriere

Scrieți un program pentru a găsi cel mai mare dintre 5 numere

* Citiți **5 numere întregi**

* Imprimați cel mai mare**număr.


# Exemplu
  | **Intrare** | **Ieșire** |
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
