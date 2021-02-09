# Programmability

[slide hideTitle]

# Indexes

A database index is a data structure that improves the speed of operations in a table.

Indexes can be created using one or more columns, providing the basis for both rapid random lookups and efficient ordering of access to records.

While creating an index, it should be taken into consideration which of the columns will be used to make SQL queries and create one or more indexes on those columns.

There are two types of indexes: **Clustered** and **Non-Clustered**.

**Clustered** indexes are bound to the **primary key** and are used to physically sort data.

**Non-Clustered** indexes can be bound to any field, and they are used to reference the primary index.

[image assetsSrc="Introduction-To-Databases(12).png" /]

[/slide]

[slide hideTitle]

# Views

Views are prepared queries for displaying sections of our data. 

Use the `CREATE VIEW` statement to create a new view.

Once we execute the `CREATE VIEW` statement, MySQL creates the view and stores it in the database so we can use it later if we need it.

Example of create view statement:

```Java
CREATE VIEW v_employee_names AS
	SELECT employee_id,
        first_name,
        last_name
    FROM employees
SELECT * FROM v_employee_names
```

[/slide]

[slide hideTitle]

# Procedures, FunctionsAnd Triggers

A database can be customized, with reusable code, and for this, we can use **Procedures**, **Functions**, and **Triggers**.

A procedure is like a subprogram in a regular scripting language, stored in a database. A MySQL procedure has a **name**, a **parameter list**, and **SQL statement(s)**.

In MySQL, a function is a stored program that you can pass parameters into and then return a value.

A trigger in MySQL is a set of SQL statements that reside in a system catalog. 

It is a special type of stored procedure that is invoked automatically in response to an event. 

Each trigger is associated with a table, which is activated on any DML statement such as **INSERT**, **UPDATE**, or **DELETE**.

[/slide]