[slide hideTitle]
# Using Inherited Members

**You can access inherited members**

As we mention we can access the inherited members, we do it as we normally call class members.

Create an object of the derived class and when we call it we can access all **non-private** members derived or declared.

```java
class Person { public void sleep() { … } }
class Student extends Person { … }
class Employee extends Person { … }
```
```java
Student student = new Student();
student.sleep();
Employee employee = new Employee();
employee.sleep();
```

We can also hold a reference to an object of the derived class in the base class variable.

```java
Person student = new Student(); // The baseclass variable holds the object of the Subclass type.
Person employee = new Employee();
```

What changes here is that we will only have access to the base class members, as we use the `Student` as a `Person`;

[/slide]

[slide hideTitle]

# Reusing Constructors

**Constructors are not inherited**

When a **parent class** declares a **constructor** with parameters everybody that inherits from this class must fulfill the **Parent class's** constructor.

Because the base constructor gets called automatically when the derived class is created.

The parameter from the **constructor** of the derived class must be passed to the parent **constructor** with the keyword super.

Here is an example of a constructor chaining.

```java
class Person{
    private String name;
    // If we don't have parameterized constructor in the parent class, we can skip calling it in the Subclass.
    public Person(String name){
        this.name = name;
    }
}

class Student extends Person {
  private School school;
  public Student(String name, School school) {  // If we don't call our Superclass's constructor a compile-time error will be thrown.
    super(name); //Best practises says that constructor call should be called first
    this.school = school;
  }

//You can also fulfill the parent constructor with some default values, just like this.
  public Student(School school){ 
      String defaultName = "John Doe";
      super(defaultName);
      this.school = school;
  }

}

```
[/slide]

[slide hideTitle]

# Thinking about Inheritance – Extends

What happens with the memory when a class **inherits** another one.

As you can see in the image below, when we inherit, the memory for the **Parent** is allocated plus the new needed memory for the **Derived class**.

That is because all the members of the **Parent** are declared as well as all the new members from the **Derived class**.

[image assetsSrc="inheritance-example(6).png" /]

[/slide]

[slide hideTitle]

# Inheritance has a transitive relation

```java
class Person { … }                              //Base class with some functionallity.
class Student extends Person { … }              //Student will get all the functionallity from Person and add more to it.
class CollegeStudent extends Student { … }      //CollegeStudent will inherit all the functionallity from Student and from Person.
```

That's what transitive relation is, a **Subclass** gets all the functionality from it is Superclasses up the hierarchy.

[image assetsSrc="inheritance-example(7).png" /]

[/slide]

[slide hideTitle]
# Multiple Inheritance

**In Java multiple inheritances is now allowed**

Instead, if you need one class to be from few families you can implement many **interfaces** on a single class.

**Interfaces** will be covered further in our lessons.

[image assetsSrc="inheritance-example(8).png" /]

[/slide]

[slide hideTitle]
# Access to Base Class Members

Sometimes we need to access the base class members.

To access the base class members, use the `super` keyword.

We can also re-use some of the logic.

Example:

```java
class Person {
    protected String name;
    
    public Person(String name){
        this.name = name;
    }
 }

class Employee extends Person { 
  public void fire(String reasons) { 
    System.out.println(
        super.name +                        //We use the `super` keyword to access the Superclass/Inherited class members.
        " got fired because " + reasons);
  }
}
```
[/slide]

