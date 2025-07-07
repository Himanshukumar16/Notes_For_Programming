```
                MySql
```
1) Database :-> A database in MySQL is a collection of tables, views, procedures, triggers, and other objects that work together to store and manage data.
it consists of many tables. tables consist of rows and columns.

2) SQL :-> SQL is programming language used to interact with relational databases. it helps in create , read, update, delete data...It is not a case sensitive small likho ya capital sab same !

3) creating a database :-> ```CREATE DATBASE dtabaseName;```
```
   mysql> CREATE DATABASE practice;
   Query OK, 1 row affected (0.01 sec)

	or
  mysql> create database if not exists databaseName; preferred
```
5) delete a database :-> ```drop database databaseName;``` same we can do with tables. as drop table.
```
   mysql> drop Database Practice;
   Query OK, 0 rows affected (0.01 sec)

	or

  mysql> drop database if exists databaseName; preferred
```
7) to use database :-> ```use databaseName```
```
   mysql> use practice;
   Database changed
```
9) to create table for using :-> ```create table tableName(columnName 1 datatype,columnName 2 datatype,columnName 3 datatype);```
```
mysql> create table student(id int primary key,name varchar(50),age int not null);
Query OK, 0 rows affected (0.07 sec)
```
10) to see the tables in database :->```show tables;```
```
    mysql> show tables;
+--------------------+
| Tables_in_practice |
+--------------------+
| student            |
+--------------------+
1 row in set (0.01 sec)
```
11) Add values in table :-> ```insert into tableName values(id,name,age);```
```
mysql> insert into student values(1,"Himanshu",50);// generally used for adding one value to table.
Query OK, 1 row affected (0.02 sec)

or

mysql> insert into student(id,name,age) values(4,"chootu",18); // generally used for adding mulitple value to table.
Query OK, 1 row affected (0.02 sec)
```
12) SQL Datatypes :-> 

Numerical Datatypes:

| Datatype       | Description                  | Example                      |
| -------------- | ---------------------------- | ---------------------------- |
| `INT`          | Integer number               | `5`, `-20`                   |
| `BIGINT`       | Large integer                | `9876543210`                 |
| `FLOAT`        | Floating point (approximate) | `3.14`                       |
| `DOUBLE`       | Double precision float       | `2.718281828`                |
| `DECIMAL(M,D)` | Fixed point, precise         | `DECIMAL(10,2)` → `12345.67` |

String / Text Data Types

| Datatype     | Description                 | Example                          |
| ------------ | --------------------------- | -------------------------------- |
| `CHAR(n)`    | Fixed-length string         | `CHAR(5)` → `'abc  '`            |
| `VARCHAR(n)` | Variable-length string      | `VARCHAR(50)` → `'hello world'`  |
| `TEXT`       | Large text block            | Long article                     |
| `ENUM`       | One value from a list       | `'small'`, `'medium'`, `'large'` |
| `SET`        | Multiple values from a list | `'red,blue'`                     |

date and time datatypes

| Datatype    | Description                  | Example                 |
| ----------- | ---------------------------- | ----------------------- |
| `DATE`      | Date only                    | `'2025-07-07'`          |
| `TIME`      | Time only                    | `'14:30:00'`            |
| `DATETIME`  | Date and time                | `'2025-07-07 14:30:00'` |
| `TIMESTAMP` | Date and time (auto updates) | `'2025-07-07 14:30:00'` |
| `YEAR`      | Year only                    | `2025`                  |

Binary Data Types

| Datatype       | Description                         | Example         |
| -------------- | ----------------------------------- | --------------- |
| `BLOB`         | Binary Large Object (images, files) | Image file      |
| `VARBINARY(n)` | Variable-length binary              | Raw binary data |

13) types of SQL commands :-> 

| Category | Example Commands                             |
| -------- | -------------------------------------------- |
| DDL      | CREATE, ALTER, DROP, TRUNCATE, RENAME        |
| DML      | INSERT, UPDATE, DELETE                       |
| DQL      | SELECT                                       |
| DCL      | GRANT, REVOKE                                |
| TCL      | COMMIT, ROLLBACK, SAVEPOINT, SET TRANSACTION |

