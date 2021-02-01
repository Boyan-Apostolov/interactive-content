[slide hideTitle]
# Bucla For cu un pas

[vimeo-video]
[stream language="EN" videoId="487119404/67365f350f" default /]
[stream language="RO" videoId="487119404/67365f350f"  /]
[/video-vimeo]

În această secține vom oferi mai multe detalii cu privre la o  parte specială și foarte importantă a buclei `for`, **și anume pasul.**

**Pasul** este acea **parte** a construcției buclei care indică cum să fie incrementată sau decrementată valoarea variabilei principale. 

Aceasta este declarată ultimă în corpul buclei for.

Foarte des, pasul are dimensiunea 1 și în acest caz, în loc sî scriem `i += 1` sau `i -= 1`, putem folosi operatorii `i++` sau `i--`.

```js live
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

Dacă dorim ca pasul nostru să fie **diferit de 1**, atunci când **incrementăm**, folosim `i +=` + operaorul pentru dimensiunea pasului.

Cu un pas de 2, bucla ar arăta astfel:

```js live
for (let i = 0; i < 10; i += 2) {
  console.log(i);
}
```

S-ar putea să dorim să avem un **pas descrescător** - `i - =` + dimensiunea pasului.

În acest caz, ar trebui să fim atenți la condiția finală pentru a evita **o** buclă infinită.

```js live
for (let i = 10; i >= 1; i--) {
  console.log(i);
}
```

[/slide]


[slide hideTitle]
# Problem: Number Ending with 7

[vimeo-video]
[stream language="EN" videoId="487119426/15f9ad851f" default /]
[stream language="RO" videoId="487119426/15f9ad851f"  /]
[/video-vimeo]


[code-task title="Number Ending with 7" taskId="pb-js-for-loop-lab-Number-Ending-with-7" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function numbersEndingWith7(n) {
  // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Description
Scrieți un program care:

* Citește un număr **n**
* Imprimă toate numerele de la  **7 până la n**, **care se termină cu 7**

# Example
| **Input** | **Output** |
| --- | --- |
|30| 7 |
||17 |
||27 |

[/task-description]
[tests]
[test]
[input]
40
[/input]
[output]
7
17
27
37
[/output]
[/test]
[test]
[input]
35
[/input]
[output]
7
17
27
[/output]
[/test]
[test]
[input]
80
[/input]
[output]
7
17
27
37
47
57
67
77
[/output]
[/test]
[test]
[input]
130
[/input]
[output]
7
17
27
37
47
57
67
77
87
97
107
117
127
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Solution: Number Ending with 7

[vimeo-video]
[stream language="EN" videoId="487119464/39daf17177" default /]
[stream language="RO" videoId="487119464/39daf17177"  /]
[/video-vimeo]

[code-task title="Number Ending with 7" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function numbersEndingWith7(n) {
  // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Description
Scrieți un program care:

* Citește un număr **n**
* Imprimă toate numerele de la  **7 până la n**, **care se termină cu 7**

# Example
|**Input** | **Output** |
| --- | --- |
|30| 7 |
||17 |
||27 |

[/task-description]
[tests]
[test]
[input]
40
[/input]
[output]
7
17
27
37
[/output]
[/test]
[test]
[input]
35
[/input]
[output]
7
17
27
[/output]
[/test]
[test]
[input]
80
[/input]
[output]
7
17
27
37
47
57
67
77
[/output]
[/test]
[test]
[input]
130
[/input]
[output]
7
17
27
37
47
57
67
77
87
97
107
117
127
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Exam Countdown

[vimeo-video]
[stream language="EN" videoId="487119503/367fcdcc3d" default /]
[stream language="RO" videoId="487119503/367fcdcc3d"  /]
[/video-vimeo]

[code-task title="Exam Countdown" taskId="pb-js-for-loop-lab-Exam-Countdown" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function examCountdown(days) {
   // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Description
Scrieți un program care:

* Citește un număr întreg - numărul de **zile înainte de examen**
* După fiecare zi trecută, imprimă: `{numberOfDaysLeft} days before the exam`
* La final imprimă: `The exam has come.`

# Example
| **Input** | **Output** |
| --- | --- |
|3| 3 days before the exam |
||2 days before the exam |
||1 days before the exam |
||The exam has come. |

[/task-description]
[tests]
[test]
[input]
4
[/input]
[output]
4 days before the exam
3 days before the exam
2 days before the exam
1 days before the exam
The exam has come.
[/output]
[/test]
[test]
[input]
5
[/input]
[output]
5 days before the exam
4 days before the exam
3 days before the exam
2 days before the exam
1 days before the exam
The exam has come.
[/output]
[/test]
[test]
[input]
6
[/input]
[output]
6 days before the exam
5 days before the exam
4 days before the exam
3 days before the exam
2 days before the exam
1 days before the exam
The exam has come.
[/output]
[/test]
[test]
[input]
7
[/input]
[output]
7 days before the exam
6 days before the exam
5 days before the exam
4 days before the exam
3 days before the exam
2 days before the exam
1 days before the exam
The exam has come.
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Solution: Exam Countdown

[vimeo-video]
[stream language="EN" videoId="487119549/e38e542417" default /]
[stream language="RO" videoId="487119549/e38e542417"  /]
[/video-vimeo]

[code-task title="Exam Countdown" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function examCountdown(days) {
   // Scrieți codul dvs. aici
}
```
[/code-editor]
[task-description]
# Description
* Citește un număr întreg - numărul de **zile înainte de examen**
* După fiecare zi trecută, imprimă: `{numberOfDaysLeft} days before the exam`
* La final imprimă: `The exam has come.`

# Example
| **Input** | **Output** |
| --- | --- |
|3| 3 days before the exam |
||2 days before the exam |
||1 days before the exam |
||The exam has come. |

[/task-description]
[tests]
[test]
[input]
4
[/input]
[output]
4 days before the exam
3 days before the exam
2 days before the exam
1 days before the exam
The exam has come.
[/output]
[/test]
[test]
[input]
5
[/input]
[output]
5 days before the exam
4 days before the exam
3 days before the exam
2 days before the exam
1 days before the exam
The exam has come.
[/output]
[/test]
[test]
[input]
6
[/input]
[output]
6 days before the exam
5 days before the exam
4 days before the exam
3 days before the exam
2 days before the exam
1 days before the exam
The exam has come.
[/output]
[/test]
[test]
[input]
7
[/input]
[output]
7 days before the exam
6 days before the exam
5 days before the exam
4 days before the exam
3 days before the exam
2 days before the exam
1 days before the exam
The exam has come.
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]
