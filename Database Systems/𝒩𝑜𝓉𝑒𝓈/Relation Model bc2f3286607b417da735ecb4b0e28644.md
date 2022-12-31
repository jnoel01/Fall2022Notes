# Relation Model

- OLTP: Online Transaction Process
    - Transaction management
    - Transaction (in this context) implies changes
    - Most of the databases that we encounter (99%)
    - “simplify” design
        - 1 thing per table (entity)

![Untitled](Relation%20Model%20bc2f3286607b417da735ecb4b0e28644/Untitled.png)

- OLAP: Online Analytical Process
    - Used for reading and analyzing information
        - As many things that are related in a preset single table
        
- *Third Normal Form* - a form used to normalize the database design to avoid duplication of data

***Entity Relationship Model***

- Models an enterprise as a collection of *entities* and *relationships*
    - Entity: a “thing” or “object” in the enterprise that is distinguishable from other objects
        - Described by a set of *attributes*
    - Relationship: an association among several entities
- Represented diagrammatically by an *entity-relationship* diagram:
    
    ![https://i.gyazo.com/7fc74c726f69016eff8f0c31c343d205.png](https://i.gyazo.com/7fc74c726f69016eff8f0c31c343d205.png)
    

***Object-Relational Data Models***

- Extend the relational data model by including object orientation and constructs to deal with added data types
- Allow attributes of tuples to have complex types, including non-atomic values such as nested relations
- Preserve relational foundations, in particular the declarative access to data, while extending modeling power
- Provide upward compatibility with existing relational languages
- Object-Relation databases are great for defining but not great for manipulating
    - Hard to order/manipulate objects within objects
    

***Query Processing***

1. Parsing and translation
2. Optimization
3. Evaluation

![https://i.gyazo.com/1117ae78eacc50557c16f89e304119b2.png](https://i.gyazo.com/1117ae78eacc50557c16f89e304119b2.png)

---

***Relation Algebra***

- In relation algebra, we need to know what the set of “things” are and what the set of operators are that we are working with.
    - In databases: Things → { *relations }*
        
                                Operators → { x, p, etc }
        
- A relation is a subset of all possible domain values

![Untitled](Relation%20Model%20bc2f3286607b417da735ecb4b0e28644/Untitled%201.png)

***A relation is an INSTANCE of a SCHEMA***

***Keys***

- Let k be in R
- K is a superkey of R if values for K are sufficient to identify a unique tuple of each possible relation r(R)
    - by “possible r” we mean a relation r that could exist in the enterprise we are modeling
    - Example: { customer_name, customer_street } and { customer_name }
        
                         are both superkeys of *customer*, if no two customers can possibly have the same name
        
        - In real life, an attribute such as *custoner_id* would be used instead of *customer_name*
- K is a candidate key if K is minimal
    - Id K is a superkey and no subset of it is a super key then it is a candidate key

***Foreign Keys***

- A relation schema may have an attribute that corresponds to the primary key of another relation. The attribute is called a foreign key
    - E.g. *customer_name* and *account_name* attributes of *depositor* are foreign keys to *customer* and *account* respectively
    - Only values occurring in the primary key attribute of the referenced relation may occur in the foreign key attribute of the referencing relation.
    
    ![Untitled](Relation%20Model%20bc2f3286607b417da735ecb4b0e28644/Untitled%202.png)