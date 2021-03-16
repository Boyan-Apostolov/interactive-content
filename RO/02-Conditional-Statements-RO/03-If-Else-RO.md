// sectionId: "Javascript::Programming-Basics::Conditional-Statements::If-Else"

[slide hideTitle]
# Condiții If-Else

[video src="https://videos.softuni.org/hls/javascript-basics/RO/02-Conditions/02-conditional-statements-js-17-if-else-conditions-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Construcția `if` poate conține, de asemenea, o clauză `else` pentru a da o acțiune specifică în cazul în care expresia booleană (care este setată la început `if(expresia bool)`) se schimbă in rezultat negativ(`false`).

Construită astfel, **instrucțiunea condițională** se numește `if-else` și comportamentul său este după cum urmează:

* Dacă rezultatul declarației este pozitiv (`true`) - efectuăm unele acțiuni

* Atunci când este negativ (`false`) - altele

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

După ce instrucțiunea 'then' sau instrucțiunea `else` rulează, controlul este transferat la următoarea instrucțiune după instrucțiunea `if`.

Într-o instrucțiune `if` care nu include o instrucțiune else, dacă condiția este `true`, instrucțiunea then rulează.

Dacă condiția este `false`, controlul este transferat la următoarea instrucțiune după instrucțiunea if.

Atât ce instrucțiunea "then" cât și instrucțiunea `else` pot consta dintr-o singură instrucțiune sau mai multe instrucțiuni care sunt încadrate între paranteze `{}`.

Pentru o singură instrucțiune, parantezele sunt opționale, dar recomandate.

Isntrucțiunea sau instrucțiunile din ce instrucțiunea "then" sau instrucțiunea `else` pot fi de orice fel, inclusiv o altă instrucțiune if imbircată  în interiorul instrucțiunii originale if.

## Exemplu: Vremea
Aceasta este o versiune extinsă a exemplului din diapozitivul anterior.

După cum puteți vedea acum, avem un alt caz, care va fi executat atunci când condiția din `if` se dovedește a fi **falsă.**

```js
function example(input) {
  if (weather == 'rainy') {
    console.log('Take an umbrella!');
  } else {
    console.log('Leave your umbrella at home!')
  }
}
```
[/slide]

[slide hideTitle]
# Block of Code

[video src="https://videos.softuni.org/hls/javascript-basics/RO/02-Conditions/02-conditional-statements-js-18-19-Blocks-of-code-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Când avem **o singură comandă** în corpul construcției **if**, putem **sări peste parantezele crețate**, indicând corpul operatorului condiționat.

Când vrem să executăm un  **bloc de cod** (un grup de comenzi), parantezele crețate sunt **necesare**.

În cazul în care le eliminăm, **numai prima linie** după **clauza if** va fi executată. 

Iată un exemplu în care **omiterea** parantezelor crețate duce la o **confuzie:**

```js live
let color = 'red';
if (color == 'red') 
  console.log('tomato');
else
  console.log('banana');
console.log('lemon'); 
```

Cu acolade:

```js live
let color = 'red';
if (color == 'red') {
  console.log('tomato');
  console.log('strawberry'); 
} else {
  console.log('banana');
  console.log('lemon');
}
```
[/slide]

[slide hideTitle]

# Problemă cu Soluție: Even or Odd

[video src="https://videos.softuni.org/hls/javascript-basics/RO/02-Conditions/02-conditional-statements-js-20-Problem-Solution-Even-or-Odd-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

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
Creați un program care verifică dacă un număr este **par sau impar**

* Dacă este par, tipăriți "**even**"
* Dacă este impar, tipăriți "**odd**"

# Exemplu
| **Intrare** | **Ieșire** |
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


