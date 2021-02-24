// sectionId: "Javascript::Programming-Basics::Conditional-Statements::Homework"

# Homework
[slide hideTitle]

# Problem with Solution: Guess the Password

[video src="https://videos.softuni.org/hls/javascript-basics/02.Conditions/EN/problem1-Guess-the-Password-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Guess the Password" taskId="pb-js-Conditions-Guess-The-Password" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function guessThePassword(input) {
    // Write your code here
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

Create a program, which verifies a password:

* You receive a string: the password **guess**
* Print "**Welcome**" if the password guess is "**s3cr3t!**"
* Print "**Wrong password!**" in all other cases 

# Example

| **Input** | **Output** |
| --- | --- |
| guessThePassword('s3cr3t!') | Welcome |
| guessThePassword('qwerty') | Wrong password! |

[/task-description]
[tests]
[test open]
[input]
guessThePassword('s3cr3t!')
[/input]
[output]
Welcome
[/output]
[/test]
[test open]
[input]
guessThePassword('qwerty')
[/input]
[output]
Wrong password!
[/output]
[/test]
[test]
[input]
guessThePassword('wrong')
[/input]
[output]
Wrong password!
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem with Solution: Boiling Water

[video src="https://videos.softuni.org/hls/javascript-basics/02.Conditions/EN/problem2-Boiling-Water-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Boiling Water" taskId="pb-js-Conditions-Boiling-Water" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function boilingWater(input) {
    // Write your code here
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

Create a program, which determines if the water in a pot is boiling: 

* You receive a floating-point number: the water **temperature** (in °C)
* Print "**The water is boiling**" if the number is **equal to** or **bigger** than 100.0
* Print "**The water is not hot**" enough in all other cases 

  # Example

| **Input** | **Output** |
| --- | --- |
| boilingWater(104.8) | The water is boiling |
| boilingWater(29) | The water is not hot enough |

[/task-description]
[tests]
[test]
[input]
boilingWater(104.8)
[/input]
[output]
The water is boiling
[/output]
[/test]
[test]
[input]
boilingWater(29)
[/input]
[output]
The water is not hot enough
[/output]
[/test]
[test]
[input]
boilingWater(105)
[/input]
[output]
The water is boiling
[/output]
[/test]
[test]
[input]
boilingWater(10)
[/input]
[output]
The water is not hot enough
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Speed Info
[code-task title="Speed Info" taskId="pb-js-Conditions-Speed-Info" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function speedInfo(input) {
    // Write your code here
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
Create a program, which determines if you are moving **fast** or **slow** with a given speed: 

* You receive the **speed**: (a floating-point number)
* Print "**Slow**" if the speed is **smaller than** or **equal to** 30
* Print "**Fast**" if the speed is bigger than 30

  # Example

| **Input** | **Output** |
| --- | --- |
| speedInfo(30) | Slow |
| speedInfo(60) | Fast |

[/task-description]
[tests]
[test open]
[input]
speedInfo(30)
[/input]
[output]
Slow
[/output]
[/test]
[test open]
[input]
speedInfo(60)
[/input]
[output]
Fast
[/output]
[/test]
[test]
[input]
43
[/input]
[output]
Fast
[/output]
[/test]
[test]
[input]
speedInfo(49)
[/input]
[output]
Fast
[/output]
[/test]
[test open]
[input]
speedInfo(20)
[/input]
[output]
Slow
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Bonus Score
[code-task title="Bonus Score" taskId="pb-js-Conditions-Bonus-Score" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function bonusScore(input) {
    // Write your code here
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
You receive an integer, which represents the initial **number** of points. 

**Bonus points** are awarded according to the rules described below. 

Create a program, which calculates:

- The **received** bonus points from the number 

- Which the initial **total number of points** is

- Which the **number plus the bonus points** is

If the number is up to **100 inclusive**, the bonus points are **5**.
If the number is **greater than 100**, the bonus points are **20 percent of the number**.
If the number is **greater than 1000**, the bonus points are **10 percent of the number**.

Additional bonus points, added separately from the previous ones:

- For an even number you add 1 point

- For a number ending in 5, you add 2 points

# Example

| **Input** | **Output** |
| --- | --- |
| bonusScore(20)| 6 |
|  |26 |
| bonusScore(175)| 37 |
|  |212 |
| bonusScore(2703)| 270.3 |
|  |2973.3 |

[/task-description]
[tests]
[test open]
[input]
bonusScore(20)
[/input]
[output]
6
26
[/output]
[/test]
[test open]
[input]
bonusScore(175)
[/input]
[output]
37
212
[/output]
[/test]
[test open]
[input]
bonusScore(2703)
[/input]
[output]
270.3
2973.3
[/output]
[/test]
[test]
[input]
bonusScore(140)
[/input]
[output]
29
169
[/output]
[/test]
[test]
[input]
bonusScore(175)
[/input]
[output]
37
212
[/output]
[/test]
[test]
[input]
bonusScore(35)
[/input]
[output]
7
42
[/output]
[/test]
[test]
[input]
bonusScore(17)
[/input]
[output]
5
22
[/output]
[/test]
[test]
[input]
bonusScore(0)
[/input]
[output]
6
6
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

[slide hideTitle]
# Problem: Tickets
[code-task title="Tickets" taskId="pb-js-Conditions-Tickets" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function tickets(input) {
    // Write your code here
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
Create a program, which calculates ticket price:

* You receive a ticket type: either **student** or **regular**

* Print the **price** in the following format **$**\{**price**\}:
    * The price should be **formatted** to 2nd digit after the decimal point

* Student ticket price: **1.00**

* Regular ticket price: **1.60**

* For invalid tickets, print: "**Invalid ticket type!**"

# Example

| **Input** | **Output** |
| --- | --- |
| tickets('student') | $1.00 |
| tickets('teacher') | Invalid ticket type! |


[/task-description]
[tests]
[test]
[input open]
tickets('student')
[/input]
[output]
$1.00
[/output]
[/test]
[test]
[input]
tickets('regular')
[/input]
[output]
$1.60
[/output]
[/test]
[test]
[input]
tickets('ticket')
[/input]
[output]
Invalid ticket type!
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]

[/slide]

