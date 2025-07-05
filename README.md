# SQL-Database-
# MySql

# Installation
Click on the URL It will redirect to MY SQL -> download page

[https://www.oracle.com/mysql/technologies/mysql-enterprise-edition-downloads.html#windows
](https://dev.mysql.com/downloads/file/?id=541636)

To install my sql we need to login to oracle account.

1. Provide all the required details.

2. create account.

3. Install My sql.


After installation:

type for MySql bench in search bar connect to the local database connection.

Ready to code!!

# Database

A database is an organized collection of data stored electronically. It allows users and applications to easily access, update, and manipulate information. This data contains text, numbers, images, videos and more. Databases are managed using specialized software known as a Database Management System (DBMS), which facilitates the storage, retrieval, and manipulation of data.

# Table

In a database, a table is a structured collection of data organized into rows and columns. 

# Schema
A schema specifies the names of tables, the attributes (fields or columns) within each table, and the data types of those attributes (e.g., text, number, date). Think of it as a blueprint of the table.

# create database in SQL:

```sql
create database sql_class
```

# Datatypes
1.chr()
2.varChr()
3.float()
4.Double()
5.int()
6.BigInt()
7.Date()
8.DateTime()

# create a table in SQL:

```sql
CreaTe table Test(ID int(5),name char(5),height float(5,4));



```

# To show commands in a database

```sql
show tables;
```
# insert data in table:

```sql
Insert into test(ID,name) values(1,'sandy');
```

# display all data in table

```sql
select * from test;
```

# Today's Code july 5th
```sql
--Didn't need to add database since using online compiler
create table drive(name varchar(20), age int(3), id int(10), item varchar(200));

insert into drive(name, age, id, item) values("samiam",14, 9493792, "book");

insert into drive(name, age, id, item) values("maimas",21, 2973949, "hooks");

insert into drive(name, age, id, item) values("viji",48, 8759420, "TV");

insert into drive(name, age, id, item) values("Raj",20, 9203154, "Chair");

insert into drive(name,age,id,item) values("samiam", 25, 9345627, "Bat");
```

# to display data from certain columns
```sql
select name,ID from drive;
```
#To display certain data by rows:
```sql
select * from drive where(name="sandy")
```

# where clause
Coparison operators:
| Operator     | Description      | Example          |
| ------------ | ---------------- | ---------------- |
| =          | Equal to         | salary = 50000 |
| != or <> | Not equal to     | name != 'John' |
| >          | Greater than     | age > 30       |
| <          | Less than        | stock < 100    |
| >=         | Greater or equal | score >= 60    |
| <=         | Less or equal    | rating <= 4.5  |

EX:
```sql
--Filter by Columns
select age,name from drive;
--Filter by Rows using = operator/Equal To operator
select * from drive where(name="samiam");
--Filter by Rows using <> operator/ Not Equal to operator
select * from drive where(name<>"samiam");
--Filter by Rows using != operator/ Not Equal to operator
select * from drive where(name!="samiam");
--Filter by Rows using > operator/ Greater Than operator
select * from drive where(age>20);
--Filter by Rows using < operator/ Less than operator
select * from drive where(age<20);
--Filter by Rows using <= operator/Less than or equal to Operator
select * from drive where(age<=21)
--Filter by Rows using >= operator/ Greater than or equal to Operator
select * from drive where(age>=21)
```
Logical Operators:
| Operator | Description           | Example                              |
| -------- | --------------------- | ------------------------------------ |
| AND    | Both conditions true  | age > 25 AND city = 'Delhi'        |
| OR     | Either condition true | role = 'Admin' OR role = 'Manager' |
| NOT    | Negates condition     | NOT (status = 'Inactive')          

```sql
-- Filter using Not operator
select * from drive where(Not(name="samiam"));
--Filter using and operator
select * from drive where(name="samiam" and age>20);
-filter using or operator
select * from drive where(name="samiam" or name="maimas");
```
