// sectionId: "Javascript::Programming-Basics::Conditional-Statements::If-Else"

[slide hideTitle]
# Condiții If-Else

[vimeo-video]
[stream language="EN" videoId="486879057/c8e3a2cdaa" default /]
[stream language="RO" videoId="486879057/c8e3a2cdaa"  /]
[/video-vimeo]

Construcția`if`poate conține,de asemenea,o clauză`else`pentru a da o acțiune specifică în cazul în care expresia booleană(care este setată la început`if(expresia bool)`)se schimba in rezultat negativ(`false`).

Construită astfel, **instrucțiunea condițională** se numește `if-else` și comportamentul său este după cum urmează:

* dacă rezultatul declarației este pozitiv (`true`)- efectuăm unele acțiuni

* atunci când este negativ (`false`) - altele.

[image assetsSrc="02-usecase-if-else-statement.png" /]

Formatul construcției este:
```js
if (condition) {
  // condition body;
} else {
  // else construction body;
}
```
Dacă condiția este `false`, se va executa instrucțiunea else.

Deoarece o condiție nu poate fi simultană `adevărată` și `falsă`, instrucțiunea then și instrucțiunea else a unei instrucțiuni `if-else` nu pot **niciodată să ruleze impreună**.

După ce instrucțiunea 'then'  sau instrucțiunea `else` rulează, controlul este transferat la următoarea instrucțiune după instrucțiunea `if`.

Într-o instrucțiune `if` care nu include o instrucțiune else, dacă condiția este `true`, instrucțiunea then rulează.

Dacă condiția este `false`, controlul este transferat la următoarea instrucțiune după instrucțiunea if.

Atât ce instrucțiunea 'then'  cât și instrucțiunea `else` pot consta dintr-o singură instrucțiune sau mai multe instrucțiuni care sunt încadrate între paranteze `{}`.

Pentru o singură instrucțiune, parantezele sunt opționale, dar recomandate.

Isntrucțiunea sau instrucțiunile din ce instrucțiunea 'then'  sau instrucțiunea `else` pot fi de orice fel, inclusiv o altă instrucțiune if imbircată  în interiorul instrucțiunii originale if

## Exemplu: Vremea
Aceasta este o versiune extinsă a exemplului din diapozitivul anterior.

După cum puteți vedea acum, avem un alt caz, care va fi executat atunci când condiția din `if` se dovedește a fi **false.**

```js
function example(input) {
  if (weather == "rainy") {
    console.log("Take an umbrella!");
  } else {
    console.log("Leave your umbrella at home!")
  }
}
```
[/slide]

[slide hideTitle]
# Block of Code

[vimeo-video]
[stream language="EN" videoId="486879069/fa69d41600" default /]
[stream language="RO" videoId="486879069/fa69d41600"  /]
[/video-vimeo]

Când avem **o singură comandă** în corpul construcției **if**, putem **sări peste parantezele buclate**, indicând corpul operatorului condiționat.

Când vrem să executăm un  **bloc de cod** (un grup de comenzi), parantezele cretate sunt **necesare**.

În cazul în care le eliminăm, **numai prima linie** după **clauza if** va fi executată. 

Iată un exemplu în care **omiterea** parantezelor cretate duce la o **confuzie:**

```js live
let color = "red";
if (color == "red") 
  console.log("tomato");
else
  console.log("banana");
console.log("lemon"); 
```

Cu acolade:

```js live
let color = "red";
if (color == "red") {
  console.log("tomato");
  console.log("strawberry"); 
} else {
  console.log("banana");
  console.log("lemon");
}
```
[/slide]

[slide hideTitle]

# Problemă cu soluția: Even or Odd
[code-task title="Even or Odd" taskId="pb-js-conditional-statements-Even-or-Odd" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function evenOrOdd(input) {
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
# Descriere
Creați un program, care verifică dacă un număr este **par sau impar**

* Dacă este par, tipăriți "**even**"
* Dacă este impar, tipăriți "**odd**"

# Exemplu
| **Input** | **Output** |
| --- | --- |
| evenOrOdd(4) | even |
| evenOrOdd(7) | odd |


[/task-description]
[tests]
[test open]
[input]
evenOrOdd(4)
[/input]
[output]
even
[/output]
[/test]
[test open]
[input]
evenOrOdd(7)
[/input]
[output]
odd
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
even
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]


