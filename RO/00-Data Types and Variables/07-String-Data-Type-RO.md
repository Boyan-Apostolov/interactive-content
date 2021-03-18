# Tipul Șir

[slide hideTitle]

# Tipul de Date Șir
[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/01.Java-Fundamentals-Data-types-and-variables/RO/interactive-java-fundamentals-data-types-and-variables-45-48-string-data-type-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Șirurile sunt utilizate pentru stocarea textului.

O variabilă **Șir** conține o colecție de caractere înconjurate de ghilimele duble și are o valoare implicită **nul** (fără valoare).

- Exemplu:
Creați o variabilă de tip **Șir** și atribuiți-i o valoare:

```Java live
String greeting = "Hello";
System.out.println(greeting);
```

## Formatarea șirului

```Java live
String secret = "loves metal music";
String name = "Tom";
String secretRevealed = String.format("%s has a secret, he %s.", name, secret);
System.out.println(secretRevealed);
```

Puteți folosi `String.format` pentru a insera valorile unei variabile șir într-un alt șir.

## Exemplu: Saying Hello

Iată cum putem combina prenumele și numele unei persoane pentru a imprima numele complet al acesteia.

```Java live
String firstName = "John";
String lastName = "Smith";
String fullName = String.format("%s %s", firstName, lastName);
System.out.printf("Your full name is %s.", fullName);
```

## Concatenarea șirului

Operatorul `+` poate fi folosit între șiruri pentru a le combina. 

Aceasta se numește concatenare:

```Java live
String firstName = "John";
String lastName = "Doe";
System.out.println(firstName + " " + lastName);
```

* Rețineți că am adăugat un text gol `(" ")` pentru a crea un spațiu între prenume și prenume pe tipărire


[/slide]

[slide hideTitle]
# Problemă cu Soluție: Concat Names

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/01.Java-Fundamentals-Data-types-and-variables/RO/interactive-java-fundamentals-data-types-and-variables-49-problem-and-solution-concat-names-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Concat Names" taskId="java-fund-1-data-types-lab-concat-names" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Citiți două nume și un delimitator.

Imprimați numele alăturate de delimitator.

## Exemplu
| **Intrare**|**Ieșire**|
| --- | --- |
| John | John->Smith |
| Smith | |
| -> | |

| **Intrare**|**Ieșire**|
| --- | --- |
| Jan | Jan<->White |
| White | |
| <-> | |


[/task-description]
[code-io /]
[tests]
[test open]
[input]
John
Smith
-\>
[/input]
[output]
John-\>Smith
[/output]
[/test]
[test open]
[input]
Jan
White
\<-\>

[/input]
[output]
Jan\<-\>White
[/output]
[/test]
[test open]
[input]
Linda
Terry
=\>

[/input]
[output]
Linda=\>Terry
[/output]
[/test]
[test]
[input]
a
b
\{\}
[/input]
[output]
a\{\}b
[/output]
[/test]
[test]
[input]
a
a
!
[/input]
[output]
a!a
[/output]
[/test]
[test]
[input]
x
y
\*\*
[/input]
[output]
x\*\*y
[/output]
[/test]
[test]
[input]
abc
def
&
[/input]
[output]
abc&def
[/output]
[/test]
[test]
[input]
abc
123
--\>
[/input]
[output]
abc--\>123
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

