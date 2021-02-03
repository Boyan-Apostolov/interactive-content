# Reusing Classes

[slide hideTitle]
# Access Modifiers and Shadowing Variables

- Derived classes **can access all public** and **protected** members
- Derived classes can access **default** members **if in same package**
- **Private** fields **aren't inherited** in subclasses (can not be accesssed)

```java
class Person {
  protected String address;
  public void sleep();
  String name; //Can be accessed through other methods
  private String id;
}
```

## Shadowing Variables

- Derived classes **can hide** superclass variables

```java
class Person { protected int weight; }

class Patient extends Person {
  protected float weight; //hides int weight
  public void method() {
    double weight = 0.5d; //hides both
  }
}
```

[/slide]

[slide hideTitle]

# Shadowing Variables – Access

- Use **super** and **this** to specify member access

```java
class Person { protected int weight; }

class Patient extends Person {
  protected float weight;
  public void method() {
    double weight = 0.5d; //Local variable
    this.weight = 0.6f; //Instance member
    super.weight = 1; //Base class member
  }
}

```
[/slide]

[slide hideTitle]
# Overriding Derived Methods

Overriding is a mechanism in which we can give custom implementation of a given class method down the hierarchy, we can achieve it with the keyword `@Override`.

It's an imporant tool as it is connected to another pillar of the OOP **Polymorphism**.


```java
public class Person {  
  public void sleep() { 
	System.out.println("Person sleeping"); } 
}
```
- A method that we want to override should not be set as `final`

```java
public class Student extends Person {
  @Override 
  public void sleep(){
	System.out.println("Student sleeping"); }
}
```
- Signature and return type **should match**

[/slide]

[slide hideTitle]

# Final Methods and Classes

- `final` – defines a method that **can not be overridden**.
  We should use this tool when we want to preserve our method implementation down the class hierarchy.
  `final` can be declared in any derived class and it gets in power for the classes children down the hierarchy.

```java
public class Animal {
  public final void eat() { … }
}

public class Dog extends Animal { 
  
  @Override
  public void eat() {} // Error…
}
```

- **Inheriting from a final classes is forbidden**

```java
public final class Animal {
  …
}

public class Dog extends Animal { }      // Error…
public class MyString extends String { } // Error…
public class MyMath extends Math { }     // Error…
```

[/slide]

[slide hideTitle]

# Inheritance Benefits 

## Abstraction

- With inheritance we can provide abstraction to the classes we use.
- We can re-use logic, less code means less bugs.
- We can achieve **Polymorphism**

```java
Person person = new Person();
Student student = new Student();

List<Person> people = new ArrayList();

people.add(person);
people.add(student);
```

[image assetsSrc="inheritance-example(13).png" /]

## Extension

- We can extend a class that we can't otherwise change, implementing the custom logic we need.

[image assetsSrc="inheritance-example(14).png" /]

[/slide]

[slide hideTitle]
# Problem: Random Array List
[code-task title="Random Array List" taskId="a002eea4-0c9f-4728-bb88-a7e24ab26a52" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description

Create a **RandomArrayList** class that has all the functionality of an **ArrayList**.

Add additional function that **returns** and **removes** a random element from the list.

- Public method: **getRandomElement(): Object**


[/task-description]
[code-io /]
[tests]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

import java.lang.reflect.Method;
import java.util.Optional;
import java.util.stream.Stream;

public class TestRandomArrayList \{
    private static final String RANDOM_ARRAY_LIST_CLASS_NAME = "RandomArrayList";
    private static final String ARRAY_LIST_CLASS_NAME = "ArrayList";
    private static final String GET_RND_ELEMENT_METHOD_NAME = "getRandomElement";

    @Test
    public void testRandomArrayList() \{

        Assert.assertTrue("Class 'RandomArrayList' not found", Classes.allClasses.containsKey(RANDOM_ARRAY_LIST_CLASS_NAME));
        Class ral = Classes.allClasses.get(RANDOM_ARRAY_LIST_CLASS_NAME);
        Class ralBase = ral.getSuperclass();
        Assert.assertTrue("Class 'RandomArrayList' should extend 'ArrayList'", ralBase.getSimpleName().equals(ARRAY_LIST_CLASS_NAME));

        Method\[\] methods = ral.getDeclaredMethods();
        Assert.assertTrue("Method 'getRandomElement()' not present", isMethodPresent(methods, GET_RND_ELEMENT_METHOD_NAME));
    \}

    private boolean isMethodPresent(Method\[\] methods, String name) \{
        Optional\<Method\> method =  Stream.of(methods)
                .filter(m -\> m.getName().equals(name))
                .findFirst();

        return method.isPresent();
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Solution: Random Array List
[code-task title="Random Array List" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description

Create a **RandomArrayList** class that has all the functionality of an **ArrayList**.

Add additional function that **returns** and **removes** a random element from the list.

- Public method: **getRandomElement(): Object**


[/task-description]
[code-io /]
[tests]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

import java.lang.reflect.Method;
import java.util.Optional;
import java.util.stream.Stream;

public class TestRandomArrayList \{
    private static final String RANDOM_ARRAY_LIST_CLASS_NAME = "RandomArrayList";
    private static final String ARRAY_LIST_CLASS_NAME = "ArrayList";
    private static final String GET_RND_ELEMENT_METHOD_NAME = "getRandomElement";

    @Test
    public void testRandomArrayList() \{

        Assert.assertTrue("Class 'RandomArrayList' not found", Classes.allClasses.containsKey(RANDOM_ARRAY_LIST_CLASS_NAME));
        Class ral = Classes.allClasses.get(RANDOM_ARRAY_LIST_CLASS_NAME);
        Class ralBase = ral.getSuperclass();
        Assert.assertTrue("Class 'RandomArrayList' should extend 'ArrayList'", ralBase.getSimpleName().equals(ARRAY_LIST_CLASS_NAME));

        Method\[\] methods = ral.getDeclaredMethods();
        Assert.assertTrue("Method 'getRandomElement()' not present", isMethodPresent(methods, GET_RND_ELEMENT_METHOD_NAME));
    \}

    private boolean isMethodPresent(Method\[\] methods, String name) \{
        Optional\<Method\> method =  Stream.of(methods)
                .filter(m -\> m.getName().equals(name))
                .findFirst();

        return method.isPresent();
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
