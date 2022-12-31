# M4:A1: Traditional Testing

***Software Testing***

- The goal of software testing is to determine if the implementation meets its specifications
    - Does the system do what it’s supposed to do?
- Testing and debugging are related . but different tasks
    - Testing identifies problems - debugging fixes problems
- You want to have an automatic test script that runs in the repo so you know when the code breaks at anytime

- You test that a release works in waterfall at the end
- You test that a feature works in agile continuously

***Traditional testing : Unit Testing***

- Ensures that recently changed unit works correctly
    - Who - developers
    - What - New features or bug fixes; Code/branch coverage
    - When - After code complete; before integration

***Integration Testing***

- Ensures that components, potentially written by different developers, integrate cleanly and work together
    - Who - developers and/or testers
    - What - Test multiple modules from potentially different developers
    - When - After unit test is complete on relevant modules
    

***System Testing***

- Ensures that complete system is correct
- May include functionality, performance, stress testing, etc.
    - Who - system test team (not devs)
    - What- Test complete system; performance and security; stress testing
    - When - After all code modules are complete

***Acceptance Testing***

- Customer verifies that the system performs as expected and meets requirements
    - Who - Customer test engineers
    - What - Complete system based on requirements
    - When - After system test, frequently before final payment

![Untitled](M4%20A1%20Traditional%20Testing%20bccbf77352bd47a3b4d652f1ac6d5c8a/Untitled.png)

![Untitled](M4%20A1%20Traditional%20Testing%20bccbf77352bd47a3b4d652f1ac6d5c8a/Untitled%201.png)

***When to integrate?***

- Agile methods you integrate after every code push (everyday)
- Traditional methods could be every week or until every piece of the code is done