# SQL
SQL stand for structerd query language
## Queries
**1.SELECT**

synatax: 

SELECT column, another_column, …
FROM mytable;

[Ex1](./sqlScreenShoot/Screenshot%20(49).png)

**2.Queries with constraints**

synatax:

SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
    
[Ex2](./sqlScreenShoot/Screenshot%20(50).png)

**3.Queries with constraints**

these in the where condition

-=	Case sensitive exact string comparison

-!= or <>	Case sensitive exact string inequality comparison

-LIKE	Case insensitive exact string comparison

-NOT LIKE	Case insensitive exact string inequality comparison

-%	Used anywhere in a string to match a sequence of zero or more characters 

-IN (…)	String exists in a list

-NOT IN (…)	String does not exist in a list

[Ex3](./sqlScreenShoot/Screenshot%20(51).png)

**4.Filtering and sorting Query results**

syntax:

SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;

DISTINCT mean no duplicate in the rows

limit mean how many rows of the output

offset means from where it start limiting

[Ex4](./sqlScreenShoot/Screenshot%20(52).png)

**5.Simple SELECT Queries**

syntax:

SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;

[Ex5](./sqlScreenShoot/Screenshot%20(53).png)

**6.Multi-table queries with JOINs**

syntax :

SELECT c1,c2,...
FROM table1
INNER JOIN table2 
    ON table1.id = table2.id
WHERE condition(s)
ORDER BY c1 or c2 ASC/DESC
LIMIT num_limit OFFSET num_offset;

JOIN that matches rows from table1 and the table2 which have the same key (id)

[Ex6](./sqlScreenShoot/Screenshot%20(56).png)

**13.Inserting rows**

synatx:

INSERT INTO table
(c1,c2,c3,..)
VALUES (v1,v2,v3,...)

[Ex13](./sqlScreenShoot/Screenshot%20(57).png)

**14.Updating rows**

synatx:

UPDATE table
SET c1 = value, 
    c2 = value, 
    …
WHERE condition;

[Ex14](./sqlScreenShoot/Screenshot%20(58).png)


**15.Deleting rows**

synatx:

DELETE FROM table
WHERE condition;

[Ex15](./sqlScreenShoot/Screenshot%20(59).png)

**16.Creating tables**

synatx:

CREATE TABLE IF NOT EXISTS table-name (
    column1 DataType TableConstraint DEFAULT default_value,
    column2 DataType TableConstraint DEFAULT default_value,
    …
);

*Datatype like:

-INT

-BOOLEAN (0 or 1)

-FLOAT, DOUBLE, REAL

-CHARACTER(num_chars), VARCHAR(num_chars), TEXT  (string)

*Constraint	like
PRIMARY KEY

[Ex16](./sqlScreenShoot/Screenshot%20(60).png)

**17.Altering tables**

-synatx for adding column:

ALTER TABLE table
ADD column DataType OptionalTableConstraint 
    DEFAULT default_value;

-suntax for deleting column:

ALTER TABLE table
DROP column-name;

syntax for renaming the table:

ALTER TABLE mytable
RENAME TO new_table_name;

[Ex17](./sqlScreenShoot/Screenshot%20(61).png)

**18.Dropping table**

syntax :

DROP TABLE IF EXISTS table-name;

[Ex18](./sqlScreenShoot/Screenshot%20(62).png)






