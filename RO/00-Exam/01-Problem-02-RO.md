﻿# Problem: Family Trip
[slide hideTitle]
# Family Trip
[code-task title="Family Trip" taskId="pb-java-exam-family-trip" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```java
import java.util.Scanner;

public class Program {
  public static void main(String[] args) {
    // Scrieți codul dvs. aici
  }
}
```
[/code-editor]
[task-description]
## Description

Familie Smith își planifică vacanța impreuna.

Sarcina dvs. este să scrieți un program care să calculeze dacă bugetul lor va fi suficient, știind câte nopți au planificat, care este prețul pe noapte și ce procent din buget a fost asigurat pentru costuri suplimentare.

Rețineți că, dacă numărul de nopți este mai mare de 7, prețul pe noapte se reduce cu 5%.

## Intrare 

Veți primi 4 linii de pe consolă:
- Bugetul care este disponibil - număr real în intervalul [1.00 ... 10000.00]
- Numărul de nopți - număr întreg în intervalul [0 ... 1000]
- Preț pe noapte - număr real în intervalul [1.00 ... 500.00]
- Procent de costuri suplimentare - număr întreg în intervalul [0 ... 100]

## Ieșire
Imprimarea pe consolă depinde de rezultatul:
- Dacă bugetul este suficient:
	-  "**The Smiths will be left with** \{**money left after the trip**\} **dollars after the vacation.**"
- Dacă bugetul NU este suficient:
	- "\{**money needed**\} **dollars needed.**"

Suma trebuie formatată la a doua cifră după punctul zecimal.

## Exemple
|**Intrare**|**Ieșire** |
| --- | --- |
| 800.50 | The Smiths will be left with 24.49 dollars after the vacation. |
| 8 | |
| 100 | |
| 2 | |

[hints]
[hint]
Determine if there will be a discount if the Smiths are staying more than 7 days.
If there's a discount, calculate how much is it and subtract it from the price per 1 night.
[/hint]
[hint]
Calculate the price for the all the nights and add the additional costs.
[/hint]
[hint]
Check if their budget is sufficient and print the correct output.
[/hint]
[/hints]

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
