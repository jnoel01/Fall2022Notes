# Chapter 1: Introduction

***DBMS has:***

- storage

- tables

- lists

- tools

- data

- transferring tools

- structure

- column names

- ways to organize data

- filter data

- admin rights

---

- There is a host of software components, working jointly or independently to interact with the data
- There is an environment that controls the data as well as the programs themselves
- OS talks to software and software talks to data (OS>Software>Data xfer)

- DDL- Data definition language
- DML- Data manipulation language

![Untitled](Chapter%201%20Introduction%20b5a46289d5ac4ed38bfef48e6eee7de3/Untitled.png)

![Untitled](Chapter%201%20Introduction%20b5a46289d5ac4ed38bfef48e6eee7de3/Untitled%201.png)

- Unit of working = transaction
    - Example: transferring $2.00 from moms bank account to a kids bank account. The transaction could fail while transferring so the entire process (from removal of money to insertion of money) is considered a transaction a.k.a “unit of work”

![Untitled](Chapter%201%20Introduction%20b5a46289d5ac4ed38bfef48e6eee7de3/Untitled%202.png)

***Database Management System***

- DBMS contains information about a particular enterprise
    - Collection of interrelated data
    - Set of Programs to access the data
    - An environment that is both **convenient** and **efficient** to use
- Database Applications:
    - Banking: all transactions
    - Airlines: reservations, schedules
    - Universities: registration, grades
    - Sales: customers, products, purchases
    - Online retailers: order tracking, customized recommendations
    - Manufacturing: production, inventory, orders, supply chain
    - Human Resources: employee records, salaries, tax deductions
- Databases touch all aspects of our lives

- Summary breakdown:

![Untitled](Chapter%201%20Introduction%20b5a46289d5ac4ed38bfef48e6eee7de3/Untitled%203.png)

---

***Purpose of Database Systems***

- In early days, database applications were built directly on top of file systems
- Drawbacks of using file systems to store data:
    - Multiple file formats, duplication of information in different files
- *Difficulty in accessing data*
    - Need to write a new program to carry out each new task
- *Data Isolation:* Multiple files and formats
- *Integrity* problems:
    - Integrity constraints (e.g. account balance > 0) become “buried” in program code rather than being stated explicitly
    - Hard to add new constraints or change existing ones
- *Atomicity of updates*
    - Failures may leave database in an inconsistent state with partial updates carried out
    - Example: Transfer of funds from one account to another should either complete or not happen at all
- *Concurrent access* by multiple users
    - Concurrent accessed needed for performance
    - Uncontrolled concurrent accesses can lead to inconsistencies
        - Example: Two people reading a balance and updating it at the same time
- *Security* problems
    - Hard to provide user access to some, but not all, data
- Database systems will offer solutions to all the above

---

- The difference between big data and just data is that big data is so big that having all the “big data” in a relation database is not practical.
    - It’s happening so quickly that it doesn’t make sense to translate all the activities into a relation format
- You go to the data instead of bringing the data into the database
- Because big data is so big, small errors in the data, won’t make a large difference in the analysis of the data

***Levels of Abstraction***

- Physical Level: describes how a record (e.g., customer) is stored
- Logical Level: describes data stored in database, and the relationships among the data
    
    ```jsx
    type *customer* = record
    	*customer_id:* string
    	*customer_name: string
    	customer_street: string
    	customer_city: integer
    end*
    ```
    
- View Level: A way to hide (a) details of data types and (b) information

***Instances and Schemas***

- Similar to types and variables in programming languages
- *Schema* - the logical structure of the database
    - Example: The database consists of information about a set of customers and accounts and the relationship between them
    - Analogous to type information of a variable in a program
    - *Physical Schema*: database design at the physical level
    - *Logical Schema*: database design at the logical level
- *Instance* - the actual content of the database at a particular point in time
    - Analogous to the value of a variable
- *Physical Data Independence:* the ability to modify the physical schema without changing the logical schema
    - Applications depend on the logical schema
    - In general, the interfaces between the various levels and components should be well defined so that changes in some parts do not seriously influence others.
    
- **Schema is the structure, Instance is the actual content/database**

![Untitled](Chapter%201%20Introduction%20b5a46289d5ac4ed38bfef48e6eee7de3/Untitled%204.png)

---

***Data Models***

- A collection of tools for describing
    - Data
    - Data relationships
    - Data semantics
    - Data constraints
- Relational model

- Entity-Relationship data model
    - Mainly for database design
    - Non-technical people
- Semistructured data model (XML)
- Other older models:
    - Network model
    - Hierarchical model

***Data Manipulation Language***

- Language for accessing and manipulating the data organized by the appropriate data model
    - DML also known as query language
- Two classes of languages
    - *Procedural:*  user specifies what data is required and how to get those data
    - *Declarative (nonprocedural)*- user specifies what data is required without specifying how to get those data
- SQL is the most widely used query language

***Data Definition Language***

- Specification notation for defining the database schema
- DDL compiler generates a set of tables stored in a *data* *dictionary*
- Data dictionary contains metadata (i.e. data about the data)
    - Database schema
    - Data *storage and definition* language

---

***Relational Model***

- Example of tabular data in the relational model

![https://i.gyazo.com/d72778deffdfbf50b84c4354cb85fcce.png](https://i.gyazo.com/d72778deffdfbf50b84c4354cb85fcce.png)

- In mathematical model columns are attributes
- In a mathematical model a particular instance of data is a tuple
- If you have a set of tuples that represent the data they are called relations

- D**atabase is a set of relations or tables**
- A **table or relation is a tuples or rows**
- E**ach row contains attributes/columns of data**

---

***SQL***

- SQL: widely used non-procedural language
    - Example: Find the name of the customer with customer-id 192-83-7465
    
    ```sql
    select customer.customer_name
    from customer
    where customer.customer_id = '192-83-7465'
    ```
    
    - Example: Find the balances of all accounts held by the customer with customer-id 192-83-7465
    
    ```sql
    select account.balance
    from depositor, account
    where depositor.customer_id = '192-83-7465' and
    			depositor.account_number = account.account_number
    ```
    
    - Application programs generally access databases through one of
        - Language extensions to allow embedded SQL
        - Application program interface (e.g., ODBC/JDBC) which allow SQL queries to be sent to a database