# SQL
![sql](https://res.cloudinary.com/practicaldev/image/fetch/s--MlzXm8j1--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/15utqnbl0s7x63q54crj.jpg)

SQL is a standard language for accessing and manipulating databases.

## Database :
- Create a new database
    ````
    CREATE DATABASE DB_NAME
    ````
- Remove a database
    ````
    DROP DATABASE DB_NAME
    ````
- Backup a database
    ````
    BACKUP DATABASE databasename
    TO DISK = 'filepath';
    ````
## TABLE DDL (Data Definition Language):
- Create a new table
    ````
    CREATE TABLE tableName(column datatype,...)
    ````
- Remove a table
    ````
    DROP TABLE tableName
    ````
- Alter a table
    The alter statement is used to add or drop columns from a table
    ````
    ALTER TABLE tableName
    ADD column_name datatype;
    ````
    ````
    ALTER TABLE tableName
    DROP COLUMN column_name;
    ````
- Constraints

    | Constraint  | what do     |
    | ----------- | ----------- |
    | NOT NULL    | column cannot have a NULL value |
    | UNIQUE      | all values in a column are different |
    | PRIMARY KEY | combination of a NOT NULL and UNIQUE |
    | FOREIGN KEY | destroy links between tables |
    | CHECK       | check condition for thee value |
    | DEFAULT     | Set a Default value if no value is specified |
    | CREATE INDEX | create and retrieve data from the database very quickly |

- Index
    The index is used to speed up searches/queries.
    - Create a new index
        ````
        CREATE INDEX index_name
        ON table_name (column1, column2, ...);
        ````
    - Remove an index
        ````
        DROP INDEX index_name ON table_name;
        ````
        in mysql
        ````
        ALTER TABLE table_name
        DROP INDEX index_name;
        ````
- Views
    In SQL, a view is a virtual table based on the result-set of an SQL statement.
    - Create a View
        ````
        CREATE VIEW view_name AS
        SELECT column1, column2, ...
        FROM table_name
        WHERE condition
        ````
    - Update a View
        ````
        CREATE OR REPLACE VIEW view_name AS
        SELECT column1, column2, ...
        FROM table_name
        WHERE condition
        ````
    - Remove a View
        ````
        DROP VIEW view_name;
        ````

## Table DML (Data Manipulation Language)

- SELECT
    ````
    SELECT columm FROM tableName
    ````
- SELECT DISTINCT
    ````
    SELECT DISTINCT column1, column2, ... FROM tableName
    ````
- SELECT WHERE condition
    ````
    SELECT column1, column2, ... FROM tableName WHERE condition
    ````
- INSERT
    ````
    INSERT INTO table_name(column1, column2, ...)
    VALUES (value,value ....)
    ````
- UPDATE
    ````
    UPDATE table_name SET column = value
    WHERE condition
    ````
- DELETE
    ````
    DELETE column FROM tableName
    WHERE condition
    ````
- SELECT TOP & LIMIT 
    ````
    SELECT TOP 3 FROM tableName
    SELECT FROM tableName LIMIT 3
    ````
- MAX() & MIN()
    ````
    SELECT MAX(price) FROM tableName
    SELECT MIN(price) FROM tableName
    ````
- COUNT() AVG() SUM()
    `````
    SELECT COUNT(column) FROM tableName
    SELECT AVG(column) FROM tableName
    SELECT SUM(column) FROM tableName
    ````
## SQL JOINS :
- Inner Join :
    ````
    SELECT column1, column2, ...FROM table1
    Inner Join table2
    ON condition
    ````
- Left Join :
    ````
    SELECT column1 , column2, ... FROM table1
    LEFT Join table2
    ON condition
    ````
- Right Join :
    ````
    SELECT column1 , column2, ... FROM table1
    Right Join table2
    ON condition
    ````
- Full Join

    ````
    SELECT column1 , column2, ... FROM table1
    FULL OUTER JOIN table2
    ON condition
    ````
## Having

Having is working with (COUNT,SUM,AVG,MIN,MAX) as a condition

    ````
    SELECT COUNT(id) FROM tableName
    HAVING COUNT(id) > 10
    ````

## Exists

- Exists is return a boolean value

    ````
    SELECT id FROM tableName
    WHERE Exists (SELECT ....)
    ````
## ANY & ALL

- Any return true if one or more value respect the condition

    ````
    SELECT column1, column2, ... FROM table1
    WHERE column = ANY (SELECT ....)
    ````
- All return true if all of the values respect the condition

    ````
    SELECT column1, column2, ... FROM table1
    WHERE column = ALL (SELECT ....)
    ````

    