14) printing whole table :->```select * from tableName;``` this will print whole table . 
```
    mysql> select * from student;
+----+----------+-----+
| id | name     | age |
+----+----------+-----+
|  1 | Himanshu |  50 |
|  2 | Anurag   |  21 |
|  3 | Ritika   |  19 |
+----+----------+-----+
3 rows in set (0.00 sec)
```
15) to show table's all aspect :-> ``` desc info;  or describe info;```
```
mysql> describe info;
+--------+-------------+------+-----+---------+-------+
| Field  | Type        | Null | Key | Default | Extra |
+--------+-------------+------+-----+---------+-------+
| id     | int         | YES  |     | NULL    |       |
| name   | varchar(50) | YES  |     | NULL    |       |
| salary | int         | YES  |     | NULL    |       |
+--------+-------------+------+-----+---------+-------+
3 rows in set (0.01 sec)

or

mysql> desc info;
+--------+-------------+------+-----+---------+-------+
| Field  | Type        | Null | Key | Default | Extra |
+--------+-------------+------+-----+---------+-------+
| id     | int         | YES  |     | NULL    |       |
| name   | varchar(50) | YES  |     | NULL    |       |
| salary | int         | YES  |     | NULL    |       |
+--------+-------------+------+-----+---------+-------+
3 rows in set (0.00 sec)
```
16) Keys :-> Primary key and foreign Key
Primary key :- A Primary Key is a column (or combination of columns) in a table that uniquely identifies each row.
Key points:
	Must be unique — no two rows can have the same primary key value.
	Cannot be NULL — every row must have a valid primary key value.
	A table can have only one primary key, but it can be made of multiple columns (called a composite key).

foreign key :- A Foreign Key is a column (or columns) that creates a link between two tables. It points to the primary key (or unique key) in another table.
Key points:
	A foreign key value must match a value in the referenced table’s primary key (or be NULL).
	Used to create relationships between tables.
 	declaring foreign key.:- FOREIGN KEY (iss_table_main_kon_hai) REFERENCES DushraTableName(dushreTableKaForeignKeyName);
 ```
CREATE TABLE enrollments (
  enrollment_id INT PRIMARY KEY,
  student_id INT,
  FOREIGN KEY (student_id) REFERENCES students(student_id)
);
```
we can declare primary key in 2 ways:
```
enrollment_id INT PRIMARY KEY,
  student_id INT,
  FOREIGN KEY (student_id) REFERENCES students(student_id)

or

enrollment_id INT ,
  student_id INT,
  FOREIGN KEY (student_id) REFERENCES students(student_id); // declaring foreign key.
  Primary key(enrollment_id)

```
| Feature          | Primary Key                                   | Foreign Key                                 |
| ---------------- | --------------------------------------------- | ------------------------------------------- |
| Purpose          | Uniquely identifies each row in its own table | Links two tables together                   |
| Unique           | Must be unique                                | Can have duplicate values                   |
| NULL allowed?    | No                                            | Yes (unless `NOT NULL` constraint is added) |
| Number per table | One primary key                               | Can have multiple foreign keys              |

17) SQL Constraints :->

| Constraint          | What it does                                                              |
| ------------------- | ------------------------------------------------------------------------- |
| **PRIMARY KEY**     | Uniquely identifies each row. Cannot be NULL.                             |
| **FOREIGN KEY**     | Links two tables to enforce referential integrity.                        |
| **NOT NULL**        | The column **must** have a value (can’t be empty).                        |
| **UNIQUE**          | All values in the column must be unique (no duplicates).                  |
| **CHECK**           | Ensures that values meet a specific condition.                            |
| **DEFAULT**         | Sets a default value if no value is given.                                |
| **AUTO\_INCREMENT** | Automatically increases numeric values (commonly used with primary keys). |

17) Distinct keyword :->```mysql> select distinct name from students;```
    give distinct name from students table.

18) applying condition in select :-> ```mysql> select roll_no from students where name = "Himanshu";```
    we use where clause to filter the table content.

