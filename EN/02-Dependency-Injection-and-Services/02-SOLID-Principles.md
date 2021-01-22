# SOLID Principles

[slide hideTitle]

# Single Responsibility Principle

## SOLID Overview

The **SOLID** principles, introduced by American software engineer and instructor **Robert Cecil Martin** are the five most important principles in **object-oriented programming**.

**SOLID** is an acronym for:

- **S**: Single responsibility principle;
- **O**: Open-closed principle;
- **L**: Liskov substitution principle;
- **I**: Interface segregation principle;
- **D**: Dependency inversion principle.

The SOLID principles form a core **philosophy** for methodologies such as **agile** and **adaptive** software development.

When **combined**, these principles make our applications easier to **maintain** and **extend**.

## What is the Single Responsibility Principle?

The Single Responsibility Principle is the first **SOLID** principle.

It states that **every class** should have **responsibility** over **only one** part of a program's functionality.

In other words, a class should have one, and **only one**, reason to change.

When applied, this principle leads to better **logical grouping**, which in turn makes the intentions of your code **clearer** and **maintenance** easier.


[/slide]

[slide hideTitle]

# Open-Closed Principle

The **Open-Closed Principle** states that a class, module or function should be **open for extension**, but **closed for modification**.

What this means is that as soon as a given **software entity** is **in use** by clients, you **should not change its behavior**. 

However, it should be possible to **extend** it as long as adding new functionality **does not require changes** in the already established codebase.

**Bug fixes** are an **exception** of this rule and you are **allowed** to **modify** the source code directly for debugging purposes.

By following the Open-Closed Principle, a component is more likely to contain **maintainable** and **reusable code**.

If you decide to **break** this principle and modify a  functionality that is already deployed and is being used by clients, this change can have a **profound impact** on the application and its users.

[/slide]

[slide hideTitle]

# Liskov Substitution Principle

Introduced by Barbara Liskov in 1987, the **Liskov substitution principle** states that **child classes** should **never break** the **parent class' type definitions**.

In simple terms, derived types must be **completely substitutable** for their base types.

Derived classes that follow this rule only **extend** the functionality of the base class.

Child classes also **must not remove** the behavior of their **parent class**.

[/slide]

[slide hideTitle]

# Interface Segregation Principle

The **Interface Segregation Principle**, abbreviated as \(ISP\), states that clients **should not** be forced to depend on **methods they do not use**.

The main objective of ISP is to split the so\-called **"fat" interfaces** that are very large, into smaller and more specific **"role" interfaces**.
 
By doing so, **clients** will only have to know about the **methods** that are of interest to **them**.

The main intention of ISP is to keep a system **decoupled**, resulting in easier **refactoring**, **modification**, and **redeployment**.

[/slide]

[slide hideTitle]

# Dependency Inversion Principle

The **Dependency Inversion Principle** \(DIP\) states that:

- Both **high** and **low-level modules** should depend on **abstractions**, but high-level modules **should not depend** on low-level modules;
- **Details(concretions)** should **depend** on abstractions, but abstractions should **not depend** on details.

DIP changes the **direction** of the dependency and **splits it** between the high and low levels.

[/slide]

[slide hideTitle]

# Dependency Inversion Principle: Abstractions and Concretions

- **What are Abstractions?**

**Abstraction** is a different word for an **Interface**.

We use **Interfaces** to define what an implementing class **must** include:

```js
interface Person {
    firstName: string,
    lastName: string,
    age: number,
    city: string
}
```

Any class that **implements** the `Person` interface **must include** the four **properties** with their respective **type**:

```js
class Brandon implements Person {
    firstName: string = 'Brandon',
    lastName: string = 'Charles',
    age: number = 29,
    city: string = 'Berlin'
}
```

**Interfaces** are called **Abstractions** because they focus on the **characteristics** of the implementing classes, rather than an individual class' **implementation**.

- **What are Concretions?**

**Concretions** are **Classes**.

Being the opposite of **Abstractions**, they contain the **full implementation** of their **characteristics**.

In the above example, the `Person` interface is an **Abstraction**.

The classes that **implement** it, like `Brandon` for example, are **Concretions**, which means that they contain the **implementation** of the `Person` interface.

[/slide]

[slide hideTitle]

# Dependency Injection

**Dependency Injection** is a popular design pattern and one of Angular's **most important features**.

It allows us to **inject** dependencies, like a **framework** or **database**, in different **components** across our applications.

Also referred to as **Inversion of Control**, Dependency Injection is the practice of separating **configuration** from **implementation**.

A **downside** of dependencies is that they **decrease code reuse**.


[/slide]

[slide hideTitle]

# Dependency Injection: Example

The following code is an example for dependency injection:

```js
private class ManageUsersService {
  constructor({ users }) {
    this.users = users
  }

  async findAllUsers() {
    return this.users.findAllUsers();
  }

  async addNewUser(user) {
    await this.users.addNewUser(user);
    alert('New user added');
  }
}

module.exports = ManageUsersService;

const ManageUsersService = new ManageUsersService({ users });
```

To inject a dependency in a **class**, we use the **constructor**, in which we can pass them as parameters **one by one** or by a single **object**.

[/slide]

[slide hideTitle]

# Classic Violations

You **should not** use the `new` keyword inside the constructor or use **static** methods and properties.


```js
public class Car {
  public engine: Engine;
  public gearbox: Gearbox;

  constructor() {
    this.engine = new Engine('Honda F20C');
    this.gearbox = new Gearbox('NORD 215N');
  }
}
```

This makes your class **brittle**, **inflexible** and **hard to test**.


[/slide]

[slide hideTitle]

# How to Fix?

You should always add dependencies through the **constructor**:

```js
constructor( public engine: Engine, public gearbox: Gearbox)
```

**Do not** create **dependencies** inside the **current** class.

Then, create as many new instances as you like:

```js
let carOne = new Car(  
  new Engine('Audi N392'),  
  new Gearbox('Stober JP34'));

let carTwo = new Car(  
  new Engine('BMW RV371'),  
  new Gearbox('BorgWarner NH83'));

```

[/slide]

[slide hideTitle]

# General Requirements

To conclude, these are the requirements for the DI Pattern:

- Classes should **never** create dependencies themselves
  - They should be received from **external sources**
- You should **decouple** dependencies through constructor injection
- Your code should be **easier to test**

For additional information visit [Angular's documentation](https://angular.io/guide/dependency-injection).

[/slide]