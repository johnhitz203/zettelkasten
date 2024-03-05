# sql

## Basic Structure: classes and schemas
https://web.csulb.edu/colleges/coe/cecs/dbdesign/dbdesign.php?page=class.php
<ins>Objects/things modeled by UML classes</ins>

### Introduction 

- A UML class is used to model a "thing" in the enterprise 
  - This could be a physical thing (eg a store, an animal)
  - Or it could be a fact or an event (e.g. lending of a book)

- UML classes have
  - name: nearly always a noun because it is a thing
  - description: differentiates two classes with the same name
  - attributes: uniquely defines the class

- Class Diagram: A three element rectangle 
```
-----------------------
|        Customer      | <- UML Class Name
-----------------------
| - first_name: string | <- Attribute names and types
| - last_name: string  |
| - phone : string     |
| - zip : string   |
-----------------------
|                      | <- Methods (not used here)
-----------------------
```

- Relational Scheme - Identified by the plural class name and list all attributes and represented as a row
```
Scheme name --> Customer
attributes  --> [ first_name | last_name | phone | street | zip ]

or in set notation as
Customer = {first_name, last_name, phone, zip}
```
- Everything is a set

### Basic Structures: tables and rows
https://web.csulb.edu/colleges/coe/cecs/dbdesign/dbdesign.php?page=tables.php

<ins>Database tables, rows, keys</ins>
- Representing data in rows - each real world item is a represented in a row and each row is tuples

### SQL Statements

- Insert single item
```
INSERT INTO customers(first_name, last_name, phone, street, zipcode)
  VALUES ('Tom', 'Jewett', '714-555-1212', '10200 Slater', '92708');
```

- Insert multiple with some fields missing
```
INSERT INTO customers(first_name, last_name, phone)
  VALUES ('Alvaro', 'Monge', '562-985-4671'),
         ('Wayne', 'Dick', '562-985-1190');
```

- Updating rows
```
UPDATE customers
  SET phone = '714-555-2323'
  WHERE phone = '714-555-1212';
```

- Deleting rows :: 
  #### <ins> Caution </ins> - if where clause is left off it will delete all rows
```
DELETE FROM customers
  WHERE cZipCode = '90840';
  ```

### SQL Tables with constraints
- Table - a set of zero or more tuples (rows)
  - Tuples is unique - it can not share exactly the same attributes with any other row
  - Tuples are unordered - can be displayed in any order w/o changing the meaning
  - Tuple inclusion criteria is used to define subsets
  - Tuple subset allow union, intersection, and difference within a given schemas

### Insuring unique rows
- constraints - Insure tables follow rule of uniqueness for tuples
  - To implement a relation as a SQL table, there must b a set of attributes whose values together guarantee uniqueness of each row

- Add constraint for the primary key
  ```
  ALTER TABLE customers
    ADD CONSTRAINT customers_pk PRIMARY KEY (first_name, last_name, phone);
  ```

- [[database]]
- [[index]]