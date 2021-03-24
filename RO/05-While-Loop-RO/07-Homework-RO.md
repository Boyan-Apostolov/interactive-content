# Teme Pentru Acasă

[slide hideTitle]
# Problemă cu Soluție: Sum Digits

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/05-while-loops/RO/Java-While-Loops-Problem-and-Solution-Sum-Digits-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Sum Digits" taskId="pb-java-while-loop-sum-digits" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Scrieți un program care:

* Citește un număr de pe  consolă
* **Adună** toate **cifrele** unui număr
* Imprimă suma

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 5634 | 18 |

[/task-description]
[tests]
[test open]
[input]
5634
[/input]
[output]
18
[/output]
[/test]
[test]
[input]
123456
[/input]
[output]
21
[/output]
[/test]
[test]
[input]
489451
[/input]
[output]
31
[/output]
[/test]
[test]
[input]
8498498
[/input]
[output]
50
[/output]
[/test]
[test]
[input]
000000
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
5684915
[/input]
[output]
38
[/output]
[/test]
[test]
[input]
8
[/input]
[output]
8
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă: Favorite Book
[code-task title="Favorite Book" taskId="pb-java-while-loop-favourite-book" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Scrieți un program care: 

* Citește **numele unei cărți** de pe consolă
* Primește nume până ce ajunge la **cartea cu același nume ca prima**
* Imprimă "**Book found! Attempts:** \{**attemptsCount**\}" și după aceea se  oprește

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| Alice in Wonderland | Book found! Attempts: 3 |
| Winnie the Pooh | |
| Peter Pan | |
| Alice in Wonderland | |
[/task-description]
[tests]
[test open]
[input]
Alice in Wonderland
Winnie the Pooh
Peter Pan
Alice in Wonderland
[/input]
[output]
Book found! Attempts: 3
[/output]
[/test]
[test]
[input]
Fav Book
Book1
Book2
Book3
Book4
Book5
Book6
Book7
Book8
Book9
Book10
Book11
Fav Book
[/input]
[output]
Book found! Attempts: 12
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă cu Soluție: Find Min and Max

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/05-while-loops/RO/Java-While-Loops-Problem-and-Solution-Find-Min-and-Max-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Find Min and Max" taskId="pb-java-while-loop-find-min-and-max" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Descirere
Scrieți un program care: 

* Primește numere întregi până la mesajul **"END"**
* Imprimă **cel mai mare** și **cel mai mic** număr întreg în următorul format:
   * "**Max number:** \{**max number**\}"
   * "**Min number:** \{**min number**\}"

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 10 | Max number: 304 |
| 20 | Min number: 0 |
| 304 |  |
| 0 |  |
| 50 |  |
| END |  |

[/task-description]
[tests]
[test open]
[input]
10
20
304
0
50
END
[/input]
[output]
Max number: 304
Min number: 0
[/output]
[/test]
[test]
[input]
5
10
66
456
-4
1
0
END
[/input]
[output]
Max number: 456
Min number: -4
[/output]
[/test]
[test]
[input]
3
15
56
32
7
9
END
[/input]
[output]
Max number: 56
Min number: 3
[/output]
[/test]
[test]
[input]
-34
-4
-12
-45
END
[/input]
[output]
Max number: -4
Min number: -45
[/output]
[/test]
[test]
[input]
0
1
4
5
END
[/input]
[output]
Max number: 5
Min number: 0
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă: Special Number
[code-task title="Special Number" taskId="pb-java-while-loop-special-number" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Desciere
Numărul special este un număr **divizibil cu toate cifrele sale** fără rest. 

Scrieți un program care: 
* Primește un număr întreg
* **Prints** "\{**num**\} **is special**", dacă numărul este special
* În celelalte situații, imprimă "\{**num**\} **is not special**"

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 23 | 23 is not special |
| 404 | 404 is special |

[/task-description]
[tests]
[test open]
[input]
23
[/input]
[output]
23 is not special
[/output]
[/test]
[test open]
[input]
404
[/input]
[output]
404 is special
[/output]
[/test]
[test]
[input]
55
[/input]
[output]
55 is special
[/output]
[/test]
[test]
[input]
43
[/input]
[output]
43 is not special
[/output]
[/test]
[test]
[input]
202
[/input]
[output]
202 is special
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă cu Soluție: Special Bonus

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/05-while-loops/RO/Java-While-Loops-Problem-and-Solution-Special-Bonus-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Special Bonus" taskId="pb-java-while-loop-special-bonus" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Desciere
Scrieți un program care: 

* Citește un număr **întreg** de pe consolă
* Continuă să citescă numerele întregi până ce ajunge la **același număr ca primul**
* Când îl găsește, crește valoarea **numărului** anterior **dinaintea lui** cu 100% și îl imprimă

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 25 | 60 |
| 20 | |
| 30 | |
| 25 | |
[/task-description]
[tests]
[test open]
[input]
25
20
30
25
[/input]
[output]
60
[/output]
[/test]
[test]
[input]
20
5
5
20
[/input]
[output]
10
[/output]
[/test]
[test]
[input]
20
20
[/input]
[output]
40
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă: Sequence 2k + 1
[code-task title="Sequence 2k + 1" taskId="pb-java-while-loop-sequence-2k-1" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Scrieți un program care: 

* Citește un număr **n** de pe consolă
* Imprimă o **secvență** de numere care sunt **<= n** și îndeplinesc următoarea condiție:
* Fiecare dintre numere este egal cu numărul aflat imediat înaintea sa, multiplicat cu **2**, plus **1**

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 8 | 1 |
|  | 3 |
|  | 7 |
[/task-description]
[tests]
[test open]
[input]
8
[/input]
[output]
1
3
7
[/output]
[/test]
[test]
[input]
1
[/input]
[output]
1
[/output]
[/test]
[test]
[input]
7
[/input]
[output]
1
3
7
[/output]
[/test]
[test]
[input]
100
[/input]
[output]
1
3
7
15
31
63
[/output]
[/test]
[test]
[input]
511
[/input]
[output]
1
3
7
15
31
63
127
255
511
[/output]
[/test]
[test]
[input]
10000
[/input]
[output]
1
3
7
15
31
63
127
255
511
1023
2047
4095
8191
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Problemă: Account Balance
[code-task title="Account Balance" taskId="pb-java-while-loop-account-balance" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Scrieți un program care: 

* Primește **o sumă de bani** pentru fiecare tranzacție până la **"END"**

* **Adaugă** banii în  **sold** și **tipărește: "**Increase:**\{**money**\}", formatați `banii` la **a două cifră** după punctul zecimal 
* După **"END"** calculează și **imprimă** suma totală din cont: "**Total:** \{**balance**\}", formatați `balance` până la **a doua cifră** după punctul zecimal



## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 5.51 | Increase: 5.51 |
| 69.42 | Increase: 69.42 |
| 100 | Increase: 100.00 |
| END | Total: 174.93 |
[/task-description]
[tests]
[test open]
[input]
5.51
69.42
100
END
[/input]
[output]
Increase: 5.51
Increase: 69.42
Increase: 100.00
Total: Total: 174.93
[/output]
[/test]
[test]
[input]
5.50
60.23
100
END
[/input]
[output]
Increase: 5.50
Increase: 60.23
Increase: 100.00
Total: ‭165.73‬
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]
[/slide]

[slide hideTitle]
# Problemă: Old Books
[code-task title="Old Books" taskId="pb-java-while-loop-old-books" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Andreea merge acasă după ce a fost plecată mult timp în afara țării. 

Când ajunge acasă, ea vede biblioteca bunicii și își amintește de cartea sa preferată.

Ajutați-o pe Andreea scriind un program în care Andreea să introducă titlul unei **cărți** pe care o caută  (**un șir**) și **capacitatea** bibliotecii(**un număr întreg**). 

**Până ce** Andreea găsește cartea sa preferată **sau** nu verifică toate cărțile din bibliotecă, programul trebuie să citească de fiecare dată titlul următoarei cărți pe o linie separată.

## Intrare
- Prima linie de intrare este titlul cărții pe care o caută Andreea - un șir
- A doua linie este capacitatea bibliotecii - un număr întreg
- Pe fiecare dintre liniile următoare - titlul unei cărți din bibliotecă - un șir

## Ieșire
- Dacă Andreea **nu** găsește cartea, imprimă **două** linii:
  - "**The book you search is not here!**"
  - "**You checked** \{**count**\} **books.**"
- Dacă Andreea **găsește** cartea, imprimă o **singură** linie:
    - "**You checked** \{**count**\} **books and found it.**"

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| Troy | You checked 2 books and found it. |
| 8 | |
| Stronger | |
| Life Style | |
| Troy | |

[hints]
[hint]
Andreea caută o carte cu titlul "Troy", iar capacitatea bibliotecii este de 8 cărți.
[/hint]
[hint]
Prima carte este "Stronger", a doua carte este "Life Style", a treia este cea căutată - "Troy" și programul se încheie.
[/hint]
[/hints]

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| The Spot | The book you search is not here! |
| 4 | You checked 4 books. |
| Hunger Games | |
| Harry Potter | |
| Torronto | | 
| Spotify | | 

[hints]
[hint]
Andreea caută o carte cu titlul "The Spot". Biblioteca conține 4 cărți.
Prima carte este "Hunger Games", a doua - "Harry Potter", a treia - "Torronto", a patra - "Spotify".
[/hint]
[hint]
Cum nu mai sunt alte cărți în bibliotecă, citirea titlurilor se încheie. Andreea nu a găsit cartea.
[/hint]
[/hints]
[/task-description]
[tests]
[test open]
[input]
Troy
8
Stronger
Life Style
Troy
[/input]
[output]
You checked 2 books and found it.
[/output]
[/test]
[test open]
[input]
The Spot
4
Hunger Games
Harry Potter
Torronto
Spotify
[/input]
[output]
The book you search is not here!
You checked 4 books.
[/output]
[/test]
[test]
[input]
Bourne
32
True Story
Forever
More Space
The Girl
Spaceship
Strongest
Profit
Tripple
Stella
The Matrix
Bourne
[/input]
[output]
You checked 10 books and found it.
[/output]
[/test]
[test]
[input]
Horror
22
Storm
Worms
Bronks
Paradise
Serdika
Stronger
Steroid
Proud
epic
Pepper
Purple Rain
Sephia
Philip The Killer
Saturday Night
Terror
Poor Man
Medom
medusa
saturn
story teller
Spotify
santas Life
[/input]
[output]
The book you search is not here!
You checked 22 books.
[/output]
[/test]
[test]
[input]
Sports
7
Stars
String It
Glamour
Paris 
Life Spell
Poppay
Proud of ME
[/input]
[output]
The book you search is not here!
You checked 7 books.
[/output]
[/test]
[test]
[input]
Programming Basics
4
Four
Triple W
Sarrah
Programming Basics
[/input]
[output]
You checked 3 books and found it.
[/output]
[/test]
[test]
[input]
La Liga
1
Troy
[/input]
[output]
The book you search is not here!
You checked 1 books.
[/output]
[/test]
[test]
[input]
The Post
5
Porto
Troy
Stormy
Udemy
The Post
[/input]
[output]
You checked 4 books and found it.
[/output]
[/test]
[test]
[input]
Most Wanted
9
Post Fight
stormy Wife
Windows..
Saturn
Karate Kid
Don't Think about me
Most Dangerous
Prepare for fight
Fair
The book you search is not here!
[/input]
[output]
The book you search is not here!
You checked 9 books.
[/output]
[/test]
[test]
[input]
Paramedick
11
Pop
Rock
Metallica
Mamma Mia
Morandy
Solo
Ordinary Life
Portable
Paramedick
[/input]
[output]
You checked 8 books and found it.
[/output]
[/test]
[test]
[input]
Possesion
1
Possesion
[/input]
[output]
You checked 0 books and found it.
[/output]
[/test]
[test]
[input]
Keep Trying
1
sout
[/input]
[output]
The book you search is not here!
You checked 1 books.
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]

[slide hideTitle]
# Problemă: Exam Preparation
[code-task title="Exam Preparation" taskId="pb-java-while-loop-exam-preparation" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Scrieți un program prin care Martin rezolvă probleme pentru examen până când primește din partea profesorului său mesajul: "**Enough**". 

De fiecare dată când rezolvă o problemă, primește o notă. **Programul trebuie să se oprească când** Martin primește comanda "Enough" sau **primește un număr de note slabe**. 

O notă slabă este mai mică sau egală cu 4.00.

## Intrare
- Pe prima linie – **număr de note proaste** – un număr întreg în intervalul \[1…5\]
- **După aceea în mod repetat două linii**:
  - **numele problemei - text**
  - **notă** - un număr întreg în intervalul\[2…6\]

## Ieșire
- Dacă Martin ajunge la comanda **Enough**", imprimă **3** linii:
  - "**Average score:** \{**average grade**\}"
  - "**Number of problems:** \{**number of ALL problems**\}"
  - "**Last problem:** \{**last problem\'s name**\}"
- **Dacă obține numărul specificat de note slabe**:
   - "**You need a break**, \{**number poor grades**\} **poor grades.**"

**Nota medie trebuie să fie formatată la a doua zecimală.**

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 3 | Average score: 5.25 |
| Money | Number of problems: 4 |
| 6 | Last problem: Bus |
| Story | |
| 4 | |
| Spring Time | |
| 5 | |
| Bus | |
| 6 | |
| Enough | |

[hints]
[hint]
Numărul de note slabe este 3.
[/hint]
[hint]
Numele primei probleme este Money, nota lui Martin este 6.
A doua problemă - Story, nota - 4.
A treia problemă - Spring Time, nota - 5.
A patra problemă - Bus, nota - 6.
Următoarea comandă este Enough, programul se încheie.
[/hint]
[hint]
Media notelor: 21 / 4 = 5.25
Numărul problemelor rezolvate: 4
Ultima problemă: Bus
[/hint]
[/hints]

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 2| You need a break, 2 poor grades. |
| Income| |
| 3| |
| Game Info| |
| 6| |
| Best Player| |
| 4| |

[hints]
[hint]
Numărul permis de note mici este 2.
[/hint]
[hint]
Numele primei probleme este Income, nota lui Martin este 3.
A doua problemă - Game Info, nota - 6.
A treia problemă - Best Player, nota - 4.
Martin atinge numărul de note mici permise, este timpul pentru o pauză.
[/hint]
[/hints]
[/task-description]
[tests]
[test open]
[input]
3
Money
6
Story
4
Spring Time
5
Bus
6
Enough
[/input]
[output]
Average score: 5.25
Number of problems: 4
Last problem: Bus
[/output]
[/test]
[test open]
[input]
2
Income
3
Game Info
6
Best Player
4
[/input]
[output]
You need a break, 2 poor grades.
[/output]
[/test]
[test]
[input]
4
Stone Age
5
Freedom
5
Storage
3
Enough
[/input]
[output]
Average score: 4.33
Number of problems: 3
Last problem: Storage
[/output]
[/test]
[test]
[input]
1
Estonia
6
Friday
6
Spaceship
5
Moving
6
Cake
4
[/input]
[output]
You need a break, 1 poor grades.
[/output]
[/test]
[test]
[input]
2
Personality
6
Stable versin
4
Stereotipe
6
Forerunner
6
IronMan
6
Enough
[/input]
[output]
Average score: 5.60
Number of problems: 5
Last problem: IronMan
[/output]
[/test]
[test]
[input]
2
Toronto
6
Graduation Pt3
3
Lilli
6
Graduation Pt2
6
Old Library
4
[/input]
[output]
You need a break, 2 poor grades.
[/output]
[/test]
[test]
[input]
3
ExamPrep
6
oldBooks
5
ForestGump
6
IronMan
6
Sephia
6
From 1 to 100
6
Substitute
6
Footbal Kit
5
Best Player
6
Game Statistics
6
Enough
[/input]
[output]
Average score: 5.80
Number of problems: 10
Last problem: Game Statistics
[/output]
[/test]
[test]
[input]
3
Iron Man
3
Substitute
6
Cat Walk
4
Cat Watch
3
[/input]
[output]
You need a break, 3 poor grades.
[/output]
[/test]
[test]
[input]
4
Stadium Income
6
New House
6
Old Books
6
Fishing Boat
6
Substitute
4
Troubles
4
Checker
6
Mathematics
6
Enough
[/input]
[output]
Average score: 5.50
Number of problems: 8
Last problem: Mathematics
[/output]
[/test]
[test]
[input]
4
Football Kit
3
Game Statistics
4
Argumented Reality
5
Virtual Reality
6
Cat Walk
3
Problem
4
[/input]
[output]
You need a break, 4 poor grades.
[/output]
[/test]
[test]
[input]
5
Sofia
6
Arested
6
Substitute
4
Graduation Pt3
3
On time for Exam
5
Cat Walk
4
Football Kit 4
4
Festival
3
[/input]
[output]
You need a break, 5 poor grades.
[/output]
[/test]
[test]
[input]
4
Stronger
6
Coliseum
5
Medicine
6
Static play
6
Volleyball
6
New House
6
Old Library
6
Fishing Boat
6
Enough
[/input]
[output]
Average score: 5.88
Number of problems: 8
Last problem: Fishing Boat
[/output]
[/test]
[test]
[input]
3
PlayStation
5
Best Player
5
Poison
5
Enough
[/input]
[output]
Average score: 5.00
Number of problems: 3
Last problem: Poison
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]

[slide hideTitle]
# Problemă: Walking
[code-task title="Walking" taskId="pb-java-while-loop-Walking" executionType="tests-execution" executionStrategy="java-code" requiresInput ]
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
Gaby vrea să înceapă o viață sănătoasă și își propune să meargă **10000 de pași** pe **zi**.

Scrieți un program **care citește de pe consolă câți pași** Gaby merge de fiecare dată când iese și **când atinge obiectivul stabilit**, printează mesajul: 
- "**Goal reached! Good job!**"

În cazul în care vrea să ajungă acasă **înainte de** atingerea scopului, va introduce comanda "**Going home**" și numărul de **pași** pe care i-a **făcut** în timp ce **merge acasă**. 

După aceea, dacă nu reușește să atingă obiectivul, va trebui să imprimați mesajul următor pe consolă: 
- "\{**difference in steps**\} **more steps to reach goal.**"

## Exemple

| **Intrare** | **Ieșire** |
| --- | --- |
| 1000 | Goal reached! Good job! |
| 1500| | 
| 2000| | 
| 6500| |


| **Intrare** | **Ieșire** |
| --- | --- |
| 1500 | 2500 more steps to reach goal. |
| 300| |
| 2500| |
| 3000| |
| Going home| |
| 200| |
[/task-description]
[tests]
[test open]
[input]
1000
1500
2000
6500
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test open]
[input]
1500
300
2500
3000
Going home
200
[/input]
[output]
2500 more steps to reach goal.
[/output]
[/test]
[test]
[input]
1500
3000
250
1548
2000
Going home
2000
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test]
[input]
125
250
4000
30
2678
4682
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test]
[input]
Going home
10000
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test]
[input]
Going home
2000
[/input]
[output]
8000 more steps to reach goal.
[/output]
[/test]
[test]
[input]
1000
1000
2333
1234
12455
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test]
[input]
10000
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test]
[input]
50
505
50
50
50
50
50
50
50
20
450
30
30
30
20
10
30
1
20
30
340
1000
30
40
200
30
200
20
20
1000
1000
305
5066
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test]
[input]
100
100
200
3004
3445
2344
Going home
4000
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test]
[input]
1321
1345
457
6577
Going home
20
[/input]
[output]
280 more steps to reach goal.
[/output]
[/test]
[test]
[input]
Going home
4500
[/input]
[output]
5500 more steps to reach goal.
[/output]
[/test]
[test]
[input]
350
120
1204
1245
7432
[/input]
[output]
Goal reached! Good job!
[/output]
[/test]
[test]
[input]
5000
344
234
2344
Going home
200
[/input]
[output]
1878 more steps to reach goal.
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]

