# M4.A3: Test-Driven Development

***Test-Frist or Test-Driven Development (TDD)***

- Motivation:
    - Programmers don’t write tests because:
        - They don't like to
        - They don’t have time
        - They have “more important” things to do
- Result:
    - Code breaks
    - Debugging reduces productivity and doesn't improve testing
    - Still no tests
- In test driven development we write tests, watch them fail and refactor

***Alternative TDD Scenario***

- Write tests first
- Run the tests (they’ll probably fail)
- Write some code
- Rerun the tests
- Debug until the tests pass
    - Relatively little untested code at any one time so bugs are likely to be in the most recent code
    

***TDD provides useful feedback***

- Programmers get feedback when their tests pass
- Programmers get feedback when their tests fail
- Customers get feedback when the tests pass or fail
    - Provides insights on how the developers are doing
- Provides frequent metrics for management

***Pace***

- Write a few tests
- Write  a few lines of code
- Don’t write too many tests at once/don’t write too much code at once bc its harder to debug when testing

***xUnit***

- Framework for unit tests, e.g. jUnit, PyUnit(unittest)
- Tests are written as class methods
    - Developers appreciate that tests are code
- Test code is separate from production code
- There are similar xUnit frameworks and tools for many other programming languages
    - CUnit
    - CppUnit
    - csUnit
    

***Architecture of a test***

1. fixture - creates objects and context for test
2. exercise- invokes methods under test
3. result- asserts equality (or something else) about the result of the exercise
    1. Assert equal, not equal, close, membership, etc.
    

***Combining test into a suite***

- collect all the tests for a class in a test suite

![Untitled](M4%20A3%20Test-Driven%20Development%206e84318dca6d4bcdb57ee60b0722b69f/Untitled.png)

***From TDD → Behavior Driven Development (BDD)***

- Customers and some developers have trouble defining tests:
    - Where to start?
    - What to test?
    - What to call the tests?
- How can we improve the test process to include the customers?
    - Change the syntax and simplify the process

***Simplify Testing:***

- Replace source with natural language descriptions
    - Eliminate the word “Test”

***Behavior Templates Aid Testing***

- Given the _
- When _
- Then _

***Evolving User Stories to Behavior Stories***

- Behavior stories are still easy for customers to write and understand
    - Describe what needs to happen

BUT…

- Behavior Stories are easier to map automatically from user descriptions to executable tests cases

***Common table formats for tests***

- ColumnFixture
    - Each row specifies one input and one output
    - One input or output may be a collection of values
- RowFixture
    - First row is input, remaining rows are output
    - Analogous to a query
- ActionFixture
    - Each row is either an action to perform or a value to check
    - Analogous to a state machine