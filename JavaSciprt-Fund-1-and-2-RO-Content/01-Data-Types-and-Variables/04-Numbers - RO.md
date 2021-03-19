[slide hideTitle]

# Ce Este un Număr?

Numerele în JavaScript nu au tipuri separate pentru **numerele întregi** și pentru **numerele zecimale.**

Avem un singur tip care se numește **numere.**

Cel mai mare număr care poate fi stocat este `2^54 +-1`

Avem, de asemenea, valori speciale, precum:

- `+Infinit` și `-Infinit` pe care le obținem când împărțim numerele la 0

``` js live
console.log(5 / 0);
console.log(-5 / 0);
```

Vom obține infinit pentru a nu obține ca rezultat **eroare de timp de compilare.**

- `NaN` (sau așa numitul non-număr):  Putem obține NaN când încercăm să parsăm un șir care nu poate fi parsat sau când vrem să împărțim la 0:

``` js live
let nanVar = Number('not a number');
console.log(nanVar);
```

Problema operațiilor cu `NaN` este atunci când o folosim din **perspectivă strict matematică**, pentru că vom obține mereu acest rezultat. 

Dacă avem o **logică în programul nostru care dă ca rezultat** `NaN`, și apoi avem orice altă **operație matematică**, rezultatul va fi mereu `NaN`. 

Acest lucru poate să dea logica programului nostru peste cap.

``` js live
let nanVar = Number('not a number');
console.log(5 + nanVar);
```

## Parsarea Numerelor

Parsarea numerelor poate fi făcută în câteva moduri:

- folosind `parseInt`: preluăm doar partea întreagă a unui număr, fără a-l rotunji

``` js live
let myVar = parseInt('3.14');
console.log(myVar);
```

- folosind `parseFloat`: preluăm numărul așa cum este el, împreună cu zecimalele sale

``` js live
let myVar = parseFloat('3.14');
console.log(myVar);
```

- folosind `Number`: parsăm un șir ca număr

``` js live
let myVar = Number('10');
console.log(myVar + 10);
```
[/slide]

[slide hideTitle]


# Problem with Solution: Număr întreg sau număr cu zecimală

[code-task title="Integer or Float" taskId="fund-js-data-types-and-variables-lab-integer-or-float" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function integerOrFloat(firstNumber, secondNumber, thirdNumber){
  // Scrieți codul dvs. aici
}
```
[/code-editor]
[code-adapter]
```
function adapter(input, code) {
    let inputParams = /\((.+)\)$/.exec(input)[1];
    inputParams = eval(`[${inputParams}]`);
    return code(...inputParams);
}
```
[/code-adapter]
[task-description]
# Descrierea problemei
Veți primi **trei numere**. 

Sarcina voastră este să aflați **suma** acestora și s-o tipăriți pe consolă, folosind adunarea 

"\{**number**\} - **Integer or Float**"


# Exemplus
  | **Date de intrare** | **Rezultat** |
| --- | --- |
| integerOrFloat(9, 100, 1.1) | 110.1 - Float |
| integerOrFloat(100, 200, 303) | 603 - Integer|

[/task-description]
[code-io /]
[tests]
[test open]
[input]
integerOrFloat(9, 100, 1.1)
[/input]
[output]
110.1 - Float
[/output]
[/test]
[test open]
[input]
integerOrFloat(100, 200, 303)
[/input]
[output]
603 - Integer
[/output]
[/test]
[test]
[input]
integerOrFloat(9, 14156, 1231.41)
[/input]
[output]
15396.41 - Float
[/output]
[/test]
[test]
[input]
integerOrFloat(456, 120, 145.41)
[/input]
[output]
721.41 - Float
[/output]
[/test]
[test]
[input]
integerOrFloat(912, 54610, 451.11)
[/input]
[output]
55973.11 - Float
[/output]
[/test]
[test]
[input]
integerOrFloat(56, 2120, 3203)
[/input]
[output]
5379 - Integer
[/output]
[/test]
[test]
[input]
integerOrFloat(170, 2098, 483)
[/input]
[output]
2751 - Integer
[/output]
[/test]
[test]
[input]
integerOrFloat(10990, 78, 483)
[/input]
[output]
11551 - Integer
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]
