# SQL Interview Questions

## Link
https://www.upwork.com/i/interview-questions/sql/

## Questions

1. What is a Relational Database Management System (RDBMS), and which one are you most familiar with?

- A storage system that organizes data into related tables, fields(columns), and records(rows, tuples),
- Postgres, MySQL

2. What are the standard SQL commands every SQL developer should know?

### Data Manipulation Language (DML)
- C: INSERT - Create Data
- R: SELECT - Retrieve/Read Data
- U: UPDATE - Update Data
- D: DELETE - Delete Data


### Data Definition Language (DDL)
- CREATE
- ALTER
- DROP

### Data Control Language (DCL)
- GRANT: Grants privileges to users.
- REVOKE: Revokes privileges previously granted to a user.

3. Can you explain how a RDBMS organizes data into tables and fields?
- Tables contain records consisting of data corresponding to the fields for the given table.
- Example: Customer table has a record with customer first name, last name, and address

4. What is a NULL value and how does it differ from a zero value?
- A null value is the absence of any value, whereas a zero value represents the number zero

5. What are SQL Constraints?
- Restrictions or validations placed on fields to maintain data integrity
- Examples: Default Values, Primary Key, Foreign Key, Unique, Check, Index

6. Name four ways to maintain data integrity within a RDBMS.
- Entity Integrity: Prevent duplicate records (e.g. enforcing unique values on a field)
- Domain Integrity: Restrict type, format, or range of values for data validation (e.g. you can insert a text value into a number field)
- Referential Integrity: Don't orphan records!! Make sure a record use by another record cannot be deleted unless you delete all the related records (Cascade deletion)
- User-Defined Integrity: Rules that aren't database specific (business logic)

7. What is the purpose of database normalization and how does it work?
- Eliminate redundancy and store data in a logical way that reduces space and improves performance

8. Explain the difference between an inner join and outer join using an example.
- Inner join combines rows from two tables and creates a set that only returns rows that match in both tables
- Single Outer Join will include unmatched rows from one table
- Full Outer Join will include unmatched rows from both tables