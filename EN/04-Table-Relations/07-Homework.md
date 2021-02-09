[slide hideTitle]

# Homework

[/slide]

[slide hideTitle]
# Problem: One-To-One Relationship
[code-task title="Problem: One-To-One Relationship" taskId="27c5e29b-5fb1-475e-bb58-f84ee19f60ed" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

**Here is a link to the** [resources](https://videos.softuni.org/resources/java/java-mysql/05.Table-Relations-Geography-Db-Exercise.zip) **for this task.**

Create two tables as follows. Use appropriate data types.

**Insert the data from the example below.**

•	Alter table **people** and make **person_id** a **primary key**. 

•	Create a **foreign key** between **people** and **passports** by using the **passport_id** column. 

•	Think about which passport field should be **UNIQUE**.

## Examples

**People**

| **person_id** | **first_name** | **salary** | **passport_id** |
| --- | --- | --- | --- |
| 1   | Roberto | 43300.00 | 102 |
| 2 | Tom | 56100.00 | 103 |
| 3 | Yana | 60200.00 | 101 |
|  |  |  |  |

**Passports**

| **passport_id** | **passport_number** |
| --- | --- |
| 101 | N34FG21B |
| 102 | K65LO4R7 |
| 103 | ZE657QP2 |
|  |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
people
first_name
passport_id
person_id
salary
passports
passport_id
passport_number
passports
1
people
1
passport_id
people
passport_id
passports
passport_id
1
Roberto
43300.00
102
102
K65LO4R7
2
Tom
56100.00
103
103
ZE657QP2
3
Yana
60200.00
101
101
N34FG21B
[/input]
[output]
people
first_name
passport_id
person_id
salary
passports
passport_id
passport_number
passports
1
people
1
passport_id
people
passport_id
passports
passport_id
1
Roberto
43300.00
102
102
K65LO4R7
2
Tom
56100.00
103
103
ZE657QP2
3
Yana
60200.00
101
101
N34FG21B
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: One-To-Many Relationship
[code-task title="Problem: One-To-Many Relationship" taskId="a7d399f9-16ab-4018-9b73-4f5076075285" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

**Here is a link to the** [resources](https://videos.softuni.org/resources/java/java-mysql/05.Table-Relations-Geography-Db-Exercise.zip) **for this task.**

Create two tables as follows. Use appropriate data types.

Insert the data from the example below. 

•	Add primary and foreign keys.

Submit your queries by using "**MySQL run queries & check DB**" strategy.


## Examples

**manufacturer**

| **manufacturer_id** | **name** | **established_on** |
| --- | --- |
| 1   | BMW | 01/03/1916 |
| 2 | Tesla | 01/01/2003 |
| 3 | Lada | 01/05/1966 |
|  |  | |

**models**

| **model_id** | **name** | **manufacturer_id** |
| --- | --- |
| 101 | X1 | 1 |
| 102 | i6 | 1 |
| 103 | Model S | 2 |
| 104 | Model X | 2 |
| 105 | Model 3 | 2 |
| 106 | Nova | 3 |
|  |  |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
manufacturers
established_on
manufacturer_id
name
models
manufacturer_id
model_id
name
manufacturers
1
models
1
models
manufacturer_id
1
1
BMW
1916-03-01 00:00:00
101
X1
1
BMW
1916-03-01 00:00:00
102
i6
2
Tesla
2003-01-01 00:00:00
103
Model S
2
Tesla
2003-01-01 00:00:00
104
Model X
2
Tesla
2003-01-01 00:00:00
105
Model 3
3
Lada
1966-05-01 00:00:00
106
Nova
[/input]
[output]
manufacturers
established_on
manufacturer_id
name
models
manufacturer_id
model_id
name
manufacturers
1
models
1
models
manufacturer_id
1
1
BMW
1916-03-01 00:00:00
101
X1
1
BMW
1916-03-01 00:00:00
102
i6
2
Tesla
2003-01-01 00:00:00
103
Model S
2
Tesla
2003-01-01 00:00:00
104
Model X
2
Tesla
2003-01-01 00:00:00
105
Model 3
3
Lada
1966-05-01 00:00:00
106
Nova
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Many-To-Many Relationship
[code-task title="Problem: Many-To-Many Relationship" taskId="8fdeb158-948f-43dd-bd93-7c481485049e" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

**Here is a link to the** [resources](https://videos.softuni.org/resources/java/java-mysql/05.Table-Relations-Geography-Db-Exercise.zip) **for this task.**

Create three tables as follows. Use appropriate data types.

**Insert the data from the example above**.

•	Add primary and foreign keys.

•	Have in mind that the table **student_exams** should have a composite primary key.

Submit your queries by using "**MySQL run queries & check DB**" strategy.
.

## Examples

**students**

| **student_id** | **name** |
| --- | --- |
| 1   | Mila |
| 2 | Toni |
| 3 | Ron |
|  |  |

**exams**

| **exam_id** | **name** |
| --- | --- |
| 101 | Spring MVC |
| 102 | Neo4j |
| 103 | Oracle 11g |
|  |  |

**students_exams**

| **student_id** | **exam_id** |
| --- | --- |
| 1 | 101 |
| 1 | 102 |
| 2 | 101 |
| 3 | 103 |
| 2 | 102 |
| 2 | 103 |
|  |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
students
name
student_id
exams
exam_id
name
students_exams
exam_id
student_id
student_id
exam_id
students_exams
student_id
students
student_id
students_exams
exam_id
exams
exam_id
1
Mila
1
101
101
Spring MVC
1
Mila
1
102
102
Neo4j
2
Toni
2
101
101
Spring MVC
2
Toni
2
102
102
Neo4j
2
Toni
2
103
103
Oracle 11g
3
Ron
3
103
103
Oracle 11g
[/input]
[output]
students
name
student_id
exams
exam_id
name
students_exams
exam_id
student_id
student_id
exam_id
students_exams
student_id
students
student_id
students_exams
exam_id
exams
exam_id
1
Mila
1
101
101
Spring MVC
1
Mila
1
102
102
Neo4j
2
Toni
2
101
101
Spring MVC
2
Toni
2
102
102
Neo4j
2
Toni
2
103
103
Oracle 11g
3
Ron
3
103
103
Oracle 11g
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Self-Referencing
[code-task title="Problem: Self-Referencing" taskId="8c60b62a-5656-4d77-a686-10ef21c87e57" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

**Here is a link to the** [resources](https://videos.softuni.org/resources/java/java-mysql/05.Table-Relations-Geography-Db-Exercise.zip) **for this task.**

Create a single table as follows. Use appropriate data types.

**Insert the data from the example above**.

•	Add primary and foreign keys. 

•	The foreign key should be between **manager_id** and **teacher_id**.

Submit your queries by using "**MySQL run queries & check DB" strategy**.

## Examples

**Teachers**

| **teacher_id** | **name** | **manager_id** |
| --- | --- |
| 101 | John |
| 102 | Maya | 106 |
| 103 | Silvia | 106 |
| 104 | Ted | 105 |
| 105 | Mark | 101 |
| 106 | Greta | 101 |
|  |  |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
teachers
manager_id
name
teacher_id
teacher_id
teachers
manager_id
teachers
teacher_id
101
John

102
Maya
106
103
Silvia
106
104
Ted
105
105
Mark
101
106
Greta
101
[/input]
[output]
teachers
manager_id
name
teacher_id
teacher_id
teachers
manager_id
teachers
teacher_id
101
John

102
Maya
106
103
Silvia
106
104
Ted
105
105
Mark
101
106
Greta
101
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Online Store Database
[code-task title="Problem: Online Store Database" taskId="5311ac44-15d7-4e0b-a4dd-26852366f9a3" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

**Here is a link to the** [resources](https://videos.softuni.org/resources/java/java-mysql/05.Table-Relations-Geography-Db-Exercise.zip) **for this task.**

Create a new database and design the following structure:

Submit your queries by using "**MySQL run queries & check DB" strategy**".

[image assetsSrc="Table-Relations-Homework.png" /]


[/task-description]
[code-io /]
[tests]
[test open]
[input]
orders
customer_id
int
order_id
int
order_id
customers
birthday
date
city_id
int
customer_id
int
name
varchar(50)
customer_id
cities
city_id
int
name
varchar(50)
city_id
items
item_id
int
item_type_id
int
name
varchar(50)
item_id
item_types
item_type_id
int
name
varchar(50)
item_type_id
order_items
item_id
int
order_id
int
item_id
order_id
customers
city_id
cities
city_id
items
item_type_id
item_types
item_type_id
order_items
item_id
items
item_id
order_items
order_id
orders
order_id
orders
customer_id
customers
customer_id
[/input]
[output]
orders
customer_id
int
order_id
int
order_id
customers
birthday
date
city_id
int
customer_id
int
name
varchar(50)
customer_id
cities
city_id
int
name
varchar(50)
city_id
items
item_id
int
item_type_id
int
name
varchar(50)
item_id
item_types
item_type_id
int
name
varchar(50)
item_type_id
order_items
item_id
int
order_id
int
item_id
order_id
customers
city_id
cities
city_id
items
item_type_id
item_types
item_type_id
order_items
item_id
items
item_id
order_items
order_id
orders
order_id
orders
customer_id
customers
customer_id
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Problem: Peaks in Rila
[code-task title="Problem: Peaks in Rila" taskId="67b6ba43-c2c6-4d77-ae2e-9a594b867a9c" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

**Here is a link to the** [resources](https://videos.softuni.org/resources/java/java-mysql/05.Table-Relations-Geography-Db-Exercise.zip) **for this task.**

Display all peaks for "**Rila**" **mountain_range**. Include:

•	**mountain_range**

•	**peak_name**

•	**peak_elevation**

Peaks should be sorted by **peak_elevation** descending.

Submit your queries by using "**MySQL prepare DB & run queries**" strategy.

## Examples
| **mountain_range** | **peak_name** | **peak_elevation** |
| --- | --- |
| Rila | Musala | 2925 |
| … | … | … |
|  |  |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Rila
Musala
2925
Rila
Malka Musala
2902
Rila
Malyovitsa
2729
Rila
Orlovets
2685
[/input]
[output]
Rila
Musala
2925
Rila
Malka Musala
2902
Rila
Malyovitsa
2729
Rila
Orlovets
2685
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide hideTitle]
# Homework Results
[tasks-results/]

[/slide]
