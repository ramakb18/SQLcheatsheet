# SQLcheatsheet
# SQL Commands Cheatsheet

SQL commands are essential for managing databases effectively. These commands are divided into categories such as Data Definition Language (DDL), Data Manipulation Language (DML), Data Control Language (DCL), Data Query Language (DQL), and Transaction Control Language (TCL).

## Table of Contents
1. [What are SQL Commands?](#what-are-sql-commands)
2. [Categories of SQL Commands](#categories-of-sql-commands)
   - [DDL – Data Definition Language](#ddl--data-definition-language)
   - [DQL – Data Query Language](#dql--data-query-language)
   - [DML – Data Manipulation Language](#dml--data-manipulation-language)
   - [DCL – Data Control Language](#dcl--data-control-language)
   - [TCL – Transaction Control Language](#tcl--transaction-control-language)
3. [Important SQL Commands](#important-sql-commands)
4. [FAQs](#faqs)

---

## What are SQL Commands?

SQL commands are instructions used to interact with the database and perform operations such as creating tables, adding data, modifying data, and controlling access. SQL commands are categorized into five sublanguages:

- **DDL**: Data Definition Language
- **DML**: Data Manipulation Language
- **DCL**: Data Control Language
- **DQL**: Data Query Language
- **TCL**: Transaction Control Language

---

## Categories of SQL Commands

### DDL – Data Definition Language

DDL commands define, alter, and delete database structures such as tables, indexes, and schemas. They deal with the descriptions of the database schema and help modify the structure of database objects.

#### Common DDL Commands:
- `CREATE TABLE`: Used to create a new table.
- `ALTER TABLE`: Used to modify an existing table.
- `DROP TABLE`: Used to delete an entire table.

#### Example of DDL:
```sql
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    hire_date DATE
);


SELECT first_name, last_name, hire_date
FROM employees
WHERE department = 'Sales'
ORDER BY hire_date;


INSERT INTO employees (first_name, last_name, department)
VALUES ('Jane', 'Smith', 'HR');


GRANT SELECT, UPDATE ON employees TO user_name;



BEGIN TRANSACTION;
UPDATE employees SET department = 'HR' WHERE employee_id = 1;
SAVEPOINT savepoint1;
UPDATE employees SET department = 'Sales' WHERE employee_id = 2;
ROLLBACK TO SAVEPOINT savepoint1;
COMMIT;