[slide hideTitle]
# Problem: Multiple Inheritance
[code-task title="Multiple Inheritance" taskId="5cf868e8-02f2-4b35-9377-f7b81085064e" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create three classes named **Animal, Dog** and **Puppy**. 

**Animal** with a single public method `.eat()` that prints: **"eating…"**.

**Dog** with a single public method `.bark()` that prints: **"barking…"**.

Puppy with a single public method weep() that prints: **"weeping…"**.

**Dog** should inherit from **Animal**. **Puppy** should inherit from **Dog**. 

[image assetsSrc="inheritance-example(10).png" /]

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

public class TestPuppy \{
    @Test
    public void testPuppyClass() \{
        Assert.assertTrue("Class 'Puppy' not found", Classes.allClasses.containsKey("Puppy"));

        Class puppy = Classes.allClasses.get("Puppy");
        Method\[\] methods = puppy.getDeclaredMethods();
        Optional\<Method\> weepMethod = Stream.of(methods).filter(m -\> m.getName().equals("weep")).findFirst();
        Assert.assertTrue("Method 'weep' not found", weepMethod.isPresent());
        Assert.assertTrue("Method 'weep' has incorrect return type", weepMethod.get().getReturnType().equals(Void.TYPE));
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

public class TestSuperclass \{
    @Test
    public void testDogParent() \{
        Assert.assertTrue("Class 'Puppy' not found", Classes.allClasses.containsKey("Puppy"));

        Class puppy = Classes.allClasses.get("Puppy");

        Class dog = puppy.getSuperclass();
        Assert.assertTrue("Class 'Puppy' should inherit from class 'Dog'", dog.getSimpleName().equals("Dog"));

        Class animal = dog.getSuperclass();
        Assert.assertTrue("Class 'Dog' should inherit from class 'Animal'", animal.getSimpleName().equals("Animal"));
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
# Solution: Multiple Inheritance
[code-task title="Multiple Inheritance" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create three classes named **Animal, Dog** and **Puppy**. 

**Animal** with a single public method `.eat()` that prints: **"eating…"**.

**Dog** with a single public method `.bark()` that prints: **"barking…"**.

Puppy with a single public method weep() that prints: **"weeping…"**.

**Dog** should inherit from **Animal**. **Puppy** should inherit from **Dog**. 

[image assetsSrc="inheritance-example(10).png" /]

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

public class TestPuppy \{
    @Test
    public void testPuppyClass() \{
        Assert.assertTrue("Class 'Puppy' not found", Classes.allClasses.containsKey("Puppy"));

        Class puppy = Classes.allClasses.get("Puppy");
        Method\[\] methods = puppy.getDeclaredMethods();
        Optional\<Method\> weepMethod = Stream.of(methods).filter(m -\> m.getName().equals("weep")).findFirst();
        Assert.assertTrue("Method 'weep' not found", weepMethod.isPresent());
        Assert.assertTrue("Method 'weep' has incorrect return type", weepMethod.get().getReturnType().equals(Void.TYPE));
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

public class TestSuperclass \{
    @Test
    public void testDogParent() \{
        Assert.assertTrue("Class 'Puppy' not found", Classes.allClasses.containsKey("Puppy"));

        Class puppy = Classes.allClasses.get("Puppy");

        Class dog = puppy.getSuperclass();
        Assert.assertTrue("Class 'Puppy' should inherit from class 'Dog'", dog.getSimpleName().equals("Dog"));

        Class animal = dog.getSuperclass();
        Assert.assertTrue("Class 'Dog' should inherit from class 'Animal'", animal.getSimpleName().equals("Animal"));
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
# Problem: Hierarchical Inheritance
[code-task title="Hierarchical Inheritance" taskId="8688e808-529e-4532-be86-b62a8cdc42fc" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create three classes named **Animal**, **Dog** and **Cat**. 

**Animal** with a single public method `.eat()` that prints: **"eating…"**

**Dog** with a single public method `.bark()` that prints: **"barking…"**

**Cat** with a single public method `.meow()` that prints: **"meowing…"**

**Dog** and **Cat** should inherit from **Animal**.

[image assetsSrc="inheritance-example(11).png" /]

[/task-description]
[code-io /]
[tests]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

public class TestCatParent \{

    @Test
    public void testCatParent() \{
        Assert.assertTrue("Class 'Cat' not found", Classes.allClasses.containsKey("Cat"));
        Class cat = Classes.allClasses.get("Cat");
        Class catParent = cat.getSuperclass();
        Assert.assertTrue("Class 'Cat' should inherit from class 'Animal'", catParent.getSimpleName().equals("Animal"));
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

public class TestDogParent \{

    @Test
    public void testCatParent() \{
        Assert.assertTrue("Class 'Dog' not found", Classes.allClasses.containsKey("Dog"));
        Class dog = Classes.allClasses.get("Dog");
        Class dogParent = dog.getSuperclass();
        Assert.assertTrue("Class 'Dog' should inherit from class 'Animal'", dogParent.getSimpleName().equals("Animal"));
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
# Solution: Hierarchical Inheritance
[code-task title="Hierarchical Inheritance" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create three classes named **Animal**, **Dog** and **Cat**. 

**Animal** with a single public method `.eat()` that prints: **"eating…"**

**Dog** with a single public method `.bark()` that prints: **"barking…"**

**Cat** with a single public method `.meow()` that prints: **"meowing…"**

**Dog** and **Cat** should inherit from **Animal**.

[image assetsSrc="inheritance-example(11).png" /]

[/task-description]
[code-io /]
[tests]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

public class TestCatParent \{

    @Test
    public void testCatParent() \{
        Assert.assertTrue("Class 'Cat' not found", Classes.allClasses.containsKey("Cat"));
        Class cat = Classes.allClasses.get("Cat");
        Class catParent = cat.getSuperclass();
        Assert.assertTrue("Class 'Cat' should inherit from class 'Animal'", catParent.getSimpleName().equals("Animal"));
    \}
\}
[/input]
[output]
Test Passed!
[/output]
[/test]
[test]
[input]
import org.junit.Assert;
import org.junit.Test;

public class TestDogParent \{

    @Test
    public void testCatParent() \{
        Assert.assertTrue("Class 'Dog' not found", Classes.allClasses.containsKey("Dog"));
        Class dog = Classes.allClasses.get("Dog");
        Class dogParent = dog.getSuperclass();
        Assert.assertTrue("Class 'Dog' should inherit from class 'Animal'", dogParent.getSimpleName().equals("Animal"));
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





