# Classes

[slide]
# What Are Classes ?

[video src="https://videos.softuni.org/hls/02.fundamentals-objects-maps-strings/01.JS-Fundamentals-Objects-and-classes/EN/01.JS-Fundamentals-Object-and-Classes-24-25-What-are-classes-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

A **class** is like a **blueprint** (or template) for creating **objects**.

Classes provide means of **bundling data and functionality** together.

Each class instance can have **attributes** attached to it.

Class instances can also have **methods** for **modifying its state**, they are its **behavior**.
[/slide]

[slide]
# Class Declaration

[video src="https://videos.softuni.org/hls/02.fundamentals-objects-maps-strings/01.JS-Fundamentals-Objects-and-classes/EN/01.JS-Fundamentals-Object-and-Classes-26-Class-declaration-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Example: 

``` js
class Student {
  constructor(name) {
    this.name = name;
  }
}
```

To declare a class we use the `class` keyword with the name of the class, in this case `Student`.

The `constructor` is a special method for creating and initializing an object.
[/slide]

[slide]
# Class example

[video src="https://videos.softuni.org/hls/02.fundamentals-objects-maps-strings/01.JS-Fundamentals-Objects-and-classes/EN/01.JS-Fundamentals-Object-and-Classes-27-Class-example-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

The `class` keyword is used to create a class.

**Class attributes** are **the same for all instances of the class**.

**Instance attributes** are **unique to each instance of the class**.

```js
class Student {
  constructor(name, grade) {
    this.name = name;
    this.grade = grade;
  }
}
```

The `this` keyword is used to set a property of the objects to a given value.

This is how we create an **instance** of the `Student` class:

```js
let student = new Student('Peter', 5.50);
```
[/slide]

[slide]
# Functions in a Class

[video src="https://videos.softuni.org/hls/02.fundamentals-objects-maps-strings/01.JS-Fundamentals-Objects-and-classes/EN/01.JS-Fundamentals-Object-and-Classes-28-Functions-in-a-class-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

The ability to modify data is performed by special functions that are a part of the class, which are called methods. 

The JavaScript classes support both **instance** and **static** methods.

Instance methods can **access and modify** instance data.

Instance methods can call other instance methods, as well as any static method.

``` js live
class Dog {
  constructor() {
    this.speak = () => {
      console.log('Woof');
    }
  }
}

let dog = new Dog();
dog.speak();
```

[/slide]

[slide]
# Problem: Cats

[vimeo-video]
[stream language="EN" videoId="489795072/b02a97d757" default /]
[stream language="RO" videoId="489795072/b02a97d757"  /]
[/video-vimeo]

[code-task title="Cats" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function cats(input){
  // Write your code here
}
```
[/code-editor]
[task-description]
# Description

Write a function that receives array of strings in the following format `{cat name} {age}`.

Create a Cat class that receives in the constructor the name and the age parsed from the input. 

It should also have a function named `meow` that will print `{cat name}, age {age} says Meow` on the console.

For each of the strings provided you must create a cat object.

# Example
  | **Input** | **Output** |
| --- | --- |
|`['Mellow 2', 'Tom 5']`| Mellow, age 2 says Meow|
||Tom, age 5 says Meow|

# Hints

* Create a Cat class with properties and methods described above

* Parse the input data

* Create all objects using class constructor and the parsed input data, store them in an array

* Loop through the array using `for…of` cycle and invoke `.meow()` method


[/task-description]
[tests]
[test]
[input]
jsakd 45
dasd 12
[/input]
[output]
jsakd, age 45 says Meow
dasd, age 12 says Meow
[/output]
[/test]
[test]
[input]
jsakd 45
gyug 11
vtv 2
vv 1
huuh 9
[/input]
[output]
jsakd, age 45 says Meow
gyug, age 11 says Meow
vtv, age 2 says Meow
vv, age 1 says Meow
huuh, age 9 says Meow
[/output]
[/test]
[test]
[input]
jsakd 5
huh 2
f 1
huuh 9
[/input]
[output]
jsakd, age 5 says Meow
huh, age 2 says Meow
f, age 1 says Meow
huuh, age 9 says Meow
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]

[slide]
# Solution: Cats

[vimeo-video]
[stream language="EN" videoId="489795144/890591bfdb" default /]
[stream language="RO" videoId="489795144/890591bfdb"  /]
[/video-vimeo]

[code-task title="Cats" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
//Different vido code

function solve(input){
    let cats =[]
    class Cat {
        constructor(name, age) {
            this.name = name
            this.age = age
        }
        sayHello(){
            console.log(`${this.name}, age ${this.age} says Meow`)
        }
    }
    for (let i = 0; i < input.length; i++) {
        let catData = input[i].split(' ')
        let [name, age] = catData
        cats.push(new Cat(name, age))
    }

    for (const key of cats) {
        key.sayHello()
    }
}
```
[/code-editor]
[task-description]
# Description

Write a function that receives array of strings in the following format `{cat name} {age}`.

Create a Cat class that receives in the constructor the name and the age parsed from the input. 

It should also have a function named `meow` that will print `{cat name}, age {age} says Meow` on the console.

For each of the strings provided you must create a cat object.

# Example
  | **Input** | **Output** |
| --- | --- |
|`['Mellow 2', 'Tom 5']`| Mellow, age 2 says Meow|
||Tom, age 5 says Meow|

# Hints

* Create a Cat class with properties and methods described above

* Parse the input data

* Create all objects using class constructor and the parsed input data, store them in an array

* Loop through the array using `for…of` cycle and invoke `.meow()` method


[/task-description]
[tests]
[test]
[input]
jsakd 45
dasd 12
[/input]
[output]
jsakd, age 45 says Meow
dasd, age 12 says Meow
[/output]
[/test]
[test]
[input]
jsakd 45
gyug 11
vtv 2
vv 1
huuh 9
[/input]
[output]
jsakd, age 45 says Meow
gyug, age 11 says Meow
vtv, age 2 says Meow
vv, age 1 says Meow
huuh, age 9 says Meow
[/output]
[/test]
[test]
[input]
jsakd 5
huh 2
f 1
huuh 9
[/input]
[output]
jsakd, age 5 says Meow
huh, age 2 says Meow
f, age 1 says Meow
huuh, age 9 says Meow
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]