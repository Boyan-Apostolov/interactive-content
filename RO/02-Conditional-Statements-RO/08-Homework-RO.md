// sectionId: "Javascript-Programming-Basics-Conditional-Statements-Homework

# Temă
[slide hideTitle]

# Problemă: Guess the Password
 
[code-task title="Guess the Password" taskId="pb-js-Conditions-Guess-The-Password" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]

```js
function guessThePassword(input) {
  // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Enunț
Scrieți un program pentru a verifica o parolă:

* Citiți un string pentru: parola **guess**
  * Imprimați `Welcome` dacă parola este `s3cr3t!`
  * Imprimați `Wrong password!` în orice altă situație

# Exemplu

| **Input** | **Output** |
| --- | --- |
| s3cr3t! | Welcome |
| qwerty | Wrong password! |

[/task-description]
[tests]
[test]
[input]
s3cr3t!
[/input]
[output]
Welcome
[/output]
[/test]
[test]
[input]
wrong
[/input]
[output]
Wrong password!
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă: Boiling Water

[code-task title="Boiling Water" taskId="pb-js-Conditions-Boiling-Water" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```js
function boilingWater(input) {
    // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Enunț
Scrieți un program care caută apă la fierbere: 

* Citiți un număr în virgulă mobilă: temperatura  **temperature** (in °C)

* Imprimați `The water is boiling` dacă numărul este `>100`

* Imprimați `The water is not hot enough` în orice altă situație

  # Exemplu

| **Input** | **Output** |
| --- | --- |
| 104.8 | The water is boiling |
| 29 | The water is not hot enough |

[/task-description]
[tests]
[test]
[input]
105
[/input]
[output]
The water is boiling
[/output]
[/test]
[test]
[input]
10
[/input]
[output]
The water is not hot enough
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă: Speed Info

[code-task title="Speed Info" taskId="pb-js-Conditions-Speed-Info" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```js
function speedInfo(input) {
  // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Enunț
Scrieți un program pentru a verifica viteza mare/mică: 

* Citiți  **speed** (un număr floating-point)

* Imprimați `Slow` dacă viteza este `<= 30`

* Imprimați `Fast` dacă viteza este `> 30`

  # Exemplu

| **Input** | **Output** |
| --- | --- |
| 30 | Slow |
| 60 | Fast |

[/task-description]
[tests]
[test]
[input]
30
[/input]
[output]
Slow
[/output]
[/test]
[test]
[input]
43
[/input]
[output]
Fast
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă: Bonus Score
[code-task title="Bonus Score" taskId="pb-js-Conditions-Bonus-Score" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```js
function bonusScore(input) {
  // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Enunț

Avem un integer cu datele ințiale **number** de puncte.

**Bonus points** sunt oferite, în funcție de regulile descrise mai jos. 

Scrieți o funcție care calculează 

- punctele bonus **received** din număr 

- care este valoarea inițială **total number of points** - Care este valoarea **number plus the bonus points.**

Dacă numărul este sub valoarea **100 inclusive**, atunci punctele bonus sunt **5**.
Dacă numărul este **greater than 100**, punctele bonus sunt **20 percent of the number**.
Dacă numărul este **greater than 1000**, punctele bonus sunt **10 percent of the number**.

Punctele adiționale din bonus, sunt obținute separat din cele anterioare:

- Pentru un număr impar, adăugați 1 punct

-	Pentru un număr care se termină cu 5, adăugați 2 puncte 

# Exemplu

| **Input** | **Output** |
| --- | --- |
| 20| 6 |
|  |26 |

| **Input** | **Output** |
| --- | --- |
| 175| 37 |
|  |212 |

| **Input** | **Output** |
| --- | --- |
| 2703| 270.3 |
|  |2973.3 |

[/task-description]
[tests]
[test]
[input]
20
[/input]
[output]
6
26
[/output]
[/test]
[test]
[input]
140
[/input]
[output]
29
169
[/output]
[/test]
[test]
[input]
175
[/input]
[output]
37
212
[/output]
[/test]
[test]
[input]
35
[/input]
[output]
7
42
[/output]
[/test]
[test]
[input]
17
[/input]
[output]
5
22
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
6
6
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă: Tickets
[code-task title="Tickets" taskId="pb-js-Conditions-Tickets" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```js
function tickets(input) {
  // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Enunț
Scrieți un program care să calculeze prețul unui bilet:

* Citiți tipul de bilet: fie **student** fie **regular**

* Imprimați **price** în formatul următor`${price}`:

    * Prețul trebuie să fie **formatted** cu 2 cifre după punctul de zecimale 

* Prețul unui bilet de student: **1.00**

* Prețul unui bilet obișnuit: **1.60**

* Pentru un tip nevalid, imprimați `Invalid ticket type!`

# Exemplu

| **Input** | **Output** |
| --- | --- |
| student | $1.00 |


[/task-description]
[tests]
[test]
[input]
student
[/input]
[output]
$1.00
[/output]
[/test]
[test]
[input]
regular
[/input]
[output]
$1.60
[/output]
[/test]
[test]
[input]
ticket
[/input]
[output]
Invalid ticket type!
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

