# Chapter 6: Entity-Relationship Model

***Modeling***

- A *database* can be modeled as:
    - A collection of entities
    - Relationship among entities
- A **entity** is an object that exists and is distinguishable from other objects
    - Example: specific person, company, event, plant
- Entities have *attributes*
- An **entity set** is a set of entities of the same type that share the same properties
    - Example: set of all persons, companies, trees, holidays

- **Reminder: Entity-set is analogous to a table in relational database model**

***Relationship Sets***

- A **relationship** **is an association among several entities
    - Example:
        
        
        | Hayes | Depositor | A-102 |
        | --- | --- | --- |
        | customer entity | relationship set | account entity |
- A relationship set is a mathematical relation among n ≥ 2 entities, each taken from entity sets
    - **{( e**1, **e**2, … **e**n**)  |  e1 ∈ E**1, **e**2 **∈ E**2, ...,  **e**n **∈ E**n**}**
    
           where (e1, e2, …, en) is a relationship
    
    - Example:
    
                     (Hayes, A-102) ∈ depositor
    

***Attributes***

- An entity is represented by a set of attributes, that is descriptive properties possessed by all members of an entity set
    - Example:
        
                 *customer = (customer_id, customer_name, customer_street, customer_city)*
        
                 *loan = (loan_number, amount)*
        
- **Domain-** the set of permitted values for each attribute
- Attribute types:
    - *Simple* and *composite* attributes
        - Composite attributes contain multiple pieces of data:
        
        ![Untitled](Chapter%206%20Entity-Relationship%20Model%20665ebeacedcb4838b62b67bc224a939e/Untitled.png)
        
    - *single-valued* and *multi-valued* attributes
        - example: phone_numbers
    - Derived attributes:
        - Can be computed from other attributes
        - Example: age, given_date_of_birth

***Mapping Cardinality Constraints***

- Express the number of entities to which another entity can be associated via a relationship set
- Most useful in describing binary relationship sets
- For a binary relationship set the mapping cardinality must be one of the following types:
    - One to one
    - One to many
    - Many to one
    - Many to many

***Keys***

- A **super key** of an entity set is a set of one or more attributes whose values uniquely determine each entity
- A **candidate key** of an entity set is a minimap super key
    - *customer_id* is a candidate key of *customer*
    - account_number **is a candidate key of *account*
- Although several candidate keys may exist, on eof the candidate keys is selected to be the **primary key**