[slide hideTitle]
# Problemă: Dishwasher
[code-task title="Dishwasher" taskId="pb-java-while-loop-Dishwasher" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
John lucrează la un restaurant și este responsabil de încărcarea mașinii de spălat vase, la finalul zilei.

Sarcina voastră este să scrieți un program care să calculeze **dacă** o cantitate de sticle de detergent este  **suficientă** pentru spălarea unui anumit număr de vase.

Știm că fiecare sticlă conține **750 ml.** de detergent. 

Pentru o  **farfurie** sunt necesari 5 ml., iar pentru o **cană** 15 ml. 

La fiecare **a treia** umplere cu vase, mașina de spălat vase este plină doar cu căni, iar în celelalte cazuri cu farfurii. 

Până la primirea comenzii **"END"** veți continua să primiți numărul de vase care trebuie să fie spălate.

## Intrare
Citiți din consolă: 
- **Numărul de sticle de detergent** care vor fi utilizate pentru spălarea vaselor - un număr întreg în intervalul \[1...10\] 
- Pe fiecare linie **următoare**, până la comanda **"End"** sau până ce **cantitatea de detergent este epuizată**, **numărul de vase** care trebuie să fie spălate - un număr întreg în intervalul \[1...100\]

## Ieșire
- În cazul în care cantitatea de detergent **a fost suficientă** pentru spălarea vaselor, printați trei linii de ieșire: 
    - "**Detergent was enough!**"
    - "\{**Number of clean plates**\} **dishes and** \{**number of clean pots**\} **pots were washed.**"
    - "**Leftover detergent** \{**amount of detergent remaining**\} **ml.**" 
- Dacă cantitatea de detergent **nu a fost suficientă** pentru spălarea vaselor, imprimați următoarea linie: 
    - "**Not enough detergent**, \{**quantity not reached detergent**\} **ml. more necessary!**"

## Exemplu

| **Intrare** | **Ieșire** |
| --- | --- |
| 2 | Detergent was enough! |
| 53 | 118 dishes and 55 pots were washed. |
| 65 | Leftover detergent 85 ml. |
| 55 | |
| End | |

[hints]
[hint]
Cantitatea de detergent = 2 \* 750 = 1500 ml.
53 farfurii încărcate = > 53 \* 5 = 265 ml.  1500 \- 265 = 1235 ml. (rest)
65 farfurii = > 65 \* 5 = 325 ml 1235 \- 325 = 910 ml. (rest)
55 căni = > 55 \* 15 = 825 ml 910\- 825 = 85 ml. (rest)
[/hint]
[hint]
Primim comanda "End". Putem concluziona că detergentul a fost suficient, deci mesajele corespunzătoare trebuie imprimate: 
- numărul de farfurii spălate = 53 \+ 65 = 118
- numărul de căni spălate = 55
[/hint]
[/hints]

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| 1 | Not enough detergent, 100 ml. more necessary! |
| 10 | |
| 15 | |
| 10 | |
| 12 | |
| 13 | |
| 30 | |
[/task-description]
[tests]
[test open]
[input]
2
53
65
55
End
[/input]
[output]
Detergent was enough!
118 dishes and 55 pots were washed.
Leftover detergent 85 ml.
[/output]
[/test]
[test open]
[input]
1
10
15
10
12
13
30
[/input]
[output]
Not enough detergent, 100 ml. more necessary!
[/output]
[/test]
[test]
[input]
2
53
65
55
End
[/input]
[output]
Detergent was enough!
118 dishes and 55 pots were washed.
Leftover detergent 85 ml.
[/output]
[/test]
[test]
[input]
1
10
15
10
12
13
30
[/input]
[output]
Not enough detergent, 100 ml. more necessary!
[/output]
[/test]
[test]
[input]
2
25
50
75
End
[/input]
[output]
Detergent was enough!
75 dishes and 75 pots were washed.
Leftover detergent 0 ml.
[/output]
[/test]
[test]
[input]
2
25
50
75
1
[/input]
[output]
Not enough detergent, 5 ml. more necessary!
[/output]
[/test]
[test]
[input]
3
66
33
99
End
[/input]
[output]
Detergent was enough!
99 dishes and 99 pots were washed.
Leftover detergent 270 ml.
[/output]
[/test]
[test]
[input]
3
38
47
59
75
31
29
[/input]
[output]
Not enough detergent, 25 ml. more necessary!
[/output]
[/test]
[test]
[input]
4
25
39
31
20
49
66
33
25
End
[/input]
[output]
Detergent was enough!
191 dishes and 97 pots were washed.
Leftover detergent 590 ml.
[/output]
[/test]
[test]
[input]
1
32
33
45
[/input]
[output]
Not enough detergent, 250 ml. more necessary!
[/output]
[/test]
[test]
[input]
4
52
3
13
39
86
50
49
37
End
[/input]
[output]
Detergent was enough!
266 dishes and 63 pots were washed.
Leftover detergent 725 ml.
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]

