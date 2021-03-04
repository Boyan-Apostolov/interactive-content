[slide]
# Tipuri Booleene și de Caractere


Un tip de date boolean este declarat cu cuvântul cheie **boolean** cu două opțiuni de valoare: **true** sau **false**:

```java live
 int firstNumber = 5;
 int secondNumber = 10;

 boolean firstBoolean = true;
 boolean secondBoolean = false;

 if (firstNumber < secondNumber) {
  System.out.println(firstBoolean);
 } else {
  System.out.println(secondBoolean);
 }       
```


[/slide]

[slide hideTitle]
# Problem with Solution: Special Numbers

[code-task title="Special Numbers" taskId="java-fund-data-types-lab-special-numbers" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Descriere
Un **număr** este **special** când **suma cifrelor sale este 5, 7 sau 11**.

Scrieți un program pentru a citi un număr întreg **n** și pentru toate numerele din intervalul **1 ... n** pentru a imprima numărul și dacă este special sau nu **(True / False)**.

## Exemplu
|**Intrare**|**Ieșire**|
| --- | --- |
| 15 | 1 -> False|
|  | 2 -> False |
|  | 3 -> False |
|  | 4 -> False |
|  | 5 -> True |
|  | 6 -> False |
|  | 7 -> True |
|  | 8 -> False |
|  | 9 -> False |
|  | 10 -> False |
|  | 11 -> False |
|  | 12 -> False |
|  | 13 -> False |
|  | 14 -> True |
|  | 15 -> False |
 
### Sugestii
Pentru a calcula suma cifrelor unui număr dat **num**, puteți repeta următoarele: suma ultimei cifre **(num % 10)** și scoaterea acesteia **(sum = sum / 10)** până la **num** ajunge la **0**.

[/task-description]
[code-io /]
[tests]
[test open]
[input]
15
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
[/output]
[/test]
[test]
[input]
1
[/input]
[output]
1 -\> False
[/output]
[/test]
[test]
[input]
5
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
[/output]
[/test]
[test]
[input]
4
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
[/output]
[/test]
[test]
[input]
40
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
16 -\> True
17 -\> False
18 -\> False
19 -\> False
20 -\> False
21 -\> False
22 -\> False
23 -\> True
24 -\> False
25 -\> True
26 -\> False
27 -\> False
28 -\> False
29 -\> True
30 -\> False
31 -\> False
32 -\> True
33 -\> False
34 -\> True
35 -\> False
36 -\> False
37 -\> False
38 -\> True
39 -\> False
40 -\> False
[/output]
[/test]
[test]
[input]
75
[/input]
[output]
1 -\> False
2 -\> False
3 -\> False
4 -\> False
5 -\> True
6 -\> False
7 -\> True
8 -\> False
9 -\> False
10 -\> False
11 -\> False
12 -\> False
13 -\> False
14 -\> True
15 -\> False
16 -\> True
17 -\> False
18 -\> False
19 -\> False
20 -\> False
21 -\> False
22 -\> False
23 -\> True
24 -\> False
25 -\> True
26 -\> False
27 -\> False
28 -\> False
29 -\> True
30 -\> False
31 -\> False
32 -\> True
33 -\> False
34 -\> True
35 -\> False
36 -\> False
37 -\> False
38 -\> True
39 -\> False
40 -\> False
41 -\> True
42 -\> False
43 -\> True
44 -\> False
45 -\> False
46 -\> False
47 -\> True
48 -\> False
49 -\> False
50 -\> True
51 -\> False
52 -\> True
53 -\> False
54 -\> False
55 -\> False
56 -\> True
57 -\> False
58 -\> False
59 -\> False
60 -\> False
61 -\> True
62 -\> False
63 -\> False
64 -\> False
65 -\> True
66 -\> False
67 -\> False
68 -\> False
69 -\> False
70 -\> True
71 -\> False
72 -\> False
73 -\> False
74 -\> True
75 -\> False
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


