# Relational Algebra

***Relation Algebra***

- Procedural language
- Six Basic Operations
    
    
    - select:  σ
    - project: π
    - union: **∪**
    - set difference: -
    - rename: **ρ**
    
- The operators take one or two relations as inputs and produce a new relation as a result

**Example of selecting certain parts of a table where all values follow said rule:**

![https://i.gyazo.com/5a1c706bf0e627ac5e22c4e9a5cca4f8.png](https://i.gyazo.com/5a1c706bf0e627ac5e22c4e9a5cca4f8.png)

This says select all where A=B and D is greater than 5

```sql
select *                                                      -> π
from r                     in relation algebra this is->      -> ()
where A=B and D>5                                             -> r
```

- Project means I want to show a certain column:
    - Project example:
    
    ![Untitled](Relational%20Algebra%20ff2cbbc1c4164f6eb9d7d53d81931313/Untitled.png)
    
    The above says: I want to show columns A and C from table r. Since we are not allowed to show duplicates that is why the representation is as shows
    
- In SQL this would be:

```sql
SELECT distinct A,C
FROM r
```

- Union Operation Example:
    
    ![Untitled](Relational%20Algebra%20ff2cbbc1c4164f6eb9d7d53d81931313/Untitled%201.png)
    

For any “set operator” to work:

1. The two relations/table must have the same number of attributes or columns
2. The corresponding columns of the 2 relations/tables must be compatible

- **In OLTP join and cartesian product are important to join and be able to view data across multiple tables**

- Cartesian product is negative bc its expensive, because it combines all rows
    - Example: if you have a 2 column 10 row relation and a 3 column 1,000 row relation, after applying the cartesian product you will have a 100,000 row relation

- If you’re joining A | B and B | C | D it’s important to use the rename function for column B

![Untitled](Relational%20Algebra%20ff2cbbc1c4164f6eb9d7d53d81931313/Untitled%202.png)

The picture equation to the left says where 

A = C I want to join table r and s

- This in SQL would be:
    
    ```sql
    select *
    from r,s
    where r.A = s.C
    ```
    

***Rename Operation***

- Rename renames two things: columns and tables