# Creating Custom Classes

[slide hideTitle]
# Defining Simple Classes

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-14-15-defining-simple-classes-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

When defining a class, it contains only those components of a class declaration that are required.

The **obligatory** components are:

- The `class` keyword

- A **name** for the class

- The **body** of the class, between **curly brackets**

Not obligatory, but **credential** components are: 

- Class fields

- Constructor

- Getters and Setters

- Class methods

Each **class**, **field**, **constructor** or **method** is initialized with an **access modifier** in front, which specifies the **accessibility**. 

Тhe **access level** can be **changed** by applying the **access modifier** on it. 

We will cover this in the next course. 

There is a possibility to generate **automatically** via IntelliJ IDEA **constructors**, **getters**, **setters**, and other most used methods. 

To do so, just use `Right-click + Generate`. 

The short command depends on the operation system of the computer: 

- In Windows and Linux it is `Alt + Insert` 

- In Macintosh it is `Cmd + N`

[/slide]


[slide hideTitle]
# Naming Classes

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-16-naming-classes-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

The class name is with the initial letter capitalized by convention, i.e. **PascalCase naming**. 

The class name should contain descriptive nouns.

Abbreviations are required to be avoided (except widely known, e.g. URL, HTTP, etc.).

```java
public class CompanyEmployee {

}
```

[/slide]

[slide hideTitle]

# Class Members

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-17-19-class-members-methods-getters-and-setters-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

**Fields** and **methods** define the **state** and **behavior** of a class.

**Fields** provide the state of the class and its objects:

- `String type` 

- `int age`

**Methods** implement the behavior of the class and its objects: 

- `makeSound()`

Consider the following example:

```java
class Car {

    //Field
    private int fuel;

    //Method
    public void drive() {...}
}
```

[/slide]

[slide hideTitle]
# Methods

It was previously covered that methods describe the **behavior** of an object.

They can do so by storing **executable code** which manipulates the **state** when called.

Take a look at how a method affects a field:

```java
class Car {
  public int fuel;

  public int drive(distance) {
    int fuelBurned = distance * 0.1;
    
    // Modifies the state
    this.fuel -= fuelBurned;

    return fuelBurned;
  }
}
```

[/slide]

[slide hideTitle]
# Getters and Setters

A getter and a setter can be declared for each field.

Getters provide **access** to the field and read its value. 

They always begin with the word `get`, followed by the variable name:

- `getColor`

- `getType`

Since the getter method is **return** type, the data type of the value returned by the method is the same as the field type.

Setters **change** and **update** a field's value.

They always begin with the word `set`, followed by the variable name:

- `setColor`

- `setType`

The setter method is of type **void**.

```java
public class Car {
    // field
    private int fuel;
    . . .
    // getter
    public int getFuel() {
        return this.fuel;
    }

    // setter
    public void setFuel(int fuel) {
        this.fuel = fuel;
    }
}
```

[/slide]

[slide hideTitle]

# Creating an Object

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-20-22-creating-an-object-constructors-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Each time an object is **created**, some **memory** is **dedicated** for it.

This is why **local variables** are created as **references** to that part of the memory.

The **Java Virtual Machine** is responsible for **tracking** the object references.

If there are **no references** to an object, it becomes **garbage** and is **deleted**.

It is possible to create **many objects** out of one class by using the `new` keyword.

Consider the following example:

```java
class Program {
  public static void main(String[] args) {
    Car sedan = new Car();
    Car coupe = new Car();
  }
}
```

[/slide]

[slide hideTitle]
# Constructor

A special method, executed during object creation, that **sets object's initial state**.

The constructor name is the **same as the name of the class**.

Constructor **can take parameters**, which is used to **initialize fields**.

All classes have **constructor by default**. 

There can be **multiple constructors of the same class**. 

This helps to instantiate objects in various ways with a different number of arguments.

```java
public class Animal {
    // fields
    private String type;
    private int age;
    private boolean herbivorous;

    // constructors
    public Animal() {

    }
    public Animal(String type) {
        this.type = type;
    }
}
```

[/slide]

[slide hideTitle]
# Problem with Solution: Students

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-problem-and-solution-students-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Students" taskId="java-fund-2-Objects-and-Classes-lab-Students" executionType="tests-execution" executionStrategy="java-zip-file-code" requiresInput]

[task-description]
## Description

Define a class **Student**, which holds the following information about students: 
 - first name
 - last name
 - age
 - hometown

### Input / Constraints

Read a list of students until you receive **"end"** command.

After that, you will receive a **city name**.

### Output

Print only students which are from the given city, in the following format: 
"\{firstName\} \{lastName\} is \{age\} years old.".

## Example
| **Input** | **Output** |
| --- | --- |
| Anthony Taylor 15 Chicago | Anthony Taylor is 15 years old. |
| David Anderson 16 Washington | Jack Lewis is 14 years old. |
| Jack Lewis 14 Chicago | David Lee is 14 years old. |
| David Lee 14 Chicago | |
| end | |
| Chicago | |



