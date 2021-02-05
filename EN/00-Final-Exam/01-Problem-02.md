# Problem 2: Mountain Run

[slide hideTitle]

# Description

George decides to improve the record for the fastest climb to Mont Blanc.

The input consists of the record George has to improve in seconds, the distance - in meters, and the time it takes for one meter - in seconds.

Create a function that determines **whether he has coped with the task**, given that:

- The slope of the terrain **slows him down by 30** seconds for **every 50 meters**.

**Calculate** the seconds George will need to climb the **distance** to the top and the time **difference from the record**.

When **calculating how many times George will slow down** as a result of the slope of the field's slope, the result should be **rounded down to the nearest whole number.**


## Input

The input comes as an **array of which contains three numbers**:

- **First Number:**  

The record in seconds, floating-point  in the interval \[0.00 … 100000.00\]

- **Second Number:** 

The distance in meters, floating-point in the interval \[0.00 … 100000.00\]

- **Third Number:**

The time in seconds for which he climbs 1 meter, floating-point in the interval \[0.00 … 1000.00\]

## Output

Printing on the console depends on the results:

- If George has improved the record, print: 

`Yes! The new record is {George's time} seconds.`

- If he has NOT improved the record, print: 

`No! He was {time needed} seconds slower.` 

The result must be **formatted** to the second digit after the decimal point.

[code-task title="Mountain Run" taskId="js-pb-final-exam-Mountain-Run" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function solve(input) {
	// Write your code here
}
```
[/code-editor]
[code-adapter]
```
(input, code) => {return code(input.map(Number))}
```
[/code-adapter]
[task-description]

# Example

| **Input** | **Output** |
| --- | --- |
|`[10164, 1400, 25]` | No! He was 25676.00 seconds slower. |


## Comments

- George has to **climb 1400 m.**:  `1400 * 25 = 35000 seconds`

- Every **50 meters**, **30 seconds are added** to his time: `(1400 / 50) * 30 = 840 seconds`

- Total time: `35000 + 840 = 35840 seconds`

- But because `10164 < 35840`, it did not **improve the record.**

- He **did not have enough time** to improve the record: `35840 - 10164 = 25676 seconds`


[/task-description]
[code-io /]
[tests]
[test open]
[input]
10164
1400
25
[/input]
[output]
No! He was 25676.00 seconds slower.
[/output]
[/test]
[test open]
[input]
5554.36
1340
3.23
[/input]
[output]
Yes! The new record is 5108.20 seconds.
[/output]
[/test]
[test open]
[input]
1377
389
3
[/input]
[output]
No! He was 0.00 seconds slower.
[/output]
[/test]
[test]
[input]
1052
100
9.77
[/input]
[output]
Yes! The new record is 1037.00 seconds.
[/output]
[/test]
[test]
[input]
108
89
0.5
[/input]
[output]
Yes! The new record is 74.50 seconds.
[/output]
[/test]
[test]
[input]
100000
100000
1000
[/input]
[output]
No! He was 99960000.00 seconds slower.
[/output]
[/test]
[test]
[input]
99999.9999
74738.1
0.2
[/input]
[output]
Yes! The new record is 59767.62 seconds.
[/output]
[/test]
[test]
[input]
2.25
5
0.5
[/input]
[output]
No! He was 0.25 seconds slower.
[/output]
[/test]
[test]
[input]
344444
378
417
[/input]
[output]
Yes! The new record is 157836.00 seconds.
[/output]
[/test]
[test]
[input]
1174
150
7
[/input]
[output]
Yes! The new record is 1140.00 seconds.
[/output]
[/test]
[test]
[input]
7.55
5
0.02
[/input]
[output]
Yes! The new record is 0.10 seconds.
[/output]
[/test]
[test]
[input]
357.5
15
23
[/input]
[output]
Yes! The new record is 345.00 seconds.
[/output]
[/test]
[test]
[input]
3164
3000
0.221
[/input]
[output]
Yes! The new record is 2463.00 seconds.
[/output]
[/test]
[test]
[input]
1401
891
1
[/input]
[output]
No! He was 0.00 seconds slower.
[/output]
[/test]
[test]
[input]
1526
68
22
[/input]
[output]
No! He was 0.00 seconds slower.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]