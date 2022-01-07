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