[/task-description]
[code-upload allowedMemory="30" /]
[tests]
[test]
[input]
John Smith 15 Sofia
Peter Ivanov 14 Plovdiv
Linda Bridge 16 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 15 years old
Linda Bridge is 16 years old
[/output]
[/test]
[test open]
[input]
Anthony Taylor 15 Chicago
David Anderson 16 Washington
Jack Lewis 14 Chicago
David Lee 14 Chicago
end
Chicago
[/input]
[output]
Anthony Taylor is 15 years old
Jack Lewis is 14 years old
David Lee is 14 years old
[/output]
[/test]
[test]
[input]
Anthony Taylor 13 varna
David A 14 b
Jack L 16 varna
David Lee 17 varna
end
varna
[/input]
[output]
Anthony Taylor is 13 years old
Jack L is 16 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
Thony Taylor 13 varna
David A 14 b
Jack L 16 varna
David Lee 17 b
end
b
[/input]
[output]
David A is 14 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
T T 13 varna
b Aa 14 b
N m 21 c
Jack L 16 varna
David Lee 17 b
end
c
[/input]
[output]
N m is 21 years old
[/output]
[/test]
[test]
[input]
T T 13 v
b Aa 14 v
N m 21 v
Jack L 16 v
David Lee 17 v
end
v
[/input]
[output]
T T is 13 years old
b Aa is 14 years old
N m is 21 years old
Jack L is 16 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
T T 22 a
b Aa 14 e
N m 30 c
Jack L 18 e
Port Lee 14 e
end
e
[/input]
[output]
b Aa is 14 years old
Jack L is 18 years old
Port Lee is 14 years old
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem with Solution: Students 2.0

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-problem-and-solution-students-2.0-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Students 2.0" taskId="java-fund-2-Objects-and-Classes-lab-Students-2.0" executionType="tests-execution" executionStrategy="java-zip-file-code" requiresInput]

[task-description]
## Description
Use the class from the previous problem.

If you receive a student, who already exists (**first name** and **last name** should be **unique**) overwrite the information.

## Examples

| **Input** | **Output** |
| --- | --- |
| John Smith 15 Sofia | John Smith is 16 years old. |
| John Smith 16 Sofia | Linda Bridge is 17 years old. |
| Linda Bridge 17 Sofia | |
| Simon Stone 12 Varna | |
| end | |
| Sofia | |


[/task-description]
[code-upload allowedMemory="30" /]
[tests]
[test open]
[input]
John Smith 15 Sofia
John Smith 16 Sofia
Linda Bridge 17 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 16 years old
Linda Bridge is 17 years old
[/output]
[/test]
[test]
[input]
John Smith 15 Sofia
Peter Ivanov 14 Plovdiv
Peter Ivanov 14 Sofia
Linda Bridge 16 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 15 years old
Peter Ivanov is 14 years old
Linda Bridge is 16 years old
[/output]
[/test]
[test]
[input]
J S 3 S
Peter Ivanov 14 P
P J 104 S
J P 61 S
Simon Stone 12 Varna
Simon Sone 12 Varna
end
Varna
[/input]
[output]
Simon Stone is 12 years old
Simon Sone is 12 years old
[/output]
[/test]
[test]
[input]
J S 3 S
Peter Ivanov 14 P
P J 104 S
J P 61 S
Simon Stone 12 Varna
Simon Sone 12 Varna
end
S
[/input]
[output]
J S is 3 years old
P J is 104 years old
J P is 61 years old
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem with Solution: Songs

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/02.Java-Fundamentals-Objects-and-Classes/EN/interactive-java-fundamentals-objects-and-classes-problem-and-solution-songs-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Songs" taskId="java-fund-2-Objects-and-Classes-lab-Songs" executionType="tests-execution" executionStrategy="java-zip-file-code" requiresInput]
[task-description]
## Description

Define a class **Song**, which holds the following information about songs: 
- **Type List**

- **Name**

- **Time**

### Input / Constraints

- On the first line you will receive the **number of songs - N**.

- On the next N-lines you will be receiving data in the following format: 
"\{typeList\}\_\{name\}\_\{time\}".

- On the last line you will receive **Type List** or **"all"**.

### Output

Print only the **Names of the songs** which are from that **Type List** or **All songs**.

## Examples

| **Input** | **Output** |
| --- | --- |
| 3 | DownTown |
| favourite_DownTown_3:14 | Kiss |
| favourite_Kiss_4:16 | Smooth Criminal |
| favourite_Smooth Criminal_4:01 | |
| favourite | |

| **Input** | **Output** |
| --- | --- |
| 4 | Andalouse |
| favourite_DownTown_3:14 | |
| listenLater_Andalouse_3:24 | |
| favourite_In To The Night_3:58 | |
| favourite_Live It Up_3:48 | |
| listenLater | |

| **Input** | **Output** |
| --- | --- |
| 2 | Replay |
| like_Replay_3:15 | Photoshop |
| ban_Photoshop_3:48 | |
| all | |



[/task-description]
[code-upload allowedMemory="30" /]
[tests]
[test open]
[input]
3
favourite_DownTown_3:14
favourite_Kiss_4:16
favourite_Smooth Criminal_4:01
favourite
[/input]
[output]
DownTown
Kiss
Smooth Criminal
[/output]
[/test]
[test open]
[input]
4
favourite_DownTown_3:14
listenLater_Andalouse_3:24
favourite_In To The Night_3:58
favourite_Live It Up_3:48
listenLater
[/input]
[output]
Andalouse
[/output]
[/test]
[test open]
[input]
2
like_Replay_3:15
ban_Photoshop_3:48
all
[/input]
[output]
Replay
Photoshop
[/output]
[/test]
[test]
[input]
4
v_rrr_3:14
listenLater_rr_3:24
v_r_3:58
v_rp_3:48
v
[/input]
[output]
rrr
r
rp
[/output]
[/test]
[test]
[input]
6
v_rrr_3:14
listenLater_rr_3:24
v_r_3:58
v_rp_3:48
b_wqeq_3:58
b_tre_3:48
b
[/input]
[output]
wqeq
tre
[/output]
[/test]
[test]
[input]
5
a_opsa_2:51
like_Replay_3:15
c_tigre_4:21
Ceca_Trepni_3:58
ban_Photoshop_3:48
all
[/input]
[output]
opsa
Replay
tigre
Trepni
Photoshop
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