[slide hideTitle]
# Problemă: Report System
[code-task title="Report System" taskId="pb-java-while-loop-Report-System" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
La un eveniment caritabil, plata pentru produsele cumpărate se poate face astfel: **plată în numerar și plată cu cardul**. Metoda de plată alternează astfel:

 - Prima plată se face **în numerar**
 - A doua plată se face **cu cardul**
 - A treia plată trebuie să fie **în numerar**, și asa mai departe

Următoarele reguli de plată au fost stabilite:

- Dacă prețul produsului **depășește 100 de dolari**, **atunci acesta nu poate fi achitat în numerar**
- Dacă produsul are prețul **sub 10 dolari**, **acesta nu poate fi achitat cu cardul**

Programul se încheie după ce primim comanda **"End"**, sau după ce **fondurile necesare au fost adunate**.

## Intrare
Citiți din consolă:
- Suma **care trebuie adunată** din vânzări - un număr întreg în intervalul \[1...10000\] 
- Pe fiecare linie următoare până când programul se încheie:
    - **Prețurile produselor** cumpărate - un număr întreg în intervalul \[1...500\]

## Ieșire
Imprimați pe consolă:
- În cazul unei tranzacții reușite: **"Product sold!"** 
- În cazul unei tranzacții eșuate: **"Error in transaction!"**  
- Dacă suma tuturor produselor cumpărate **depășește sau atinge suma așteptată**, programul a fost finalizat și **două linii** sunt imprimate pe consolă: 
    - **"Average CS: \{average payment in cash per person\}"**
    - **"Average CC: \{average payment by card per person\}"**

Plățile trebuie **formatate la a două cifră după punctul zecimal**.
- Când este primită comanda **"End"**, trebuie tipărită **linia** următoare:
    - **"Failed to collect required money for charity."**

## Exemplu

| **Intrare** | **Ieșire** |
| --- | --- |
| 500| Error in transaction!|
| 120| Error in transaction!|
| 8| Product sold!|
| 63| Product sold!|
| 256| Product sold!|
| 78| Product sold!|
| 317| Average CS: 70.50|
| | Average CC: 286.50|

[hints]
[hint]
Condiția este rulată prima oară în **numerar**, apoi prin **card**
120 > 100 tranzacția a fost respinsă 
8 < 10 tranzacție respinsă
63 <= 100 => tranzacție reușită
256 >= 10 => tranzacție reușită
78 <= 100 => tranzacție reușită
317 >= 10 => tranzacție reușită
Suma totală colectată: 63 + 256 + 78 + 317 = 714 
714 >= 500
[/hint]
[hint]
Suma totală în numerar: 63 + 78 = 141;  Suma medie în numerar: 141/2 = 70.50 
Totalul din plata cu cardul: 256 \+ 317 = 573; Suma medie din plata cu cardul: 573/2 = 286.50
[/hint]
[/hints]

[/task-description]
[tests]
[test open]
[input]
500
120
8
63
256
78
317
[/input]
[output]
Error in transaction!
Error in transaction!
Product sold!
Product sold!
Product sold!
Product sold!
Average CS: 70.50
Average CC: 286.50
[/output]
[/test]
[test]
[input]
600
86
150
98
227
End
[/input]
[output]
Product sold!
Product sold!
Product sold!
Product sold!
Failed to collect required money for charity.
[/output]
[/test]
[test]
[input]
500
100
200
100
100
[/input]
[output]
Product sold!
Product sold!
Product sold!
Product sold!
Average CS: 100.00
Average CC: 150.00
[/output]
[/test]
[test]
[input]
100
101
9
80
20
[/input]
[output]
Error in transaction!
Error in transaction!
Product sold!
Product sold!
Average CS: 80.00
Average CC: 20.00
[/output]
[/test]
[test]
[input]
5000
150
890
70
1500
200
1000
End
[/input]
[output]
Error in transaction!
Product sold!
Product sold!
Product sold!
Error in transaction!
Product sold!
Failed to collect required money for charity.
[/output]
[/test]
[test]
[input]
4333
64
333
150
1234
100
6
66
335
End
[/input]
[output]
Product sold!
Product sold!
Error in transaction!
Product sold!
Product sold!
Error in transaction!
Product sold!
Product sold!
Failed to collect required money for charity.
[/output]
[/test]
[test]
[input]
600
25
346
100
256
[/input]
[output]
Product sold!
Product sold!
Product sold!
Product sold!
Average CS: 62.50
Average CC: 301.00
[/output]
[/test]
[test]
[input]
777
120
6
333
8
453
134
End
[/input]
[output]
Error in transaction!
Error in transaction!
Error in transaction!
Error in transaction!
Error in transaction!
Product sold!
Failed to collect required money for charity.
[/output]
[/test]
[test]
[input]
2983
35
995
94
937
38
593
End
[/input]
[output]
Product sold!
Product sold!
Product sold!
Product sold!
Product sold!
Product sold!
Failed to collect required money for charity.
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]

