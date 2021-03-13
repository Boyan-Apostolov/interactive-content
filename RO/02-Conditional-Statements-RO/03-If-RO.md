[slide hideTitle]
# Condiții simple if

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/02-conditional-statements/RO/interactive-programming-basics-with-java-conditional-statements-14-15-simple-conditions-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Una dintre cele mai importante instrucțiuni  din fiecare limbaj de programare este instrucțiunea`if`. 

În programare adeseori  **verificăm  condiții particulare** și efectuăm diferite acțiuni în funcție de rezultatul verificării.
[image assetsSrc="02-usecase-if-statement.png" /]
Acest lucru se execută prin condiția `if`, care are următoarea structură:
```java
if (condition) {
  // condition body;
}
```

## Exemplu: Vreme
Aici, dacă starea vremii ploioase la evaluează in `true`, atunci corpul instrucțiunii este executat.
```java
Scanner scanner = new Scanner(System.in);
String weather = scanner.nextLine();

if (weather.equals("rainy")) {
    System.out.println("Take an umbrella!");
}
```
[/slide]

[slide hideTitle]
# Problemă cu Soluție: Freezing Weather

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/02-conditional-statements/RO/interactive-programming-basics-with-java-conditional-statements-16-problem-and-solution-freezing-weather-new-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Freezing Weather" taskId="pb-java-Conditional-Statements-Freezing-Weather" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```java
import java.util.Scanner;

public class Program {
   public static void main(String[] args) {
      // Scrieți codul aici
    }
}
```
[/code-editor]
[task-description]
# Descriere
Scrieți un program pentru a verifica dacă vremea e rece:

  * Citește o temperatură în Celsius (un număr real reprezentat în virgulă mobilă cu simplă precizie (float))
  * Imprimă "**Freezing weather!**", dacă temperatura este **egală** sau **mai mică de 0**
  
## Exemplu

|**Intrare**|**Ieșire** |
| ---- | ---- |
| -2 | Freezing weather!|
| 4 | (no output)

[/task-description]
[tests]
[test open]
[input]
-2
[/input]
[output]
Freezing weather!
[/output]
[/test]
[test open]
[input]
4
[/input]
[output]
[/output]
[/test]
[test]
[input]
-5
[/input]
[output]
Freezing weather!
[/output]
[/test]
[test]
[input]
-10
[/input]
[output]
Freezing weather!
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

