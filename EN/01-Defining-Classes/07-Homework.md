# Homework

[slide hideTitle]
# Problem: Opinion Poll
[code-task title="Opinion Poll" taskId="ff6d1ff1-daef-4e93-b24d-14c878e40e96" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
Create Person class with two fields `String name` and `int age`, write a program that reads from the console **N** lines of personal information, and then prints all people whose **age** is **more than 30** years, **sorted in alphabetical order**.

**Note:** you can use `stream()` to filter the people.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | John - 48 |
| Peter 12 | Steven – 31 |
| Steven 31 |  |
| John 48 |  |

| **Input** | **Output** |
| --- | --- |
| 5 | Robert - 44 |
| Sofia 33 | Sofia - 33 |
| Thomas 88 | Thomas - 88 |
| Camilla 22 |  |
| Robert 44 |  |
| Owen 11 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
Peter 12
Steven 31
John 48
[/input]
[output]
John - 48
Steven - 31
[/output]
[/test]
[test open]
[input]
5
Sofia 33
Thomas 88
Camilla 22
Robert 44
Owen 11
[/input]
[output]
Robert - 44
Sofia - 33
Thomas - 88
[/output]
[/test]
[test]
[input]
11
A 40
B 43
C 54
D 31
E 99
M 32
N 123
O 100
P 321534
S 3213
Z 32131
[/input]
[output]
A - 40
B - 43
C - 54
D - 31
E - 99
M - 32
N - 123
O - 100
P - 321534
S - 3213
Z - 32131
[/output]
[/test]
[test]
[input]
11
Z 32
S 12
P 0
O 100
N 123
M 32
E 99
D 1
C 54
B 43
A 40
[/input]
[output]
A - 40
B - 43
C - 54
E - 99
M - 32
N - 123
O - 100
Z - 32
[/output]
[/test]
[test]
[input]
4
A 10
B 11
C 12
D 13
[/input]
[output]

[/output]
[/test]
[test]
[input]
10
A 31
B 76
E 645
Z 55
K 53
I 43
J 543
P 67
H 76
F 88
[/input]
[output]
A - 31
B - 76
E - 645
F - 88
H - 76
I - 43
J - 543
K - 53
P - 67
Z - 55
[/output]
[/test]
[test]
[input]
10
Andrew 31
Ben 76
Edward 645
Felix 11
Harley 76
Ivy 12
Joanna 0
Kylie 30
Poppy 67
Zoie 55
[/input]
[output]
Andrew - 31
Ben - 76
Edward - 645
Harley - 76
Poppy - 67
Zoie - 55
[/output]
[/test]
[test]
[input]
4
Ann 31
Anntoanette 39
An 33
Annie 31
[/input]
[output]
An - 33
Ann - 31
Annie - 31
Anntoanette - 39
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Problem: Company Roster
[code-task title="Company Roster" taskId="76597424-6663-4f2d-b5d1-cb23dff0383e" executionType="tests-execution" executionStrategy="java-zip-file-code" requiresInput]

```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
Define a class **Employee** that holds the following information: **name, salary, position, department, email** and **age**.

The **name, salary, position** and **department** are **mandatory** while the rest are **optional**.

Your task is to write a program which takes **N** lines of information about employees from the console and calculates the department with the highest average salary and prints for each employee in that department his **name, salary, email and age** - **sorted by salary in descending order**. 

If an employee **does not have** an **email** – in place of that field you should print **"n/a"** instead, if he does not have an **age** – print **"-1"** instead. 

The **salary** should be printed to **two decimal places** after the separator.

**Hint**: you can define a **Department** class that holds a list of employees.

## Examples
| **Input** | **Output** |
| --- | --- |
| 4 | Highest Average Salary: Development |
| Peter 2200.00 Dev Development peter@softuni.org 28 | John 4400.20 john@john.com -1 |
| Tom 3300.00 Manager Marketing 33 | Peter 2200.00 peter@softuni.org 28 |
| John 4400.20 ProjectLeader Development john@john.com |  |
| Philip 0.20 Freelancer Nowhere 18 |  |

| **Input** | **Output** |
| --- | --- |
| 6 | Highest Average Salary: Sales |
| Stan 4960.37 Temp Coding stan@yahoo.com | Jimmy 6100.13 n/a -1 |
| Jimmy 6100.13 Manager Sales | Alex 6090.99 alex@softuni.org 44 |
| Alex 6090.99 Manager Sales alex@softuni.org 44 |  |
| Victoria 0.02 Director BeerDrinking victoria@gmail.com 23 |  |
| Andrew 7000.00 Director Coding |  |
| Peyton 130.3333 Sailor SpinachGroup peyton@softuni.org |  |

[/task-description]
[code-upload allowedMemory="30" /]
[tests]
[test open]
[input]
4
Peter 2200.00 Dev Development peter@softuni.org 28
Tom 3300.00 Manager Marketing 33
John 4400.20 ProjectLeader Development john@john.com
Philip 0.20 Freelancer Nowhere 18
[/input]
[output]
Highest Average Salary: Development
John 4400.20 john@john.com -1
Peter 2200.00 peter@softuni.org 28
[/output]
[/test]
[test open]
[input]
6
Stan 4960.37 Temp Coding stan@yahoo.com
Jimmy 6100.13 Manager Sales
Alex 6090.99 Manager Sales alex@softuni.org 44
Victoria 0.02 Director BeerDrinking victoria@gmail.com 23
Andrew 7000.00 Director Coding
Peyton 130.3333 Sailor SpinachGroup peyton@softuni.org
[/input]
[output]
Highest Average Salary: Sales
Jimmy 6100.13 n/a -1
Alex 6090.99 alex@softuni.org 44
[/output]
[/test]
[test]
[input]
6
Michael 1300.01 Dev Development michael@softuni.org 28
Jeremy 1200.01 QA Testing jeremy@softuni.org 21
Trevor 1300.01 QA Testing trevor@gmail.com 23
Bethany 1300.02 QA Testing bethany@bethany.net 19
Stiven 1200.43 Dev Development stiven@yahoo.com 28
Sofia 1200.23 Dev Development sofia@softuni.org 28
[/input]
[output]
Highest Average Salary: Testing
Bethany 1300.02 bethany@bethany.net 19
Trevor 1300.01 trevor@gmail.com 23
Jeremy 1200.01 jeremy@softuni.org 21
[/output]
[/test]
[test]
[input]
6
Jacob 8400.20 ProjectLeader Development jacob@jacob.com
Bishop 1230.31 Manager Marketing bishop@gmail.com
Derek 3210.23 QA Testing derek@yahoo.com
Bobby 310.1 ProjectLeader Testing bobby@bobby.net
Phil 0.23 NoWhere StreetWork kodko@street.bg
Ed 11000.33 Dev Development ed@softuni.org
[/input]
[output]
Highest Average Salary: Development
Ed 11000.33 ed@softuni.org -1
Jacob 8400.20 jacob@jacob.com -1
[/output]
[/test]
[test]
[input]
7
Ben 8400.20 ProjectLeader Development 123
Clark 1230.31 Manager Marketing  123
Wendy 3210.23 QA Testing 22
Andy 3100.1 ProjectLeader Testing 14
Sarah 0.23 NoWhere StreetWork 13
Abbigail 1100.33 Dev Development 12
Robert 9999.98 QADev Testing 13
[/input]
[output]
Highest Average Salary: Testing
Robert 9999.98 n/a 13
Wendy 3210.23 n/a 22
Andy 3100.10 n/a 14
[/output]
[/test]
[test]
[input]
3
Ed 1223.32 Dev Development email@email.em
Edward 1993.32 Dev Development 22
Edison 1223931.32 Dev Development email@email.em 44
[/input]
[output]
Highest Average Salary: Development
Edison 1223931.32 email@email.em 44
Edward 1993.32 n/a 22
Ed 1223.32 email@email.em -1
[/output]
[/test]
[test]
[input]
18
Stan 49665.37 Temp Coding stan@yahoo.com
Yasmin 610.1653 Manager Sales
Teodor 60659.99 Manager Sales teodor@tdr.com 44
Benjamin 0.0652 Trainer Training benjamin@ben.org 23
Penny 700.0650 Director Coding
Popeye 13.335433 Sailor Shipping popeye@pop.eu
Murphy 496.3734 Temp Coding murphy@yahoo.com
Kurt 610.13 Manager Sales kurt@gmail.com
Teodor 609.993 Manager Sales teodor@gmail.com 44
Victor 0.032 Director Sales sales@uni.eu 23
Andrew 700.03305 Director Coding
Popeye2 13.333333 Sailor Shipping popeye@pop.eu
Simon 496.3437 Temp Coding simon@yahoo.com
Donald 620.133333 Manager Sales 12
Duck 609.99 Manager Sales duck@gmail.com 44
Daffy 0.02 Director Training daffy@uni.eu 23
Duckk 702.00 Director Coding
Christopher 13.3333 Sailor SpinachGroup robin@pop.eu
[/input]
[output]
Highest Average Salary: Sales
Teodor 60659.99 teodor@tdr.com 44
Donald 620.13 n/a 12
Yasmin 610.17 n/a -1
Kurt 610.13 kurt@gmail.com -1
Teodor 609.99 teodor@gmail.com 44
Duck 609.99 duck@gmail.com 44
Victor 0.03 sales@uni.eu 23
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Problem: Speed Racing
[code-task title="Speed Racing" taskId="51ee0d4e-daac-43b6-8bde-2477b2e01912" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
Your task is to implement a program that keeps track of cars and their fuel and supports methods for moving cars.

Define a class **Car** that keeps track of a car information **Model, fuel amount, fuel cost for 1 kilometer**, and **distance traveled**.

A Car Model is **unique** - there will never be 2 cars with the same model.

On the first line of the input you will receive a number **N** - the number of cars you need to track. 

On **each** of the next **N** lines you will receive information for a car in the following format: 

`<model> <fuelAmount> <fuelCostFor1km>`

All **cars start at 0 kilometers traveled**.

After the **N** lines until the command `End` is received, you will receive commands in the following format: 

`Drive <carModel> <amountOfKm>`

Implement a method in the **Car** class to calculate whether a car **can** move that distance or **not**. 

If it can, the car **fuel amount** should be **reduced** by the amount of used fuel and its **distance traveled** should be increased by the number of kilometers traveled, otherwise the car should not move (its fuel amount and distance traveled should stay the same) and you should print on the console 

`Insufficient fuel for the drive` 

After the `End` command is received, print each car in order of appearing in input and its current fuel amount and distance traveled in the format:

`<model> <fuelAmount> <distanceTraveled>`

Where the fuel amount should be rounded to the **second decimal place**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | AudiA4 17.60 18 |
| AudiA4 23 0.3 | BMW-M2 21.48 56 |
| BMW-M2 45 0.42 |  |
| Drive BMW-M2 56 |  |
| Drive AudiA4 5 |  |
| Drive AudiA4 13 |  |
| End |  |

| **Input** | **Output** |
| --- | --- |
| 3 | Insufficient fuel for the drive |
| AudiA4 18 0.34 | Insufficient fuel for the drive |
| BMW-M2 33 0.41 | AudiA4 1.00 50 |
| Ferrari-488Spider 50 0.47 | BMW-M2 33.00 0 |
| Drive Ferrari-488Spider 97 | Ferrari-488Spider 4.41 97 |
| Drive Ferrari-488Spider 35 |  |
| Drive AudiA4 85 |  |
| Drive AudiA4 50 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
AudiA4 23 0.3
BMW-M2 45 0.42
Drive BMW-M2 56
Drive AudiA4 5
Drive AudiA4 13
End
[/input]
[output]
AudiA4 17.60 18
BMW-M2 21.48 56
[/output]
[/test]
[test open]
[input]
3
AudiA4 18 0.34
BMW-M2 33 0.41
Ferrari-488Spider 50 0.47
Drive Ferrari-488Spider 97
Drive Ferrari-488Spider 35
Drive AudiA4 85
Drive AudiA4 50
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
AudiA4 1.00 50
BMW-M2 33.00 0
Ferrari-488Spider 4.41 97
[/output]
[/test]
[test]
[input]
3
MustangGTR 80 4.9
FerarriGTR 10 5.5
Moher 10 0.1
Drive MustangGTR 25
Drive MustangGTR 10
Drive FerarriGTR 100
Drive FerarriGTR 1
Drive Moher 101
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
Insufficient fuel for the drive
MustangGTR 31.00 10
FerarriGTR 4.50 1
Moher 10.00 0
[/output]
[/test]
[test]
[input]
5
M1 10 1.1
M2 20 1.2
M3 40 2
M4 40 4
M 100 5
Drive M1 5
Drive M2 20
Drive M 15
Drive M1 70
Drive M3 20
Drive M4 20
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
Insufficient fuel for the drive
M1 4.50 5
M2 20.00 0
M3 0.00 20
M4 40.00 0
M 25.00 15
[/output]
[/test]
[test]
[input]
3
M100 90 6
T 100 5
H 200 7
Drive M100 15
Drive M100 10
Drive T 1000
Drive T 25
Drive H 25
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
Insufficient fuel for the drive
M100 0.00 15
T 100.00 0
H 25.00 25
[/output]
[/test]
[test]
[input]
3
K 5 0.1
S 9 10
T 10 0.2
Drive K 5
Drive K 15
Drive S 100
Drive T 15
End
[/input]
[output]
Insufficient fuel for the drive
K 3.00 20
S 9.00 0
T 7.00 15
[/output]
[/test]
[test]
[input]
5
B 50 1
S 5 0.5
M 1 0.5
D 15 2
K 20 5
Drive B 49
Drive S 10
Drive D 7
Drive D 1
Drive K 3
Drive K 1
Drive M 100
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
B 1.00 49
S 0.00 10
M 1.00 0
D 1.00 7
K 0.00 4
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Problem: Raw Data
[code-task title="Raw Data" taskId="45d1be24-82dd-4ff1-9586-d02e73ff698d" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
You are the owner of a courier company and you want to make a system for tracking your cars and their cargo.

Define a class **Car** that holds information about **model, engine, cargo**, and a **collection of exactly 4 tires**.

The engine, cargo, and tire **should be separate classes**, create a constructor that receives all information about the Car, and creates and initializes its inner components (engine, cargo, and tires).

On the first line of the input you will receive a number **N** - the number of cars you have. 

On each of the next **N** lines you will receive information about a car in the format: 

`<model> <engineSpeed> <enginePower> <cargoWeight> <cargoType> <tire1Pressure> <tire1Age> <tire2Pressure> <tire2Age> <tire3Pressure> <tire3Age> <tire4Pressure> <tire4Age>`

Where the speed, power, weight and tire age are **integers**, tire pressure is a **double**.

After the **N** lines you will receive a single line with one of 2 commands `fragile` or `flamable`.

If the command is `fragile` print all cars whose **cargoType is** `fragile` with a **tire** whose **pressure is < 1**.

If the command is `flamable` print all cars whose **cargoType is** `flamable` and have **enginePower > 250**. 

The cars should be printed in order of appearing in the input on a separate lines.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | Citroen2CV |
| ChevroletAstro 200 180 1000 fragile 1.3 1 1.5 2 1.4 2 1.7 4 |  |
| Citroen2CV 190 165 1200 fragile 0.9 3 0.85 2 0.95 2 1.1 1 |  |
| fragile |  |

| **Input** | **Output** |
| --- | --- |
| 4 | ChevroletExpress |
| ChevroletExpress 215 255 1200 flamable 2.5 1 2.4 2 2.7 1 2.8 1 | DaciaDokker |
| ChevroletAstro 210 230 1000 flamable 2 1 1.9 2 1.7 3 2.1 1 |  |
| DaciaDokker 230 275 1400 flamable 2.2 1 2.3 1 2.4 1 2 1 |  |
| Citroen2CV 190 165 1200 fragile 0.8 3 0.85 2 0.7 5 0.95 2 |  |
| flamable |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
ChevroletAstro 200 180 1000 fragile 1.3 1 1.5 2 1.4 2 1.7 4
Citroen2CV 190 165 1200 fragile 0.9 3 0.85 2 0.95 2 1.1 1
fragile
[/input]
[output]
Citroen2CV
[/output]
[/test]
[test open]
[input]
4
ChevroletExpress 215 255 1200 flamable 2.5 1 2.4 2 2.7 1 2.8 1
ChevroletAstro 210 230 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
DaciaDokker 230 275 1400 flamable 2.2 1 2.3 1 2.4 1 2 1
Citroen2CV 190 165 1200 fragile 0.8 3 0.85 2 0.7 5 0.95 2
flamable
[/input]
[output]
ChevroletExpress
DaciaDokker
[/output]
[/test]
[test]
[input]
5
ChevroletExpress 215 255 1200 flamable 2.5 1 2.4 2 2.7 1 2.8 1
ChevroletAstro 210 230 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
DaciaDokker 230 275 1400 flamable 2.2 1 2.3 1 2.4 1 2 1
Citroen2CV 190 165 1200 fragile 0.8 3 0.85 2 0.7 5 0.95 2
LaTroca 150 350 1500 flamable 2 1 1.9 2 1.7 3 2.1 1
flamable
[/input]
[output]
ChevroletExpress
DaciaDokker
LaTroca
[/output]
[/test]
[test]
[input]
4
C 200 180 1000 fragile 1.3 1 1.5 2 1.4 2 1.7 4
C2 190 165 1200 fragile 0.9 3 0.85 2 0.95 2 1.1 1
M4 300 250 1500 fragile 0.9 4 0.55 2 0.85 2 1.1 2
M 404 404 4004 fragile 0.9 1 0.9 5 0.9 4 3 5
fragile
[/input]
[output]
C2
M4
M
[/output]
[/test]
[test]
[input]
6
ChevroletExpress 215 255 1200 flamable 2.5 1 2.4 2 2.7 1 2.8 1
ChevroletAstro 210 230 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
DaciaDokker 230 275 1400 flamable 2.2 1 2.3 1 2.4 1 2 1
Citroen2CV 190 165 1200 fragile 0.8 3 0.85 2 0.7 5 0.95 2
Chevrolantiq 210 270 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
KappaMobile 210 330 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
flamable
[/input]
[output]
ChevroletExpress
DaciaDokker
Chevrolantiq
KappaMobile
[/output]
[/test]
[test]
[input]
2
ChevroletExpress 215 200 1200 fragile 2.5 1 2.4 2 2.7 1 2.8 1
ChevroletAstro 210 200 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
flamable
[/input]
[output]

[/output]
[/test]
[test]
[input]
1
T 2000 1800 10000 flamable 1.3 1 1.5 2 1.4 2 1.7 4
flamable
[/input]
[output]
T
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Problem: Car Salesman
[code-task title="Car Salesman" taskId="bd8337bb-a2b2-4af9-b2db-ab23ef09eb24" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
Define two classes **Car** and **Engine**.

A **Car** has a **model, engine, weight** and **color**.

An Engine has **model, power, displacement** and **efficiency**.

A Car's **weight** and **color** and its Engine's **displacements** and **efficiency** are **optional**.

On the first line, you will read a number **N** which will specify how many lines of engines you will receive. 

On each of the next **N** lines you will receive information about an **Engine** in the following format:

`<model> <power> <displacement> <efficiency>`

After the lines with engines, on the next line you will receive a number **M** – specifying the number of Cars that will follow. 

On each of the next **M** lines the information about a **Car** will follow in the following format:

`<model> <engine> <weight> <color>`

Where the engine in the format will be the **model of an existing Engine**. 

When creating the object for a **Car**, you should keep a **reference to the real engine** in it, instead of just the engines model, **note** that the optional properties **might be missing** from the formats.

Your task is to print each car (in the **order** you **received** them) and its information in the format defined below. 

If any of the optional fields have not been given print **"n/a"** in its place instead of:

```java
<carModel>
<engineModel>
Power: <enginePower>
Displacement: <engineDisplacement>
Efficiency: <engineEfficiency>
Weight: <carWeight>
Color: <carColor>
```

## Optional

Override the classes **toString()** methods to have a reusable way of displaying the objects.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | FordFocus: |
| V8-101 220 50 | V4-33: |
| V4-33 140 28 B | Power: 140 |
| 3 | Displacement: 28 |
| FordFocus V4-33 1300 Silver | Efficiency: B |
| FordMustang V8-101 | Weight: 1300 |
| VolkswagenGolf V4-33 Orange | Color: Silver |
|  | FordMustang: |
|  | V8-101: |
|  | Power: 220 |
|  | Displacement: 50 |
|  | Efficiency: n/a |
|  | Weight: n/a |
|  | Color: n/a |
|  | VolkswagenGolf: |
|  | V4-33: |
|  | Power: 140 |
|  | Displacement: 28 |
|  | Efficiency: B |
|  | Weight: n/a |
|  | Color: Orange |

| **Input** | **Output** |
| --- | --- |
| 4 | FordMondeo: |
| DSL-10 280 B | DSL-13: |
| V7-55 200 35 | Power: 305 |
| DSL-13 305 55 A+ | Displacement: 55 |
| V7-54 190 30 D | Efficiency: A+ |
| 4 | Weight: n/a |
| FordMondeo DSL-13 Purple | Color: Purple |
| VolkswagenPolo V7-54 1200 Yellow | VolkswagenPolo: |
| VolkswagenPassat DSL-10 1375 Blue | V7-54: |
| FordFusion DSL-13 | Power: 190 |
|  | Displacement: 30 |
|  | Efficiency: D |
|  | Weight: 1200 |
|  | Color: Yellow |
|  | VolkswagenPassat: |
|  | DSL-10: |
|  | Power: 280 |
|  | Displacement: n/a |
|  | Efficiency: B |
|  | Weight: 1375 |
|  | Color: Blue |
|  | FordFusion: |
|  | DSL-13: |
|  | Power: 305 |
|  | Displacement: 55 |
|  | Efficiency: A+ |
|  | Weight: n/a |
|  | Color: n/a |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
V8-101 220 50
V4-33 140 28 B
3
FordFocus V4-33 1300 Silver
FordMustang V8-101
VolkswagenGolf V4-33 Orange
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 28
Efficiency: B
Weight: 1300
Color: Silver
FordMustang:
V8-101:
Power: 220
Displacement: 50
Efficiency: n/a
Weight: n/a
Color: n/a
VolkswagenGolf:
V4-33:
Power: 140
Displacement: 28
Efficiency: B
Weight: n/a
Color: Orange
[/output]
[/test]
[test open]
[input]
4
DSL-10 280 B
V7-55 200 35
DSL-13 305 55 A+
V7-54 190 30 D
4
FordMondeo DSL-13 Purple
VolkswagenPolo V7-54 1200 Yellow
VolkswagenPassat DSL-10 1375 Blue
FordFusion DSL-13
[/input]
[output]
FordMondeo:
DSL-13:
Power: 305
Displacement: 55
Efficiency: A+
Weight: n/a
Color: Purple
VolkswagenPolo:
V7-54:
Power: 190
Displacement: 30
Efficiency: D
Weight: 1200
Color: Yellow
VolkswagenPassat:
DSL-10:
Power: 280
Displacement: n/a
Efficiency: B
Weight: 1375
Color: Blue
FordFusion:
DSL-13:
Power: 305
Displacement: 55
Efficiency: A+
Weight: n/a
Color: n/a
[/output]
[/test]
[test]
[input]
4
V8-101 220 50 A
V4-33 140 28 B
V6-33 230 28 D
V7-44 330 35 E
5
FordFocus V4-33 1300 Silver
Opelche V7-44 1550 Gold
Orel V8-101 1000 Pink
Nissan V8-101 1050 Yellow
Jugan V6-33 2001 Red
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 28
Efficiency: B
Weight: 1300
Color: Silver
Opelche:
V7-44:
Power: 330
Displacement: 35
Efficiency: E
Weight: 1550
Color: Gold
Orel:
V8-101:
Power: 220
Displacement: 50
Efficiency: A
Weight: 1000
Color: Pink
Nissan:
V8-101:
Power: 220
Displacement: 50
Efficiency: A
Weight: 1050
Color: Yellow
Jugan:
V6-33:
Power: 230
Displacement: 28
Efficiency: D
Weight: 2001
Color: Red
[/output]
[/test]
[test]
[input]
5
V8-101 220 50
V4-33 140 28
V6-33 230 28
V7-44 330 35
V12-45 450 60 
7
FordFocus V4-33 1300 Silver
Opelche V7-44 1550 Gold
Orel V8-101 1000 Pink
Nissan V8-101 1050 Yellow
Jugan V6-33 2001 Red
Trabant V12-45 1000 White
Trabant V7-44 600 Green
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 28
Efficiency: n/a
Weight: 1300
Color: Silver
Opelche:
V7-44:
Power: 330
Displacement: 35
Efficiency: n/a
Weight: 1550
Color: Gold
Orel:
V8-101:
Power: 220
Displacement: 50
Efficiency: n/a
Weight: 1000
Color: Pink
Nissan:
V8-101:
Power: 220
Displacement: 50
Efficiency: n/a
Weight: 1050
Color: Yellow
Jugan:
V6-33:
Power: 230
Displacement: 28
Efficiency: n/a
Weight: 2001
Color: Red
Trabant:
V12-45:
Power: 450
Displacement: 60
Efficiency: n/a
Weight: 1000
Color: White
Trabant:
V7-44:
Power: 330
Displacement: 35
Efficiency: n/a
Weight: 600
Color: Green
[/output]
[/test]
[test]
[input]
5
V8-101 220 C
V4-33 140 B
V33-33 220 D
V12-101 340 A
V10-10 210 E+
6
FordFocus V4-33 1300 Silver
Trabant V10-10 600 Gold
Jaguar V8-101 1235 Green
Toyota V33-33 1200 Green
MercedesSmart V8-101 1100 None
MiniCooper V12-101 100 YellowBlack
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: n/a
Efficiency: B
Weight: 1300
Color: Silver
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: E+
Weight: 600
Color: Gold
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: C
Weight: 1235
Color: Green
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: D
Weight: 1200
Color: Green
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: C
Weight: 1100
Color: None
MiniCooper:
V12-101:
Power: 340
Displacement: n/a
Efficiency: A
Weight: 100
Color: YellowBlack
[/output]
[/test]
[test]
[input]
7
V8-101 220
V4-33 140
V33-33 220
V12-101 340
V10-10 210
V11-1110 110
V01-1011 230
10
FordFocus V4-33 1300 Silver
Trabant V10-10 600 Gold
Ford V4-33 650 Red
Jaguar V8-101 1235 Green
Toyota V33-33 1200 Green
Trabant V11-1110 1200 BlackYellow
MercedesSmart V8-101 1100 None
Tesla V01-1011 1230 PinkGreen
MiniCooper V12-101 100 YellowBlack
Motor123 V12-101 1000 JellyBeanColor
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: n/a
Efficiency: n/a
Weight: 1300
Color: Silver
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: n/a
Weight: 600
Color: Gold
Ford:
V4-33:
Power: 140
Displacement: n/a
Efficiency: n/a
Weight: 650
Color: Red
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 1235
Color: Green
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 1200
Color: Green
Trabant:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: n/a
Weight: 1200
Color: BlackYellow
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 1100
Color: None
Tesla:
V01-1011:
Power: 230
Displacement: n/a
Efficiency: n/a
Weight: 1230
Color: PinkGreen
MiniCooper:
V12-101:
Power: 340
Displacement: n/a
Efficiency: n/a
Weight: 100
Color: YellowBlack
Motor123:
V12-101:
Power: 340
Displacement: n/a
Efficiency: n/a
Weight: 1000
Color: JellyBeanColor
[/output]
[/test]
[test]
[input]
7
V8-101 220 220 A
V4-33 140 110 D
V33-33 220 323 C
V12-101 340 325 D
V10-10 210 121 A+
V11-1110 110 450 D++
V01-1011 230 440 B+
11
FordFocus V4-33 1300
Trabant V10-10 600
Ford V4-33 650
Jaguar V8-101 1235
Toyota V33-33 1200
Trabant V11-1110 1200
MercedesSmart V8-101 1100
Tesla V01-1011 1230
MiniCooper V12-101 100
Motor123 V12-101 1001
Kolichka V11-1110 1234
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: 1300
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: 121
Efficiency: A+
Weight: 600
Color: n/a
Ford:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: 650
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: 1235
Color: n/a
Toyota:
V33-33:
Power: 220
Displacement: 323
Efficiency: C
Weight: 1200
Color: n/a
Trabant:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: 1200
Color: n/a
MercedesSmart:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: 1100
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: 440
Efficiency: B+
Weight: 1230
Color: n/a
MiniCooper:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: 100
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: 1001
Color: n/a
Kolichka:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: 1234
Color: n/a
[/output]
[/test]
[test]
[input]
7
V8-101 220 220 A
V4-33 140 110 D
V33-33 220 323 C
V12-101 340 325 D
V10-10 210 121 A+
V11-1110 110 450 D++
V01-1011 230 440 B+
11
FordFocus V4-33 Yellow
Trabant V10-10 Green
Ford V4-33 Black
Jaguar V8-101 White
Toyota V33-33 Red
Trabant V11-1110 None
MercedesSmart V8-101 GrayMetalic
Tesla V01-1011 Gray
MiniCooper V12-101 Purple
Motor123 V12-101 Pink
Kolichka V11-1110 Colorless
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: n/a
Color: Yellow
Trabant:
V10-10:
Power: 210
Displacement: 121
Efficiency: A+
Weight: n/a
Color: Green
Ford:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: n/a
Color: Black
Jaguar:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: n/a
Color: White
Toyota:
V33-33:
Power: 220
Displacement: 323
Efficiency: C
Weight: n/a
Color: Red
Trabant:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: n/a
Color: None
MercedesSmart:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: n/a
Color: GrayMetalic
Tesla:
V01-1011:
Power: 230
Displacement: 440
Efficiency: B+
Weight: n/a
Color: Gray
MiniCooper:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: n/a
Color: Purple
Motor123:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: n/a
Color: Pink
Kolichka:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: n/a
Color: Colorless
[/output]
[/test]
[test]
[input]
7
V8-101 220 220 A
V4-33 140 110 D
V33-33 220 323 C
V12-101 340 325 D
V10-10 210 121 A+
V11-1110 110 450 D++
V01-1011 230 440 B+
11
FordFocus V4-33
Trabant V10-10
Ford V4-33
Jaguar V8-101
Toyota V33-33
Trabant V11-1110
MercedesSmart V8-101
Tesla V01-1011
MiniCooper V12-101
Motor123 V12-101
Kolichka V11-1110
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: n/a
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: 121
Efficiency: A+
Weight: n/a
Color: n/a
Ford:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: n/a
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: n/a
Color: n/a
Toyota:
V33-33:
Power: 220
Displacement: 323
Efficiency: C
Weight: n/a
Color: n/a
Trabant:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: n/a
Color: n/a
MercedesSmart:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: n/a
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: 440
Efficiency: B+
Weight: n/a
Color: n/a
MiniCooper:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: n/a
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: n/a
Color: n/a
Kolichka:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: n/a
Color: n/a
[/output]
[/test]
[test]
[input]
7
V8-101 220
V4-33 140
V33-33 220
V12-101 340
V10-10 210
V11-1110 110
V01-1011 230
12
FordFocus V4-33
Trabant V10-10
Ford V4-33
Jaguar V8-101
Toyota V33-33
Trabant V11-1110
MercedesSmart V8-101
Tesla V01-1011
MiniCooper V12-101
Motor123 V12-101
Kolichka V11-1110
Tracktorche V8-101
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Ford:
V4-33:
Power: 140
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Trabant:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
MiniCooper:
V12-101:
Power: 340
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Kolichka:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Tracktorche:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
[/output]
[/test]
[test]
[input]
7
V8-101 220
V4-33 140 430
V33-33 220 E+
V12-101 340 230 A++
V10-10 210
V11-1110 110 C
V01-1011 230 330
12
FordFocus V4-33
Trabant V10-10
Ford V4-33
Jaguar V8-101
Toyota V33-33
Trabant V11-1110
MercedesSmart V8-101
Tesla V01-1011
MiniCooper V12-101
Motor123 V12-101
Kolichka V11-1110
Tracktorche V8-101
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 430
Efficiency: n/a
Weight: n/a
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Ford:
V4-33:
Power: 140
Displacement: 430
Efficiency: n/a
Weight: n/a
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: E+
Weight: n/a
Color: n/a
Trabant:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: C
Weight: n/a
Color: n/a
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: 330
Efficiency: n/a
Weight: n/a
Color: n/a
MiniCooper:
V12-101:
Power: 340
Displacement: 230
Efficiency: A++
Weight: n/a
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: 230
Efficiency: A++
Weight: n/a
Color: n/a
Kolichka:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: C
Weight: n/a
Color: n/a
Tracktorche:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
[/output]
[/test]
[test]
[input]
8
V8-101 220
V4-33 140 430
V33-33 220 E+
V12-101 340 230 A++
V10-10 210
V11-1110 110 C
V01-1011 230 330
V22-22 323 100 A-
13
FordFocus V4-33
Trabant V10-10 Yellow
Ford V4-33 1230
Jaguar V8-101 1200 Green
Toyota V33-33 900 Purple
Trabant V11-1110 1000
Lambo V22-22 999 Gold
MercedesSmart V8-101
Tesla V01-1011 GreenishPurple
MiniCooper V12-101 9000
Motor123 V12-101 790 Colorful
Kolichka V11-1110 Colorless
Tracktorche V8-101 899 Gray
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 430
Efficiency: n/a
Weight: n/a
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: Yellow
Ford:
V4-33:
Power: 140
Displacement: 430
Efficiency: n/a
Weight: 1230
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 1200
Color: Green
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: E+
Weight: 900
Color: Purple
Trabant:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: C
Weight: 1000
Color: n/a
Lambo:
V22-22:
Power: 323
Displacement: 100
Efficiency: A-
Weight: 999
Color: Gold
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: 330
Efficiency: n/a
Weight: n/a
Color: GreenishPurple
MiniCooper:
V12-101:
Power: 340
Displacement: 230
Efficiency: A++
Weight: 9000
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: 230
Efficiency: A++
Weight: 790
Color: Colorful
Kolichka:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: C
Weight: n/a
Color: Colorless
Tracktorche:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 899
Color: Gray
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Problem: Pokemon Trainer
[code-task title="Pokemon Trainer" taskId="557a0bbb-06f1-4916-aa67-034874e07cbd" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
You wanna be the very best pokemon trainer, like no one ever was, so you set out to catch pokemon.

Define a class **Trainer** and a class **Pokemon**.

Trainer has a **name**, **number of badges** and a **collection of pokemon**.

Pokemon has a **name**, an **element** and **health**, all values are **mandatory**.

Every Trainer **starts with 0 badges**.

From the console you will receive an unknown number of lines until you receive the command `Tournament`. 

Each line will carry information about a pokemon and the trainer who caught it in the format:

`<trainerName> <pokemonName> <pokemonElement> <pokemonHealth>` 

Where **trainerName** is the name of the Trainer who caught the pokemon. 

Names are **unique**, there can not be 2 trainers with the same name. 

After receiving the command `Tournament` an unknown number of lines containing one of three elements **"Fire"**, **"Water"**, **"Electricity"** will follow until the command `End` is received. 

For every command you must check if a trainer has **at least 1** pokemon with the given element. 

If he does, he receives 1 badge, otherwise all his pokemon **lose 10 health**. 

If a pokemon falls **to 0 or less health he dies** and must be deleted from the trainer's collection. 

After the command `End` is received you should print all trainers **sorted by the number of badges they have in descending order**. 

If two trainers have the same amount of badges they should be sorted by order of appearance in the input. 

Print in the format:

`<trainerName> <badges> <numberOfPokemon>`

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter Charizard Fire 100 | Peter 2 2 |
| John Squirtle Water 38 | John 0 1 |
| Peter Pikachu Electricity 10 |  |
| Tournament |  |
| Fire |  |
| Electricity |  |
| End |  |

| **Input** | **Output** |
| --- | --- |
| Stan Blastoise Water 18 | Nick 1 1 |
| Nick Pikachu Electricity 22 | Stan 0 0 |
| John Kadabra Psychic 90 | John 0 1 |
| Tournament |  |
| Fire |  |
| Electricity |  |
| Fire |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter Charizard Fire 100
John Squirtle Water 38
Peter Pikachu Electricity 10
Tournament
Fire
Electricity
End
[/input]
[output]
Peter 2 2
John 0 1
[/output]
[/test]
[test open]
[input]
Stan Blastoise Water 18
Nick Pikachu Electricity 22
John Kadabra Psychic 90
Tournament
Fire
Electricity
Fire
End
[/input]
[output]
Nick 1 1
Stan 0 0
John 0 1
[/output]
[/test]
[test]
[input]
P Charizard Fire 100
G Squirtle Water 38
P Pikachu Electricity 10
M Balbazor Fire 101
Tournament
End
[/input]
[output]
P 0 2
G 0 1
M 0 1
[/output]
[/test]
[test]
[input]
P Charizard Fire 100
G Squirtle Water 38
P Pikachu Electricity 10
P Balbazor Electricity 102
G Buterfree Fire 11
Tournament
End
[/input]
[output]
P 0 3
G 0 2
[/output]
[/test]
[test]
[input]
P Charizard Fire 100
M MiniCharizard Fire 50
P BigCharizard Fire 120
P FirePokemon Fire 101
M Char Fire 100
J Turtle Water 100
J BigTurtle Water 250
Tournament
Fire
Fire
Fire
Fire
End
[/input]
[output]
P 4 3
M 4 2
J 0 2
[/output]
[/test]
[test]
[input]
G Golem Water 102
P Charizard Water 100
M MiniCharizard Water 50
P BigCharizard Water 120
P FirePokemon Water 101
M Char Fire 100
J Turtle Electricity 100
J BigTurtle Fire 250
Tournament
Water
Water
Water
Water
Water
Water
End
[/input]
[output]
G 6 1
P 6 3
M 6 2
J 0 2
[/output]
[/test]
[test]
[input]
G Golem Water 102
P Charizard Water 100
M MiniCharizard Water 50
P BigCharizard Water 120
P FirePokemon Water 101
M Char Electricity 100
J Turtle Electricity 100
J BigTurtle Fire 250
Tournament
Electricity
Electricity
Electricity
Electricity
End
[/input]
[output]
M 4 2
J 4 2
G 0 1
P 0 3
[/output]
[/test]
[test]
[input]
G Golem Water 102
P Charizard Water 100
M MiniCharizard Water 30
P BigCharizard Water 120
P FirePokemon Water 101
M Char Electricity 100
J Turtle Electricity 100
J BigTurtle Water 250
Tournament
Fire
Fire
Fire
Fire
Fire
End
[/input]
[output]
G 0 1
P 0 3
M 0 1
J 0 2
[/output]
[/test]
[test]
[input]
G Golem Fire 102
P Charizard Fire 100
M MiniCharizard Fire 30
P BigCharizard Fire 120
P FirePokemon Electricity 101
M Char Electricity 100
J Turtle Electricity 10
J BigTurtle Fire 25
Tournament
Water
Water
Water
Water
Water
Water
Water
End
[/input]
[output]
G 0 1
P 0 3
M 0 1
J 0 0
[/output]
[/test]
[test]
[input]
G Golem Fire 102
P Charizard Fire 100
M MiniCharizard Fire 30
P BigCharizard Fire 120
P FirePokemon Water 11
M Char Water 10
J Turtle Fire 10
J BigTurtle Fire 2500
Tournament
Electricity
Electricity
Electricity
Electricity
Electricity
End
[/input]
[output]
G 0 1
P 0 2
M 0 0
J 0 1
[/output]
[/test]
[test]
[input]
An Balbazor Water 100
A Pikachu Electricity 100
Annie Squirtal Fire 100
P Balbazor Water 100
P Electricity Electricity 100
P Balbazor2 Fire 100
Tournament
Fire
Water
Electricity
End
[/input]
[output]
P 3 3
An 1 1
A 1 1
Annie 1 1
[/output]
[/test]
[test]
[input]
S Blastoise Water 18
N Pikachu Electricity 22
N Pikachu2 Electricity 200
N Pikachu3 Electricity 21
N Pikachu4 Electricity 23
N Pikachu5 Electricity 230
J Kadabra Psychic 90
S Squirtle Water 1200
P TurtoiseSVN Water 500
P Charizard Water 50
G Flower Fire 10
Tournament
Electricity
Fire
Water
Fire
Electricity
Fire
Water
Electricity
Electricity
Water
Water
Water
Water
Electricity
Fire
Fire
End
[/input]
[output]
S 6 1
P 6 1
N 5 2
J 0 0
G 0 0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Problem: Personal Information
[code-task title="Personal Information" taskId="5d118095-25ac-454f-b83d-562694f855fa" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
*You and your friends decide to create a Class that holds all the information about all of you, even your pokemon collection. Since you are good at writing code, they asked you to design that Class.*

From the console you will receive lines until the command `End`.

Each of those lines contains information about a person in one of the following formats:

- `{personName} company {companyName} {department} {salary}`

- `{personName} pokemon {pokemonName} {pokemonType}`

- `{personName} parents {parentName} {parentBirthday}`

- `{personName} children {childName} {childBirthday}`

- `{personName} car {carModel} {carSpeed}`

You should structure all information about a person in a class with nested subclasses. 

Person names are **unique** - there won't be 2 person with the same name.

A person can have **only one company** and **one car**, but can have **multiple parents, children** and **pokemon**. 

After the command `End` you will receive a **single** name on the next line.

You should **print** all information about that person. 

**Note** that the information can change **during** the **input**.

For example, if you receive multiple lines which specify a person company, only the **last one** should be the one remembered. 

The salary must be formatted to **the second decimal place**.

Print the information in the following format:

```java
{personName}
Company:
{companyName} {companyDepartment} {salary}
Car:
{carModel} {carSpeed}
Pokemon:
{pokemonName} {pokemonType}
Parents:
{parentName} {parentBirthday}
Children:
{childName} {childBirthday}
```

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter company PeshInc Management 1000.00 | Tom |
| Tom car Volvo 30 | Company: |
| Peter pokemon Pikachu Electricity | Car: |
| Peter parents JohnDoe 22/02/1920 | Volvo 30 |
| Tom pokemon Electrode Electricity | Pokemon: |
| End | Electrode Electricity |
| Tom | Parents: |
|  | Children: |


| **Input** | **Output** |
| --- | --- |
| JohnDoe pokemon Onyx Rock | JohnDoe |
| JohnDoe parents JJ 13/03/1933 | Company: |
| GeorgeAdams pokemon Moltres Fire | JLtd Jelior 777.77 |
| JohnDoe company JLtd Jelior 777.77 | Car: |
| JohnDoe children PJ 01/01/2001 | AudiA4 180 |
| StanSmith pokemon Blastoise Water | Pokemon: |
| JohnDoe car AudiA4 180 | Onyx Rock |
| JohnDoe pokemon Charizard Fire | Charizard Fire |
| End | Parents: |
| JohnDoe | JJ 13/03/1933 |
|  | Children: |
|  | PJ 01/01/2001 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter company PeshInc Management 1000.00
Tom car Volvo 30
Peter pokemon Pikachu Electricity
Peter parents JohnDoe 22/02/1920
Tom pokemon Electrode Electricity
End
Tom
[/input]
[output]
Tom
Company:
Car:
Volvo 30
Pokemon:
Electrode Electricity
Parents:
Children:
[/output]
[/test]
[test open]
[input]
JohnDoe pokemon Onyx Rock
JohnDoe parents JJ 13/03/1933
GeorgeAdams pokemon Moltres Fire
JohnDoe company JLtd Jelior 777.77
JohnDoe children PJ 01/01/2001
StanSmith pokemon Blastoise Water
JohnDoe car AudiA4 180
JohnDoe pokemon Charizard Fire
End
JohnDoe
[/input]
[output]
JohnDoe
Company:
JLtd Jelior 777.77
Car:
AudiA4 180
Pokemon:
Onyx Rock
Charizard Fire
Parents:
JJ 13/03/1933
Children:
PJ 01/01/2001
[/output]
[/test]
[test]
[input]
K company JC CEO 2000.00
K pokemon P P
K car Audi 50
S parents MJ 19/01/1950
S children KK 20/09/1992
S pokemon B B
End
S
[/input]
[output]
S
Company:
Car:
Pokemon:
B B
Parents:
MJ 19/01/1950
Children:
KK 20/09/1992
[/output]
[/test]
[test]
[input]
K pokemon C C
K pokemon S S
K pokemon S W
K car L 100
M car L 99
M car S 98
E parents P 19/09/1999
E children H 19/08/1998
End
K
[/input]
[output]
K
Company:
Car:
L 100
Pokemon:
C C
S S
S W
Parents:
Children:
[/output]
[/test]
[test]
[input]
V children AR 01/05/1995
A pokemon RA Water
A children IJ 02/06/1993
A car BMW 120
A company SoftUni Janitor 5.00
A parents SN 06/06/1966
End
A
[/input]
[output]
A
Company:
SoftUni Janitor 5.00
Car:
BMW 120
Pokemon:
RA Water
Parents:
SN 06/06/1966
Children:
IJ 02/06/1993
[/output]
[/test]
[test]
[input]
D pokemon Z Z
D parents TB 01/01/1983
D company DC P 500
K company NL JD 2000
K pokemon K K
K parents P 07/23/1960
KT company B CG 100
KT pokemon T T
End
K
[/input]
[output]
K
Company:
NL JD 2000.00
Car:
Pokemon:
K K
Parents:
P 07/23/1960
Children:
[/output]
[/test]
[test]
[input]
T company H EM 999999.99
T children H 01/01/1000
T children A 01/01/1000
T children LR 01/01/1000
T parents N 00/00/0000
T pokemon MR S
End
T
[/input]
[output]
T
Company:
H EM 999999.99
Car:
Pokemon:
MR S
Parents:
N 00/00/0000
Children:
H 01/01/1000
A 01/01/1000
LR 01/01/1000
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Problem: Family Tree
[code-task title="Family Tree" taskId="102bcf46-b2bb-4218-b78d-86641c10eeec" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
*You want to build your family tree, so you went to ask your grandmother. Sadly your grandmother keeps remembering information about your predecessors in pieces, so it falls to you to group the information and build the family tree.*

On the first line of the input, you will receive either a name or a birthdate in the format:

`<FirstName> <LastName>` or `day/month/year`

Your task is to find information about the person in the family tree. 

On the next lines, until the command `End`, you will receive information about your predecessors that is needed for the family tree.

The information will be in one of the following formats:

- `firstName lastName - firstName lastName`
- `firstName lastName - day/month/year`
- `day/month/year - firstName lastName`
- `day/month/year - day/month/year`
- `firstName lastName day/month/year`

The first 4 formats reveal a family tie: 

The person **on the left** is the **parent** to the person **on the right**.

The format can be **without names**. 

For example, the 4th format means the person **born on the left date** is the **parent to the person born on the right** date. 

The last format ties **different** information together – i.e. **the person with that name was born on that date**. 

**Names** and **birthdates** are **unique** – there won't be two persons with the same name or birthdate. 

There will **always** be enough entries to construct the family tree (all people names and birthdates are known and they have **at least one** connection to another person in the tree).

After the command `End` is received you should print all information about the person whose name or birthdate you received on the first line – his **name, birthday, parents, and children** (check the examples for the format). 

The people in the parents and children lists should be **ordered** by their **first appearance** in the input.

Regardless if they appeared as a birthdate or a name. 

For example in the first input Stan is before Jenny because his birthdate appeared first in the second line, while she appeared in the third line.

## Examples
| **Input** | **Output** |
| --- | --- |
| John Baker | John Baker 23/05/1980 |
| 11/11/1951 - 23/05/1980 | Parents: |
| Jenny Baker - 23/05/1980 | Stan Baker 11/11/1951 |
| Jenny Baker 09/02/1953 | Jenny Baker 09/02/1953 |
| John Baker - Garrett Baker | Children: |
| Garrett Baker 01/01/2005 | Garrett Baker 01/01/2005 |
| Stan Baker 11/11/1951 |  |
| John Baker 23/05/1980 |  |
| End |  |

| **Input** | **Output** |
| --- | --- |
| 13/12/1993 | Christopher Williams 13/12/1993 |
| 25/03/1934 - 04/04/1961 | Parents: |
| Leonard Williams 25/03/1934 | Benjamin Williams 04/04/1961 |
| 04/04/1961 - Christopher Williams | Children: |
| Benjamin Williams - Edward Williams |  |
| Christopher Williams 13/12/1993 |  |
| Edward Williams 07/07/1995 |  |
| Benjamin Williams 04/04/1961 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
John Baker
11/11/1951 - 23/05/1980
Jenny Baker - 23/05/1980
Jenny Baker 09/02/1953
John Baker - Garrett Baker
Garrett Baker 01/01/2005
Stan Baker 11/11/1951
John Baker 23/05/1980
End
[/input]
[output]
John Baker 23/05/1980
Parents:
Stan Baker 11/11/1951
Jenny Baker 09/02/1953
Children:
Garrett Baker 01/01/2005
[/output]
[/test]
[test open]
[input]
13/12/1993
25/03/1934 - 04/04/1961
Leonard Williams 25/03/1934
04/04/1961 - Christopher Williams
Benjamin Williams - Edward Williams
Christopher Williams 13/12/1993
Edward Williams 07/07/1995
Benjamin Williams 04/04/1961
End
[/input]
[output]
Christopher Williams 13/12/1993
Parents:
Benjamin Williams 04/04/1961
Children:
[/output]
[/test]
[test]
[input]
17/8/1950
P0 P - P8 P
P0 P 17/8/1950
P8 P - P1 P
P1 P 17/10/2001
26/5/1948 - P2 P
P2 P 13/5/1973
17/2/1952 - P P
P3 P 17/2/1952
P11 P - P4 P
P4 P 16/7/1998
26/5/1948 - P5 P
P5 P 21/1/1973
26/5/1948 - P5 P
P6 P 26/5/1948
21/1/1973 - P7 P
P7 P 18/10/2002
26/5/1948 - 28/1/1974
P8 P 28/1/1974
26/5/1948 - 23/4/1973
P9 P 23/4/1973
13/5/1973 - P10 P
P10 P 16/11/1998
P6 P - P11 P
P11 P 24/4/1977
24/7/1951 - 21/1/1973
P12 P 24/7/1951
End
[/input]
[output]
P0 P 17/8/1950
Parents:
Children:
P8 P 28/1/1974
[/output]
[/test]
[test]
[input]
6/9/1927
P7 P - 12/1/1974
P0 P 12/1/1974
17/2/1950 - 10/3/1975
P1 P 10/3/1975
P10 P - P2 P
P2 P 26/5/1924
17/2/1950 - P3 P
P3 P 28/12/1973
P1 P - 21/9/1998
P4 P 21/9/1998
P1 P - P5 P
P5 P 27/11/1998
P10 P - P6 P
P6 P 6/9/1927
P2 P - 17/2/1950
P7 P 17/2/1950
28/12/1973 - P8 P
P8 P 12/12/1999
P10 P - 10/7/1927
P9 P 10/7/1927
6/9/1900 - P9 P
P10 P 6/9/1900
End
[/input]
[output]
P6 P 6/9/1927
Parents:
P10 P 6/9/1900
Children:
[/output]
[/test]
[test]
[input]
Abc12 Abcde
3/10/1927 - 23/10/1951
Abc0 Abcde 3/10/1927
3/4/1923 - Abc1 Abcde
Abc1 Abcde 26/8/1951
3/10/1927 - Abc2 Abcde
Abc2 Abcde 24/6/1948
Abc4 Abcde - 5/2/1998
Abc3 Abcde 5/2/1998
Abc1 Abcde - 4/3/1977
Abc4 Abcde 4/3/1977
3/10/1927 - Abc5 Abcde
Abc5 Abcde 6/3/1951
Abc4 Abcde - 16/12/1998
Abc6 Abcde 16/12/1998
3/4/1923 - Abc7 Abcde
Abc7 Abcde 23/10/1951
Abc4 Abcde - 10/2/1999
Abc8 Abcde 10/2/1999
Abc4 Abcde - 23/11/2001
Abc9 Abcde 23/11/2001
Abc4 Abcde - 18/8/2000
Abc10 Abcde 18/8/2000
Abc4 Abcde - 21/6/2002
Abc11 Abcde 21/6/2002
Abc12 Abcde 3/4/1923
4/3/1977 - Abc13 Abcde
Abc13 Abcde 2/6/2001
End
[/input]
[output]
Abc12 Abcde 3/4/1923
Parents:
Children:
Abc1 Abcde 26/8/1951
Abc7 Abcde 23/10/1951
[/output]
[/test]
[test]
[input]
9/9/1975
Abc9 Abcde - 14/12/1948
Abc0 Abcde 14/12/1948
Abc9 Abcde - Abc1 Abcde
Abc1 Abcde 6/11/1952
Abc9 Abcde - Abc2 Abcde
Abc2 Abcde 10/6/1951
Abc6 Abcde - Abc3 Abcde
Abc3 Abcde 1/5/1999
Abc9 Abcde - Abc4 Abcde
Abc4 Abcde 20/8/1949
10/6/1951 - Abc5 Abcde
Abc5 Abcde 5/8/1973
14/12/1948 - Abc6 Abcde
Abc6 Abcde 9/9/1975
14/12/1948 - 14/1/1975
Abc7 Abcde 14/1/1975
Abc1 Abcde - Abc8 Abcde
Abc8 Abcde 7/10/1976
Abc9 Abcde - Abc1 Abcde
Abc9 Abcde 11/5/1925
Abc4 Abcde - 9/5/1976
Abc10 Abcde 9/5/1976
End
[/input]
[output]
Abc6 Abcde 9/9/1975
Parents:
Abc0 Abcde 14/12/1948
Children:
Abc3 Abcde 1/5/1999
[/output]
[/test]
[test]
[input]
14/6/1950
21/9/1899 - Abc9 Abcde
Abc0 Abcde 21/9/1899
22/2/1898 - 17/12/1924
Abc1 Abcde 17/12/1924
21/9/1899 - 11/2/1925
Abc2 Abcde 11/2/1925
22/2/1898 - Abc3 Abcde
Abc3 Abcde 20/7/1927
22/2/1898 - 11/2/1925
Abc4 Abcde 22/2/1898
19/6/1901 - 11/11/1926
Abc5 Abcde 11/11/1926
Abc5 Abcde - Abc6 Abcde
Abc6 Abcde 27/8/1952
14/6/1950 - 26/9/1974
Abc7 Abcde 26/9/1974
Abc2 Abcde - Abc8 Abcde
Abc8 Abcde 14/6/1950
Abc4 Abcde - Abc9 Abcde
Abc9 Abcde 17/3/1923
Abc10 Abcde - 17/12/1924
Abc10 Abcde 19/6/1901
End
[/input]
[output]
Abc8 Abcde 14/6/1950
Parents:
Abc2 Abcde 11/2/1925
Children:
Abc7 Abcde 26/9/1974
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Problem: Cat Catalog
[code-task title="Cat Catalog" taskId="750f758d-a8a6-479e-8d6e-0246f198c1ec" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
*The people from a pet shelter need to have a catalog of their cats with the breed and special characteristics.*

There are 3 special breeds of cats **"Siamese"**, **"Cymric"** and **"DomesticShorthair"**. 

**Each breed** has a special **characteristic**. 

For example, the special characteristic of the **Siamese** cats is their **ear size**, of **Cymric** cats - the **length of their fur** in millimeters and of the DomesticShorthair the **volume of their meowing**.

All the information about the cats, their breed and characteristics should be collected.

From the console you will receive lines of information about a cat until the command `End`.

The information will come in **one of** the following formats:

- `Siamese <name> <earSize>`
- `Cymric <name> <furLength>`
- `DomesticShorthair  <name> <meowingVolume>`

On the last line after the command `End` you will receive а **name** of a cat. 

You should print that cat and round the number of its s **two digits** after the decimal separator.

## Examples
| **Input** | **Output** |
| --- | --- |
| DomesticShorthair Kitty 85 | Cymric Tom 28.00 |
| Siamese Sim 4 |  |
| Cymric Tom 28 |  |
| End |  |
| Tom |  |

| **Input** | **Output** |
| --- | --- |
| DomesticShorthair Tom 80 | DomesticShorthair Kitty 100.00 |
| DomesticShorthair Kitty 100 |  |
| Cymric Tim 31 |  |
| End |  |
| Kitty |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
DomesticShorthair Kitty 85
Siamese Sim 4
Cymric Tom 28
End
Tom
[/input]
[output]
Cymric Tom 28.00
[/output]
[/test]
[test open]
[input]
DomesticShorthair Tom 80
DomesticShorthair Kitty 100
Cymric Tim 31
End
Kitty
[/input]
[output]
DomesticShorthair Kitty 100.00
[/output]
[/test]
[test]
[input]
Siamese Tony 5
Siamese Toncat 6
Siamese Antoan 5
Siamese Antony 5
Siamese Tonny 5
DomesticShorthair Kappa 95
Cymric Keepo 4.41
End
Toncat
[/input]
[output]
Siamese Toncat 6.00
[/output]
[/test]
[test]
[input]
DomesticShorthair Meow 90
DomesticShorthair Moow 91
DomesticShorthair Moew 92
Siamese Simon 5
Siamese Simmy 4
Cymric Kolly 3.20
Cymric Munny 2.30
End
Kolly
[/input]
[output]
Cymric Kolly 3.20
[/output]
[/test]
[test]
[input]
Cymric TommyTheCat 5.10
End
TommyTheCat
[/input]
[output]
Cymric TommyTheCat 5.10
[/output]
[/test]
[test]
[input]
DomesticShorthair Jerry 91
DomesticShorthair Was 92
DomesticShorthair A 93
DomesticShorthair Racecar 94
DomesticShorthair Driver 95
End
Jerry
[/input]
[output]
DomesticShorthair Jerry 91.00
[/output]
[/test]
[test]
[input]
DomesticShorthair Loly 61
Siamese Rony 4
Cymric Tommy 8.20
Cymric Dan 4.20
DomesticShorthair NoCat 1
DomesticShorthair CatCat 120
Cymric Wirehair 5.00
End
CatCat
[/input]
[output]
DomesticShorthair CatCat 120.00
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Homework Results
[tasks-results/]

[/slide]

