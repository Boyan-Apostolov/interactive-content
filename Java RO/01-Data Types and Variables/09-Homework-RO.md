# Teme de Casă

[slide hideTitle]
# Problem: Integer Operations

[code-task title="Integer Operations" taskId="java-fund-1-data-types-and-variables-Integer-Operations" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]
## Descriere
Citiți **patru numere întregi**.

**Adăugați** **primul** la **al doilea**, **împărțiți** (întreg) **suma** la **al treilea** număr și **înmulțiți** rezultatul cu **al patrulea** număr.

**Imprimați** rezultatul.

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 10 | 30 |
| 20 | |
| 3 | |
| 3 | |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
10
20
3
3
[/input]
[output]
30
[/output]
[/test]
[test]
[input]
15
14
2
3
[/input]
[output]
42
[/output]
[/test]
[test]
[input]
30
3
3
2
[/input]
[output]
22
[/output]
[/test]
[test]
[input]
40
10
5
2
[/input]
[output]
20
[/output]
[/test]
[test]
[input]
100
20
2
3
[/input]
[output]
180
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Sum Digits
[code-task title="Sum Digits" taskId="java-fund-1-data-types-and-variables-Sum-Digit" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]
## Descriere

Vi se va da un întreg **unic**.

Sarcina dvs. este de a găsi **suma cifrelor sale**.

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 245678 | 32 |

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 543 | 12 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
245678
[/input]
[output]
32
[/output]
[/test]
[test]
[input]
97561
[/input]
[output]
28
[/output]
[/test]
[test open]
[input]
543
[/input]
[output]
12
[/output]
[/test]
[test]
[input]
1000
[/input]
[output]
1
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Elevator

[code-task title="Elevator" taskId="java-fund-1-data-types-and-variables-Elevator" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Scrieți codul dvs. aici
    }
}

