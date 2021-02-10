# Installing Mocha And Chai Globally

[slide hideTitle]

# Global Installation

[video src="https://videos.softuni.org/hls/Javascript/Javascript-Applications/01.JS-Applications-Unit-Testing/EN/interactive-js-apps-unit-testing-11-12-13-14-global-installation-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

To install frameworks and libraries globally, use the Windows "CMD" or Visual Studio Code "npm".

Open an instance of the terminal in Visual Studio Code.

Type in the following commands to install **Mocha** and **Chai** globally:

```js
npm install -g mocha
```

```js
npm install -g chai
```

Check if Mocha is installed.

```js
mocha --version
```

# Node Path Configuration

By default `Node.js` does not find its globally installed modules.

You need to set the `NODE_PATH` environment variable manually.

Open the Windows `CMD` console.

To set the path use this piece of code for any future sessions.

`setx NODE_PATH %AppData%\npm\node_modules`

Use this piece of code to set the path for the current session.

`set NODE_PATH=%AppData%\npm\node_modules`

You may need to restart your IDE after changing the "NODE_PATH".

To load a library first, we need to **require** it, like in the example below.

`const expect = require("chai").expect;`

```js
const expect = require("chai").expect;
describe("Test group #1", function () {
    it("should… when…", function () {
        expect(actual).to.be.equal(expected);
    });
    it("should… when…", function () { … });
});
describe("Test group #2", function () {
    it("should… when…", function () {
        expect(actual).to.be.equal(expected);
    });
});
```

[/slide]

[slide hideTitle]
# Problem: Sum Of Numbers

[vimeo-video]
[stream language="EN" videoId="497187668/5cbd6f3899" default /]
[stream language="RO" videoId="497187668/5cbd6f3899"  /]
[/video-vimeo]

[code-task title="Problem: Sum Of Numbers" taskId="js-applications-Unit-Testing-lab-Sum-Of-Numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]

```

```
[/code-editor]
[task-description]
## Description

Write tests to check the functionality of the following code:

```js
function sum(arr) {
    let sum = 0;
    for (num of arr)
        sum += Number(num);
    return sum;
}
```

In your tests, use a function called `sum()`. 

It should meet the following requirements:
- Take an array of numbers as an argument
- Return the sum of the values of all elements inside the array

# Example

[/task-description]
[code-io /]
[tests]
[test]
[input]
//\<minTestCount\>3\</minTestCount\> - specifies the minimum amount of tests your code should have.
let sum = function(arr)\{\};
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
sum = function(arr) \{
    let sum = 0;
    for (let num of arr)
        sum += Number(num);
    return sum;
\};
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
sum = function(arr) \{
    let sum = "0";
    for (let num of arr)
        sum += Number(num);
    return sum;
\};
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
sum = function(arr) \{
    let sum = 0;
    for (let i = 0; i \< arr.length - 1; i++)
        sum += Number(arr\[i\]);
    return sum;
\};
[/input]
[output]
Test Passed!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide hideTitle]
# Solution: Sum Of Numbers

[vimeo-video]
[stream language="EN" videoId="497186830/02a87caa7f" default /]
[stream language="RO" videoId="497186830/02a87caa7f"  /]
[/video-vimeo]

[code-task title="Problem: Sum Of Numbers" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]

```

```
[/code-editor]
[task-description]
## Description

Write tests to check the functionality of the following code:

```js
function sum(arr) {
    let sum = 0;
    for (num of arr)
        sum += Number(num);
    return sum;
}
```

In your tests, use a function called `sum()`. 

It should meet the following requirements:
- Take an array of numbers as an argument
- Return the sum of the values of all elements inside the array

# Example

[/task-description]
[code-io /]
[tests]
[test]
[input]
//\<minTestCount\>3\</minTestCount\> - specifies the minimum amount of tests your code should have.
let sum = function(arr)\{\};
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
sum = function(arr) \{
    let sum = 0;
    for (let num of arr)
        sum += Number(num);
    return sum;
\};
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
sum = function(arr) \{
    let sum = "0";
    for (let num of arr)
        sum += Number(num);
    return sum;
\};
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
sum = function(arr) \{
    let sum = 0;
    for (let i = 0; i \< arr.length - 1; i++)
        sum += Number(arr\[i\]);
    return sum;
\};
[/input]
[output]
Test Passed!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
