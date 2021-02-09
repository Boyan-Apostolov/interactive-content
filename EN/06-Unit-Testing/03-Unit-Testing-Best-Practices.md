[slide hideTitle]

# Unit-Testing best practices

Here, we will take a look at some good practices in Unit Testing.

`assertEquals(expected, actual)` method gives us better description details when we are working with values than `assertTrue()` method.

For example:

When we use `assertTrue()` method here, we can see less descriptive output:

``` java
Assert.assertTrue(account.getBalance() == 50);
```

Output: 

```
java.lang.AssertionError <3 internal calls>
```

If we use `assertEquals()` method, we will obtain more information:

``` java
Assert.assertEquals(50, account.getBalance());
```

Output: 

```
java.lang.AssertionError:
Expected :50
Actual :35
<Click to see difference>
```


[/slide]

[slide hideTitle]

# Magic Numbers

Other good practice is trying to avoid using "**magic numbers**".

We must use "**constants**" instead.

Lets take this simple example:

``` java
private static final int AMOUNT = 100;
@Test
public void depositShouldAddMoney() {
  BankAccount account = new BankAccount();
  account.deposit(AMOUNT);
  Assert.assertEquals("Wrong balance",    
               AMOUNT, account.getBalance());
}
```

We see here from this example that its better to declare our int variable outside of the test and use it as a constant.

This is better because if we need to change our `amount` variable, we can change it only **outside** of the test and don't worry about the logic inside.

[/slide]

[slide hideTitle]

# Before

When we write tests, its common to find that several tests need similar object to be created before they can run.

We can use `@Before` annotation to create this behavior.

The method with that annotation will be executed each time before running the next test.

This will ensure consistent and clean data for each test, making our tests more reliable.

Lets take a look with this simple example:

``` java
 public class Example {
    HashMap empty;
    @Before
    public void initialize() {
        empty = new HashMap();
    }
    
    @Test public void size() {
      // ... our test logic here
    }
    @Test public void remove() {
       // ... our test logic here
    }
```

That way, our initialize method will execute before each test.


[/slide]

[slide hideTitle]

# Naming Test Methods:

Test naming is very important. Especially for the big long term projects.

There are few recommendations regarding test names:

- Test names should use business domain terminology.

- Test names should be descriptive and readable.

- Our tests should express a specific requirement.

- Some of ours test names could include the name of the tested method or class.

- We must write clean names.

- Do not be afriad to write long names, as long as they need to be to explain the test.

Lets see some examples of **bad** test naming:

```
increaseDMG {}
test1() {}
testTransfer()
idontrememberwhatiamtesting {}
```

Here is some **proper** test naming examples:

```
depositAddsMoneyToBalance() {}
depositNegativeShouldNotAddMoney() {}
transferSubtractsFromSourceAddsToDestAccount() {}
```

[/slide]

[slide hideTitle]

# Problem: Refactor Tests

## Description
Refactor the tests for **Axe** and **Dummy** classes

Make sure that:
- **Names** of test methods are **descriptive**
- You use **appropriate assertions** (assert equals vs assert true)
- You use **assertion messages**
- There are **no magic numbers**
- There is **no code duplication** (Don’t Repeat Yourself)

## Hints

Extract constants and private fields for `Axe` class
```java
private static final int AXE_ATTACK = 10;
private static final int AXE_DURABILITY = 1;
private static final int DUMMY_HEALTH = 20;
private static final int DUMMY_XP = 10;
private static final int EXPECTED_DURABILITY = AXE_DURABILITY - 1;

private Axe axe;
private Dummy dummy;
```

Create a method that executes before each test:
```java
@Before
public void initializeTestObjects(){
  this.axe - new Axe(AXE_ATTACK, AXE_DURABILITY);
  this.dummy = new Dummy(DUMMY_HEALTH, DUMMY_XP);
}
```

Make use of constants and private fields, as well as add assertion messages
```java
@Test
public void weaponAttackLosesDurability(){
  //Act
  this.axe.attack(this.dummy);

  //Assert
  Assert.assertEquals("Wrong Durability, "),
          EXPECTED_DURABILITY,
          this.axe.getDurabilityPoints());
}
```

Follow the same logic for other test methods and `TestDummy` class

[/slide]