[slide hideTitle]
# Problemă: Graduation
[code-task title="Graduation" taskId="pb-java-while-loop-graduation" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Scrieți un program care să calculeze **nota medie** a unui student pentru întreaga sa perioadă de educație.

## Intrare
- Pe prima linie, vom primi **numele studentului**
- Pe fiecare linie următoare sunt notele pe ani
- Studentul promovează anul dacă **nota anuală este 4.00 sau mai mare** 
- Dacă nota sa este mai mică decât 4.00, el trebuie să **repete** clasa


## Ieșire
- Dacă studentul promovează clasa trebuie să imprimați:

    - "\{**student name**\}**graduated. Average grade:** \{**average grade from his entire education**\}"

**Nota trebuie să fie formatată la a două cifră după punctul zecimal.**

## Exemplu

| **Intrare** | **Ieșire** |
| --- | --- | 
| John | John graduated. Average grade: 5.37 | 
| 4 | |
| 5.5 | | 
| 6 | | 
| 5.43 | |
| 4.5 | | 
| 6 | | 
| 5.55 | | 
| 5 | | 
| 6 | | 
| 6 | | 
| 5.43 | |
| 5 | |
[/task-description]
[tests]
[test open]
[input]
David
4
5.5
6
5.43
4.5
6
5.55
5
6
6
5.43
5
6
[/input]
[output]
David graduated. Average grade: 5.37
[/output]
[/test]
[test]
[input]
Ani
5
5.32
6
5.43
5
6
5.5
4.55
5
6
5.56
6
5
[/input]
[output]
Ani graduated. Average grade: 5.45
[/output]
[/test]
[test]
[input]
John
5
5
5
6
5.5
5
6
5.44
5
5
5
5
6
5.45
[/input]
[output]
John graduated. Average grade: 5.25
[/output]
[/test]
[test]
[input]
Prakash
5
5.43
5.55
6
5.87
5.90
6
6
5.45
5
6
5.76
[/input]
[output]
Prakash graduated. Average grade: 5.66
[/output]
[/test]
[test]
[input]
Monica
6
5.5
5.75
6
6
5
6
5.90
6
6
5
6
[/input]
[output]
Monica graduated. Average grade: 5.76
[/output]
[/test]
[test]
[input]
Alex
4
5
5.5
3.99
6
6
5
4.5
6
5.56
6
6
4
[/input]
[output]
Alex graduated. Average grade: 5.30
[/output]
[/test]
[test]
[input]
Alen
5.6
6
4
4
5
6
3
6
5.4
4.5
6
5.55
6
[/input]
[output]
Alen graduated. Average grade: 5.34
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]

