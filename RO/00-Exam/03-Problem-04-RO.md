﻿# Problem: Club
[slide hideTitle]
# Club
[code-task title="Club" taskId="pb-java-exam-Club" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

## Descriere

Vremea se încălzește, iar cluburile lansează oferte promițătoare.

Scrieți un program care să calculeze profitul unui disco club  și dacă este atins profitul dorit, ținând cont de următoarele:

Prețul unui cocktail este lungimea numelui său.

Dacă prețul unei comenzi este un număr impar, există o reducere de 25% de la prețul comenzii.

# Intrare
Veți primi:
- Pe prima linie - profitul dorit al clubului - număr real în intervalul [1.00 ... 15000.00]

O serie de două rânduri până la comanda **"Party!"** sau până la atingerea profitului dorit:
- Numele cocktailului - șir
- Numărul de cocktailuri pentru comandă - număr întreg în intervalul [1 ... 50]

## Ieșire
Mai întâi, imprimați o linie pe consolă:

- Dacă primiți comanda **"Party!"**:
	- "**We need** \{**money needed**\} **dollars more.**"
- Dacă este atins profitul dorit:
	- "**Target acquired.**"

Apoi imprimați:
- "**Club income -** \{**club's profit**\} **dollars.**"

Banii trebuie formatați la a doua cifră după punctul zecimal.


## Exemplu
|**Intrare**|**Ieșire** |
| --- | --- |
| 500 | We need 416.00 dollars more. |
| Bellini | Club income - 84.00 dollars. |
| 6 |  |
| Bamboo |  |
| 7 |  |
| Party! |  |

[hints]
[hint]
Note that the individual price of each cocktail is the length of its name. If the price for an order is an odd number, apply the discount. 
Calculate the price for each order and add them to the total.
[/hint]
[hint]
If you reach the desired profit before receiving the "Party!" command, print the correct output.
If you receive the command "Party!" and you haven't reached the desired profit, determine how much money is needed and print the correct output.
[/hint]
[/hints]

[/task-description]
[code-io /]
[tests]
[test open]
[input]
500
Bellini
6
Bamboo
7
Party!
[/input]
[output]
We need 416.00 dollars more.
Club income - 84.00 dollars.
[/output]
[/test]
[test open]
[input]
100
Sidecar
7
Mojito
5
White Russian
10
[/input]
[output]
Target acquired.
Club income - 196.75 dollars.
[/output]
[/test]
[test]
[input]
50
Rom
3
Rakia
5
Vesper
9
[/input]
[output]
Target acquired.
Club income - 79.50 dollars.
[/output]
[/test]
[test]
[input]
100
Rakia
5
Whiskey
9
Irish Coffee
5
[/input]
[output]
Target acquired.
Club income - 126.00 dollars.
[/output]
[/test]
[test]
[input]
1000
Irish Coffe
50
Party!
[/input]
[output]
We need 450.00 dollars more.
Club income - 550.00 dollars.
[/output]
[/test]
[test]
[input]
789
Painkiller
20
Party!
[/input]
[output]
We need 589.00 dollars more.
Club income - 200.00 dollars.
[/output]
[/test]
[test]
[input]
100
Bees Knees
23
[/input]
[output]
Target acquired.
Club income - 230.00 dollars.
[/output]
[/test]
[test]
[input]
200
French 75
9
French 75
9
Gimlet
3
Mai Tai
6
Gin Fizz
6
[/input]
[output]
Target acquired.
Club income - 229.50 dollars.
[/output]
[/test]
[test]
[input]
50
Rakia
3
Vodka
16
[/input]
[output]
Target acquired.
Club income - 91.25 dollars.
[/output]
[/test]
[test]
[input]
999
Rum old fashioned
10
Bloody Mary
9
Party!
[/input]
[output]
We need 754.75 dollars more.
Club income - 244.25 dollars.
[/output]
[/test]
[test]
[input]
100
White Lady
9
R
9
Party!
[/input]
[output]
We need 3.25 dollars more.
Club income - 96.75 dollars.
[/output]
[/test]
[test]
[input]
100
Caipirinha
10
[/input]
[output]
Target acquired.
Club income - 100.00 dollars.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
