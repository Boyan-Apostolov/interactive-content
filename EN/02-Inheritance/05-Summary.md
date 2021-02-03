[slide hideTitle]
# Summary

## In this lesson you learnt:

- Inheritance is a powerful tool for **code reuse**

```java
class Person { … }

class Student extends Person { … }
class Employee extends Person { … }
```

- **Subclass inherits** members from **Superclass**

```java
class Person { … } // BaseClass/ParentClass

class Student extends Person { … }  //SubClass/Child
class Employee extends Person { … } //SubClass/Child
```

- Subclass can **override** methods

```java
public class Person {  
  public void sleep() { 
	System.out.println("Person sleeping"); } 
}

public class Student extends Person {
  @Override 
  public void sleep(){
	System.out.println("Student sleeping"); }
}
```

- Look for classes with the **same role**

- Look for **IS-A** and **IS-A-SUBSTITUT**E for relationship

- Consider **Composition** and **Delegation** instead


## In the next lesson we will learn:


- What are Inheritance and Interfaces

- Abstraction as an OOP Principle

- How to use Interfaces

- What are Abstract Classes

- Interfaces vs Abstract Classes

[/slide]