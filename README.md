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
#Today's Code, 7,12,2025, July 12th
```sql
create table school(name varchar(30) not null, id int(10) not null primary key,age int(5),grade int(3) not null);

insert into school(name,id,grade,age) values("Beach",7298301, 9, 14);

insert into school(name,id,grade) values("Sandy",9187329, 12);

insert into school(name,id,grade,age) values("Wonder",7654892, 10, 15);
insert into school(name,id,grade) values("Render",8976543, 9);
insert into school(name,id,grade,age) values("Walter",6327819, 12, 19);
insert into school(name,id,grade) values("John",5482931, 11);
insert into school(name,id,grade,age) values("Mat",8302749, 5, 10);
insert into school(name,id,grade,age) values("Hunter",1920364, 7, 11);
insert into school(name,id,grade,age) values("Groot",1928304, 8, 13);
insert into school(name,id,grade,age) values("Rose",1983278, 9, 16);

select * from school;

select distinct grade from school;

select * from school where age between 13 and 16
```
#Not Null
```sql
create table school(name varchar(30) not null, id int(10) not null primary key,age int(5),grade int(3) not null);
-- Not null is a constraint.
--What it does is it makes it that, that feild when entered mandatory
--by making it that, that feild cannot have a option called Null which mean nothing
```
#Primary key
```sql
create table school(name varchar(30) not null, id int(10) not null primary key,age int(5),grade int(3) not null);
--Primary key is a constraint.
--When using primary key you have to put a value for it.
--Primary key makes it that it has unique values so no duplicates.
```

#Distinct
```sql
select distinct grade from school;
--It removes duplicates and prints only the unique ones.
--it doesn't remove values from the table
```
#CODE
```sql
create database test;
create table test_table3(id int(5) , name varchar(20) , country varchar(20));

insert into test_table3(id,name,country) values(1,"sandy","India");
insert into test_table3(id,name,country) values(2,"andy","India");
insert into test_table3(id,name,country) values(3,"ndy","India");

insert into test_table3(id,name,country) values(4,"sandy","US");
insert into test_table3(id,name,country) values(5,"andy","US");
insert into test_table3(id,name,country) values(6,"ndy","US");

insert into test_table3(id,name,country) values(7,"sandy","Africa");
insert into test_table3(id,name,country) values(8,"andy","Africa");
insert into test_table3(id,name,country) values(9,"ndy","Africa");

select * from test_table3 where country not in ("India","US");


select * from test_table3 where country like 'I%';


select * from test_table3 where country like '__d%';
```

#not in
```sql
--it is used to filter data. it is used in where, and displays the rows which the column's vlaue doesn't match the value given
select * from test_table3 where country not in ("India","US");
```
#Like
it is an operator.
```sql
--The SQL LIKE operator is used in the WHERE clause to search for a specified pattern within a column.
--The _ wildcard represents a single character.
--in this case it is saying the there needs to be 2 letters before d because there is 2 underscores
--The % wildcard represents any number of characters, even zero characters.
--In this case it is saying that there can be any number of letters after d.
select * from test_table3 where country like '__d%';
```

TODAys CODE: Used sql programz pre-existing code and new.
```sql
select * from customers where first_name like '%j%';
select * from customers where first_name like 'D%';
select * from customers where first_name like '%y';
select * from customers where first_name like '[A-Z]%';
select * from customers where last_name like '[d]%';

--update query

update Customers set first_name="sandy";
create table tests(id int(10) primary key , name varchar(10) unique);
insert into tests(id,name) values(1,'landy');
insert into tests(id,name) values(12,'bandy');
insert into tests(id,name) values(13,'randy');
update tests set name="candy" where id=1;
select * from tests;

--delete
delete from  tests where id=1
```
EXamples of Like Operator
```sql
select * from customers where first_name like '%j%';
select * from customers where first_name like 'D%';
select * from customers where first_name like '%y';
select * from customers where first_name like '[A-G]%';
select * from customers where last_name like '[d]%';
-- these brackets [] are used to give a range.
- in this case in the last to second query we gave a range that the first letter has to be A and G and can be A or G.
```