```
[/code-editor]
[task-description]
## Descriere

Calculați câte cursuri vor fi necesare pentru a **ridica n persoane** utilizând un lift cu **capacitate de p persoane**.

**Intrarea** conține **două linii**:

- Numărul de persoane **n**

- Capacitatea **p** a liftului

### Exemplu
|**Intrare**|**Ieșire**|**Comentarii**
| --- | --- | --- |
| 17 | 6 | 5 cursuri *3 persoane |
| 3 | | + 1 curs * 2 persoane |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
17
3
[/input]
[output]
6
[/output]
[/test]
[test]
[input]
4
5
[/input]
[output]
1
[/output]
[/test]
[test]
[input]
16
3
[/input]
[output]
6
[/output]
[/test]
[test]
[input]
16
4
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
2
5
[/input]
[output]
1
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Sum of Chars
[code-task title="Sum of Chars" taskId="java-fund-1-data-types-and-variables-Sum-of-Chars" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]
## Descriere

Scrieți un program, care **rezumă codurile ASCII de n caractere**.

**Imprimați suma** pe consolă.

### Intrare

- Pe prima linie, veți primi n - numărul de linii, care va urma

- Pe următoarele n linii - veți primi litere din alfabetul latin

### Ieșire
Imprimați suma totală în următorul format:
- "**The sum equals:** \{**TotalSum**\}"

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 5 | The sum equals: 399 |
| A | |
| b | |
| C | |
| d | |
| E | |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
A
b
C
d
E
[/input]
[output]
The sum equals: 399
[/output]
[/test]
[test]
[input]
12
S
o
f
t
U
n
i
R
u
l
z
z
[/input]
[output]
The sum equals: 1263
[/output]
[/test]
[test]
[input]
10
H
e
l
l
o
B
u
d
d
y
[/input]
[output]
The sum equals: 1004
[/output]
[/test]
[test]
[input]
20
a
a
a
a
a
a
a
a
a
a
a
a
a
a
a
a
a
a
a
a
[/input]
[output]
The sum equals: 1940
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Print Part of the ASCII Table
[code-task title="Print Part of the ASCII Table" taskId="java-fund-1-data-types-and-variables-Print-Part-of-the-ASCII-Table" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
      // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]

## Descriere
Găsiți online mai multe informații despre ASCII www.ascii-code.com (American Standard Code for Information Interchange) și scrieți un program care **tipărește o parte din tabelul ASCII**de caractere pe consolă.

Pe prima linie de intrare veți primi **indicele char** cu care ar trebui să **începeți** și pe a doua linie - indexul **ultimului** caracter pe care ar trebui să-l imprimați.

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 60 | < = > ? @ A |
| 65 | |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
60
65
[/input]
[output]
< = > ? @ A
[/output]
[/test]
[test]
[input]
69
79
[/input]
[output]
E F G H I J K L M N O
[/output]
[/test]
[test]
[input]
97
104
[/input]
[output]
a b c d e f g h
[/output]
[/test]
[test]
[input]
40
55
[/input]
[output]
( ) * + , - . / 0 1 2 3 4 5 6 7
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Triples of Latin Letters
[code-task title="Triples of Latin Letters" taskId="java-fund-1-data-types-and-variables-Triples-of-Latin-Letters" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
      // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]
## Descriere
Scrieți un program pentru a **citi** un număr întreg **n** și **tipări toate triplele primelor n litere latine mici**, ordonate **alfabetic**.

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 2 | aaa |
| | aab |
| | aba |
| | abb |
| | baa |
| | bab |
| | bba |
| | bbb |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
[/input]
[output]
aaa
aab
aba
abb
baa
bab
bba
bbb
[/output]
[/test]
[test]
[input]
3
[/input]
[output]
aaa
aab
aac
aba
abb
abc
aca
acb
acc
baa
bab
bac
bba
bbb
bbc
bca
bcb
bcc
caa
cab
cac
cba
cbb
cbc
cca
ccb
ccc
[/output]
[/test]
[test]
[input]
4
[/input]
[output]
aaa
aab
aac
aad
aba
abb
abc
abd
aca
acb
acc
acd
ada
adb
adc
add
baa
bab
bac
bad
bba
bbb
bbc
bbd
bca
bcb
bcc
bcd
bda
bdb
bdc
bdd
caa
cab
cac
cad
cba
cbb
cbc
cbd
cca
ccb
ccc
ccd
cda
cdb
cdc
cdd
daa
dab
dac
dad
dba
dbb
dbc
dbd
dca
dcb
dcc
dcd
dda
ddb
ddc
ddd
[/output]
[/test]
[test]
[input]
1
[/input]
[output]
aaa
[/output]
[/test]
[test]
[input]
6
[/input]
[output]
aaa
aab
aac
aad
aae
aaf
aba
abb
abc
abd
abe
abf
aca
acb
acc
acd
ace
acf
ada
adb
adc
add
ade
adf
aea
aeb
aec
aed
aee
aef
afa
afb
afc
afd
afe
aff
baa
bab
bac
bad
bae
baf
bba
bbb
bbc
bbd
bbe
bbf
bca
bcb
bcc
bcd
bce
bcf
bda
bdb
bdc
bdd
bde
bdf
bea
beb
bec
bed
bee
bef
bfa
bfb
bfc
bfd
bfe
bff
caa
cab
cac
cad
cae
caf
cba
cbb
cbc
cbd
cbe
cbf
cca
ccb
ccc
ccd
cce
ccf
cda
cdb
cdc
cdd
cde
cdf
cea
ceb
cec
ced
cee
cef
cfa
cfb
cfc
cfd
cfe
cff
daa
dab
dac
dad
dae
daf
dba
dbb
dbc
dbd
dbe
dbf
dca
dcb
dcc
dcd
dce
dcf
dda
ddb
ddc
ddd
dde
ddf
dea
deb
dec
ded
dee
def
dfa
dfb
dfc
dfd
dfe
dff
eaa
eab
eac
ead
eae
eaf
eba
ebb
ebc
ebd
ebe
ebf
eca
ecb
ecc
ecd
ece
ecf
eda
edb
edc
edd
ede
edf
eea
eeb
eec
eed
eee
eef
efa
efb
efc
efd
efe
eff
faa
fab
fac
fad
fae
faf
fba
fbb
fbc
fbd
fbe
fbf
fca
fcb
fcc
fcd
fce
fcf
fda
fdb
fdc
fdd
fde
fdf
fea
feb
fec
fed
fee
fef
ffa
ffb
ffc
ffd
ffe
fff
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Water Overflow

[code-task title="Water Overflow" taskId="java-fund-1-data-types-and-variables-Water-Overflow" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
      // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]
## Descriere
Aveți un **rezervor de apă** cu o capacitate de 255 litri.

Pe prima**linie, veți primi n.

În următoarele **n linii**, veți primi **litri** de apă, pe care trebuie să **le turnați în rezervor**.

Dacă **capacitatea nu este suficientă**, tipăriți "**Insufficient capacity!**" și **continuați să citiți** următorul rând.

Pe ultima linie, **imprimați litrii** în rezervor.

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 5 | Insufficient capacity! |
| 20 | 240 |
| 100 | |
| 100 | |
| 100 | |
| 20 | |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
20
100
100
100
20
[/input]
[output]
Insufficient capacity!
240
[/output]
[/test]
[test]
[input]
1
1000
[/input]
[output]
Insufficient capacity!
0
[/output]
[/test]
[test]
[input]
7
10
20
30
10
5
10
20
[/input]
[output]
105
[/output]
[/test]
[test]
[input]
10
3
10
12
50
30
40
10
20
60
20
[/input]
[output]
255
[/output]
[/test]
[test]
[input]
4
100
150
5
1
[/input]
[output]
Insufficient capacity!
255
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Beer Kegs

[code-task title="Beer Kegs" taskId="java-fund-1-data-types-and-variables-Beer-Kegs" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
      // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]

## Descriere
Scrieți un program care **calculează volumul** de **n** butoaie de bere.

**Veți primi** în total **3 * n linii**.

Fiecare **trei rânduri** va conține informații pentru un **butoi unic**.

**În primul rând** sus este **modelul** al butoiului, **după aceea** este **raza** (un număr în virgulă mobilă) al butoiului și **în sfârșit** este **înălțimea** a butoiului.

Calculați **volumul** folosind următoarea formulă:

`π * r^2 * h` 

La final, **tipăriți modelul celui mai mare butoi**.

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 2 | Bigger Keg |
| Smaller Keg | |
| 2.41 | |
| 10 | |
| Bigger Keg | |
| 5.12 | |
| 20 | |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
Smaller Keg
2.41
10
Bigger Keg
5.12
20
[/input]
[output]
Bigger Keg
[/output]
[/test]
[test]
[input]
3
Keg 1
10
10
Keg 2
20
20
Keg 3
10
30
[/input]
[output]
Keg 2
[/output]
[/test]
[test]
[input]
3
Keg 1
15
15
Keg 2
20
10
Keg 3
10
20
[/input]
[output]
Keg 2
[/output]
[/test]
[test]
[input]
5
Keg 1
10
10
Keg 2
20
20
Keg 3
10
30
Keg 4
213213.123
1234124124
Keg 5
1236.345534
21321124
[/input]
[output]
Keg 4
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Spice Must Flow
[code-task title="Spice Must Flow" taskId="java-fund-1-data-types-and-variables-Spice-Must-Flow" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
      // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]

## Descriere
Scrieți un program care **calculează cantitatea totală de condimente** care poate fi extrasă dintr-o sursă.

Sursa are un randament **de pornire**, care indică cât de mult condiment poate fi extras în **prima zi**.

După ce a fost exploatat pentru o zi, randamentul scade cu 10, ceea ce înseamnă că în a doua zi va produce 10 condimente mai puțin **decât în ​​prima, în a treia zi cu 10 mai puțin decât în ​​a doua**, și **și așa mai departe**(vezi exemple).

O sursă este considerată **profitabilă numai în timp ce randamentul acesteia este de cel puțin 100** - când se așteaptă mai puțin de 100 de condimente într-o zi, abandonați sursa.

Echipajul **de minerit consumă 26 de condimente în fiecare zi** la **sfârșitul schimbului și încă 26** după epuizarea minei. Rețineți că muncitorii nu pot consuma mai mult condiment decât există în depozit.

Când operațiunea este finalizată, **tipăriți pe consolă pe două linii separate** câte **zile** a funcționat mina și **cantitatea totală** de condiment extras.


### Intrare
Veți primi **un număr**, reprezentând randamentul **inițial** al sursei.

### Ieșire
Imprimați **două rânduri separate** câte **zile a funcționat mina** și **cantitatea totală de condimente extrase**.

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 111 | 2 |
| | 134 |

**Comentarii**

- In prima zi extragem 111de condimente și la sfârșitul turei, muncitorii consumă 26, lăsând 85. 

Randamentul scade cu 10 până la 101

- In a-2-a zi extragem 101de condimente, muncitorii consumă 26, lăsând 75. 

Totalul este 160 și randamentul a scăzut la 91

- Deoarece randamentul așteptat este mai mic de 100, abandonăm sursa. 

Muncitorii iau încă 26, lăsând 134. Mina a funcționat 2 zile

[/task-description]
[code-io /]
[tests]
[test open]
[input]
111
[/input]
[output]
2
134
[/output]
[/test]
[test]
[input]
450
[/input]
[output] 
36
8938
[/output]
[/test]
[test]
[input]
200
[/input]
[output]
11
1338
[/output]
[/test]
[test]
[input]
1234
[/input]
[output] 
114
73276
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Poke Mon
[code-task title="Poke Mon" taskId="java-fund-1-data-types-and-variables-Poke-Mon" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
      // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]

## Descriere
A Poke Mon este un tip special de pokemon căruia îi place să-i împingă pe alții. 

Dar la sfârșitul zilei, Poke Mon vrea să păstreze **statistici**, despre câte poke a reușit să facă.

Poke Mon își aruncă ținta și apoi trece la o altă țintă. 

**Distanța dintre ținte își reduce puterea de lovitură**.

Vi se va oferi **puterea de poke** pe care Poke Mon o are, **N** - un număr întreg.

Apoi vi se va acorda **distanța dintre țintele poke**, **M** - un număr întreg.

Apoi vi se va da **exhaustorFactor Y** - un număr întreg.

Sarcina ta este să începi **scăzând M din N până când N devine mai mic decât M**, adică Poke Mon nu are suficientă putere pentru a atinge următoarea țintă.

**De fiecare dată când scazi M de la N înseamnă că ai atins o țintă** și ai tras-o cu succes. 

CONTAȚI câte ținte ați introdus - veți avea nevoie de acest număr.

Poke Mon devine treptat **mai epuizat**. 

**Dacă N devine egal cu EXACT 50% din valoarea inițială, trebuie să împărțiți N la Y**, dacă este POSIBIL. 

Această DIVIZIUNE este între numere întregi.

Dacă o divizare nu este posibilă, NU ar trebui să o faceți. În schimb, ar trebui să continuați scăderea.

După împărțire, ar trebui să **continuați scăderea** din N, până când devine mai mic decât M.

Când N devine mai mic decât M, trebuie să luați ceea ce a rămas din N și numărul de ținte pe care le-ați atins și să le imprimați ca rezultat.

NOTĂ: Când calculați procentele, ar trebui să fiți PRECIS la maximum.

Exemplu: 505 NU este EXACT 50% din 1000, 50.5%.

### Intrare / Constrângeri

- Pe prima linie veți primi **N** - un număr întreg

- Pe a doua linie veți primi **M** - un număr întreg

- Pe a treia linie veți primi **Y** - un număr întreg

### Ieșire

- Pe prima linie tipăriți **ceea ce a rămas din N**, după ce a scăzut din acesta

- Pe cea de-a doua linie tipăriți **numărul de ținte**, ați reușit să pătrundeți

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 5 | 1 |
| 2 | 2 |
| 3 | |

**Comentarii**
- N = 5, M = 2, Y = 3
- Începem să scădem M de la N
- N - M = 3. 1 țintă aruncată
- N - M = 1. 2 ținte aruncate
- N < M
- Tipărim ceea ce a rămas din N, care este 1
- Printăm numărul de ținte, care este 2

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
2
3
[/input]
[output]
1
2
[/output]
[/test]
[test]
[input]
10
5
2
[/input]
[output]
2
1
[/output]
[/test]
[test]
[input]
1000
45
2
[/input]
[output]
10
22
[/output]
[/test]
[test]
[input]
100
19
1
[/input]
[output]
5
5
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Snowballs

[code-task title="Snowballs" taskId="java-fund-1-data-types-and-variables-Snowballs" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
      // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]

## Descriere
Tony și Andi adoră să se joace în zăpadă și să se lupte cu bulgări de zăpadă, dar se ceartă întotdeauna care este cel mai bun bulgăre de zăpadă.

Au decis să vă implice în lupta lor, făcându-vă să scrieți un program care **să calculeze datele bulgărului** și să redea cea mai bună valoare a bulgărului.

Veți primi **N** - un număr întreg, **numărul de bulgări de zăpadă fiind făcut** de Tony și Andi.

Pentru fiecare bulgăre de zăpadă veți primi 3 linii de intrare:

- Pe prima linie veți obține **snowballSnow** - un număr întreg

- Pe a doua linie veți obține **snowballTime** - un număr întreg

- Pe a treia linie veți obține **snowballQuality** - un număr întreg

Pentru fiecare bulgăre de zăpadă trebuie să calculați Valoarea acesteia cu următoarea formulă:

**(snowballSnow / snowballTime) ^ snowballQuality**

La sfârșit, trebuie să **imprimați** cea mai mare valoare calculată cu zăpadă.

### Intrare / Constrângeri

- Pe prima linie de intrare veți primi N - numărul de bulgări de zăpadă

- Pe următoarele linii de intrare N * 3 veți primi date despre bulgări de zăpadă

### Ieșire

- Ca ieșire, trebuie să imprimați **cea mai mare valoare calculată a zăpezii**, după formula specificată mai sus

- Formatul de ieșire este:

"\{**snowballSnow**\} : \{**snowballTime**\} = \{**snowballValue**\} (\{**snowballQuality**\})"

### Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 2 | 10 : 2 = 125 (3) |
| 10 | |
| 2 | |
| 3 | |
| 5 | |
| 5 | |
| 5 | |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
10
2
3
5
5
5
[/input]
[output]
10 : 2 = 125 (3)
[/output]
[/test]
[test]
[input]
3
10
5
7
16
4
2
20
2
2
[/input]
[output]
10 : 5 = 128 (7)
[/output]
[/test]
[test]
[input]
2
50
10
4
5
5
10
[/input]
[output]
50 : 10 = 625 (4)
[/output]
[/test]
[test]
[input]
2
5
5
5
15
3
5
[/input]
[output]
15 : 3 = 3125 (5)
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

