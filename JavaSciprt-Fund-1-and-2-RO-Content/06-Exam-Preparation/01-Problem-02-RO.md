# Problem 2: The Lift

[slide hideTitle]
# The Lift

[code-task title="The Lift" taskId="js-fundamentals-examPreparation-2-The-Lift" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function lift(input) {
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
# Description
Scrieți un program care să verifice dacă există **locuri goale pe un lift.**

Fiecare dintre cabinele ascensorului nu poate găzdui **mai mult de 4 persoane.**

Dacă o cabină este plină, ar trebui să îndreptați oamenii către următoarea, cu locuri disponibile.

## Intrare

* Pe prima linie, veți primi numărul de persoane care așteaptă la coadă pentru a urca pe lift

* Pe a doua linie, veți primi starea actuală a liftului - un șir de numere "(0-4)" fiecare număr reprezentând numărul de persoane din fiecare cabină următoare, separate printr-un spațiu gol

## Ieșire

Când rămâneți fără locuri libere sau dacă nu mai există oameni la coadă, ar trebui să imprimați unul dintre următoarele mesaje:

* Dacă nu mai există oameni la coadă, dar mai sunt câteva locuri pe lift:

"**There is room for more passengers!**"

Urmat de:
"\{**the state of each cabin, separated by ' '**\}"

* Dacă mai sunt oameni la coadă, dar nu mai sunt locuri disponibile:

"**The lift is full.** \{**people**\} **people currently in line.**"

Urmat de:
"\{**the state of each cabin, separated by ' '**\}"

* Dacă liftul este plin și nu mai sunt oameni care așteaptă să intre, ar trebui să imprimați starea fiecărei cabine separate printr-un singur spațiu

## Example One

|**Intrare**|**Ieșire** |
| --- | --- |
|lift([15, '0 0 0 0'])| There is room for more passengers! |
||4 4 4 3 |

## Cometariu

* Prima stare: 4 0 0 0 \-\> 11 persoane au plecat

* A doua stare: 4 4 0 0 \-\> 7 persoane au plecat

* A treia stare:  4 4 4 0 \-\> 3 persoane au plecat

## Example Two

|**Intrare**|**Ieșire** |
| --- | --- |
|lift([20, '0 2 0'])|The lift is full. 10 people currently in line.|
||4 4 4|

## Cometariu

* Prima stare: - 4 2 0  \-\> 16 persoane au plecat

* A doua stare: - 4 4 0  \-\> 14 persoane au plecat

* A treia stare: - 4 4 4 \-\> 10 oameni au plecat, dar nu mai există vagoane


[/task-description]
[code-io /]
[tests]
[test open]
[input]
lift([15, '0 0 0 0'])
[/input]
[output]
There is room for more passengers!
4 4 4 3
[/output]
[/test]
[test open]
[input]
lift([20, '0 2 0'])
[/input]
[output]
The lift is full. 10 people currently in line.
4 4 4
[/output]
[/test]
[test]
[input]
lift([10, '0 2 0 1 3 0 0 0'])
[/input]
[output]
There is room for more passengers!
4 4 4 1 3 0 0 0
[/output]
[/test]
[test]
[input]
lift([10, '4 4 4 4 4 4 4 4 1 4 4 4'])
[/input]
[output]
The lift is full. 7 people currently in line.
4 4 4 4 4 4 4 4 4 4 4 4
[/output]
[/test]
[test]
[input]
lift([20, '0 0 4'])
[/input]
[output]
The lift is full. 12 people currently in line.
4 4 4
[/output]
[/test]
[test]
[input]
lift([2, '0'])
[/input]
[output]
There is room for more passengers!
2
[/output]
[/test]
[test]
[input]
lift([14, '0 2 0 1 3'])
[/input]
[output]
4 4 4 4 4
[/output]
[/test]
[test]
[input]
lift([15, '0 0 0 0 0 0'])
[/input]
[output]
There is room for more passengers!
4 4 4 3 0 0
[/output]
[/test]
[test]
[input]
lift([20, '0 2 0'])
[/input]
[output]
The lift is full. 10 people currently in line.
4 4 4
[/output]
[/test]
[test]
[input]
lift([20, '0 0 4'])
[/input]
[output]
The lift is full. 12 people currently in line.
4 4 4
[/output]
[/test]
[test]
[input]
lift([18, '0 2 0 1 3 4'])
[/input]
[output]
The lift is full. 4 people currently in line.
4 4 4 4 4 4
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