[slide hideTitle]
# Problemă: Stream Of Letters
[code-task title="Stream Of Letters" taskId="pb-java-while-loop-stream-of-letters" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Vom primi simboluri până când comanda **End** este primită. 

Trebuie să omitem caracterele care **nu sunt litere** și prima apariție a **c**, **o** și **n**.

Când **primim prima dată** una dintre aceste litere, trebuie să o marcăm ca vizitată, **dar nu este salvată în cuvânt**.

Dacă am găsit **toate cele trei litere din comandă**, trebuie să imprimăm cuvântul nostru cu un spațiu la sfârșit. Trebuie să resetăm numărătoarea apariției fiecărei litere la 0.

## Intrare
- Vom primi o secvență de linii cu un singur simbol pe linie, până când primim comanda "**End**"

## Ieșire
- Imprimați pe consolă cuvântul, urmat de **un spațiu**

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| H | Hello |
| n| |
| e| |
| l| |
| l| |
| o| | 
| o| |
| c| |
| End| |

[hints]
[hint]
"**H**", "**n**", "**e**", "**l**", "**l**", "**o**", "**o**", "**c**" sunt toate literele citite.
Mai întâi citim simbolul "**H**" și îl adăugăm la cuvânt. Următorul simbol este "**n**". Face parte din comandă și **nu îl adăugăm la cuvânt când îl întâlnim pentru prima dată**.
Următoarele simboluri sunt"**e**", "**l**", "**l**" și le adăugăm la cuvânt. Citim "**o**" și îl notăm ca vizitat, dar încă o dată **nu îl** adăugăm la cuvânt. Următoarea literă este din nou  "**o**" și o adăugăm. Următorul simbol este  "**c**" și toate cele trei simboluri pentru comanda secretă sunt deja disponibile.
[/hint]
[hint]
Imprimăm "**Hello**",  primim comanda  "End" și programul se încheie. Rezultatul este "Hello".
[/hint]
[/hints]

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| % | BooM |
| \!| |
|  c|
| ^| |
| B| |
| \`| | 
| o| |
| %| |
| o| |
| o| |
| M| |
| \)| |
| n| |
| A| |
| D| |
| End| |

## Exemplu
| **Intrare** | **Ieșire** |
| --- | --- |
| o | Solve me |
| S | |
| % | |
| o | |
| l | |
| ^ | |
| v | |
| e | |
| c | |
| n | |
| & | |
| m | |
| e | |
| c | |
| o | |
| n | |
| End | |

[/task-description]
[tests]
[test open]
[input]
H
n
e
l
l
o
o
c
t
c
h
o
e
r
e
n
e
End
[/input]
[output]
Hello there
[/output]
[/test]
[test open]
[input]
%
\!
c
^
B
\`
o
%
o
o
M
\)
\{
n
\\
A
D
End
[/input]
[output]
BooM
[/output]
[/test]
[test]
[input]
o
S
%
o
l
^
v
e
c
n
&
m
e
c
o
n
End
[/input]
[output]
Solve me
[/output]
[/test]
[test]
[input]
c
c
o
o
n
n
End
[/input]
[output]
co
[/output]
[/test]
[test]
[input]
%
$
\!
\)
\(
\{
\}
End
[/input]
[output]
[/output]
[/test]
[test]
[input]
H
e
c
o
@
r
%
e
n
w
c
o
e
n
g
o
c
o
n
w
i
t
n
o
h
c
t
h
c
\*
o
e
n
s
i
g
&
n
n
s
@
c
o
%
n
End
[/input]
[output]
Here we go with the signs
[/output]
[/test]
[test]
[input]
o
n
C
c
n
c
O
o
c
o
N
n
End
[/input]
[output]
C O N
[/output]
[/test]
[test]
[input]
c
o
n
n
c
o
n
o
c
End
[/input]
[output]
   
[/output]
[/test]
[test]
[input]
I
c
n
n
o
t
c
h
o
e
n
n
e
n
c
d
o
L
i
n
k
i
n
P
a
r
k
End
[/input]
[output]
In the end
[/output]
[/test]
[test]
[input]
T
c
h
e
o
r
e
n
I
c
s
o
n
A
c
o
n
H
i
c
d
d
e
n
n
o
M
e
n
s
s
o
a
g
e
c
o
N
o
t
c
n
o
P
r
i
n
n
t
e
d
c
M
a
d
e
Y
o
u
L
o
o
k
\!
End
[/input]
[output]
There Is A Hidden Message Not Printed
[/output]
[/test]
[test]
[input]
O
u
t
%
O
f
%
I
d
e
a
s
End
[/input]
[output]
[/output]
[/test]
[test]
[input]
I
c
o
n
$
L
c
i
k
o
e
n
^
c
N
o
a
r
u
t
o
n
%
a
n
d
^
t
h
i
n
k
&
t
h
a
t
\)
p
e
o
p
l
e
@
a
r
e
\+
b
i
a
s
e
d
\(
t
o
w
a
r
d
s
\)
A
n
i
m
e
s
End
[/input]
[output]
I Like Naruto 
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]
