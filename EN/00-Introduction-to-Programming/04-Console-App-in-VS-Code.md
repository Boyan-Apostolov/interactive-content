[slide hideTitle]
# Console App in VS Code

[video src="https://videos.softuni.org/hls/javascript-basics/00.Introduction-to-Programming/EN/interactive-JS-PB-intorduction-to-programming-30-31-Creating-a-console-application-in-VSC-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

We already have Visual Studio Code and we can start it. 

Create a folder for your project and open it from VS Code:

`[File] -> [Open Folder]`

[image assetsSrc="intro-to-programming-4.png" /]

Create a file `hello.js` to hold your program's source code:

[image assetsSrc="intro-to-programming-5.png" /]

[/slide]

[slide hideTitle]
# Writing the Program Code

[video src="https://videos.softuni.org/hls/javascript-basics/00.Introduction-to-Programming/EN/interactive-JS-PB-intorduction-to-programming-32-32-Demo-Writing-the-program-code-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

The source code of the JS program should be written inside a function, which we later invoke in order to run it. 

Press `[Enter]` after **the opening parentheses** `{` and **start writing**.

The code of the program is written inwards, as this is a part of shaping up the text for convenience during a review and/or debugging. 

Write the following command: 
```js
console.log("Hello, JavaScript!");
```
Here is how our program should look like in Visual Studio Code: 

[image assetsSrc="intro-to-programming-9.png" /]

The command `console.log("Hello JS")` in JavaScript means to print something out `log(…)` on the console `console` in our case to print the text message **Hello JS**, which we should surround by quotation marks.
 
In order to clarify that this is a text. 

In the end of each command in the JavaScript language the symbol `;` is being put and it says that the current command ends (it does not continue on the next line). 

This command is very typical in programming: we say a given **object** should be found (in this case the console) and some **action** should be executed in it (in this case it is printing the text in the brackets).

[/slide]

[slide hideTitle]
# Starting the Program

[video src="https://videos.softuni.org/hls/javascript-basics/00.Introduction-to-Programming/EN/interactive-JS-PB-intorduction-to-programming-33-Starting-the-program-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

To start the program, press `[Ctrl + F5]`

The result will appear in the `[Debug Console]` tab
[image assetsSrc="intro-to-programming-6.png" /]

As you can see the output of the program is the following text message:
```
Hello, JavaScript!
```
In VS Code `[F5]`/`[Ctrl+F5]` keys runs your earliest created `.js` file

If you have multiple `.js` files in VS Code, you may want to start the current file with `[F5]`/`[Ctrl + F5]` \-\> edit the launch configuration

[image assetsSrc="intro-to-programming-7.png" /]

Alternatively, use the "Code Runner" extension
[image assetsSrc="intro-to-programming-8.png" /]
[/slide]

