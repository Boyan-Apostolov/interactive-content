# Statements
[slide hideTitle]

# Statement Тypes

[video src="https://videos.softuni.org/hls/Java/Java-ORM-and-Spring-Data/01.Data-Database-Access-With-JDBC/01-Data-Database-Access-With-JDBC-23-25-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Once we obtain the connection, it is time to **interact** with the database. 

As we mentioned the JDBC API provides you with **several interfaces** and classes.

The interfaces used to interact with the database and send statements to it are "**Statement, PreparedStatement, CallableStatement**".

These interfaces provide you with the methods and properties used to send SQL statements to the database and receive information from it.

Each of the interfaces is used on a different occasion, now let us have a look at each one of them, learn what they are used for, and have some examples. 

## Statement
We use this interface for general-purpose access to our database. 

It is useful when we are using static SQL statements at runtime as this interface **cannot** accept parameters.

**Example**

```java
Statement stmt = 
connection.createStatement("UPDATE Employees set age=30 WHERE id=101");
Boolean ret = stmt.execute(sql);

System.out.prinln("Is employee updated = " + ret.toString())
```

## Statements Example

### PreparedStatement

This interface is used when you intend to call a given statement several times. 

This interface **can accept** parameters.

**Example**

```java
PreparedStatement stmt = 
connection.prepareStatement("SELECT * FROM employees WHERE salary > ?");

String salary = sc.nextLine();
stmt.setDouble(1, Double.parseDouble(salary));

```

### CallableStatement
We use this statement when we need to access the database's stored procedures. 

This method **does accept** parameters.

## Example
```java
//Stored Procedure
DELIMITER //

CREATE PROCEDURE `GetAllEmployeesById` 
   (IN EMP_ID INT)
BEGIN
   SELECT * 
   FROM Employees as e
   WHERE e.ID = EMP_ID;
END //

DELIMITER

//Call with JAVA
String sql =  "{CALL GetAllEmployeesWithName(?)}";
CallableStatement stmt = con.prepareCall(sql);

int employeeId = 101;
stmt.setInt(1, employeeId);
stmt.execute();
```

[/slide]