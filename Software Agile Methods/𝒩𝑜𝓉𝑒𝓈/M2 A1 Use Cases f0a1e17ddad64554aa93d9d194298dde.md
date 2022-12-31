# M2.A1: Use Cases

- There are two types of corporate culture:

***Plan Driven Cultures***

- Mangers assign teams
- Individuals work for the manager
- Individuals measured on individual achievements
- Manager assigns tasks
- Manager responsible for improvement
- Infrequent deliveries
- Infrequent feedback from customers
- “Us and Them” e.g. testing, Ops

***Agile Cultures***

- Self organizing teams
- Individuals work for the team
- Individuals measured on team achievements
- Team members select tasks
- Team responsible for reflection and continuous improvement
- Frequent/continuous deliveries
- Frequent/continuous feedback from customers
- “us” e.g. testing, Ops

***What can go wrong with the team?***

- Dysfunctional teams
- Failure to self organize - “tell me what to do” mindset
- Hostility to members - “That’s not my job”
- Inability to adapt to change - “Losing private office space”
- Lack of overall commitment

 ***Role of Managers in both Cultures***

***Plan Driven Cultures***

- Define solutions to be implemented by the team
- Define roles and responsibilities
- Leading the effort
- Command and Control of the Team
- Manager owns the problem

***Agile Cultures***

- Asking questions while allowing the team to create the solution
- Help team to self organize
- Enabling the team while clearing roadblocks to success
- Trusting the team
- Team owns the problem

***Role of Executive in both Cultures***

***Plan Driven Cultures***

- Clear, unchanging direction defined early in the process
- Manage by business case
- Attempt to understand entire problem and outcome in advance

***Agile Cultures***

- Embrace changes
- Rapid delivery and insepction
- Quick prototype solutions to understand impacts
- Executive team is not as involved

***Why Does Agile Not Work For Everyone?***

- Lack of clarity across the team
- Forcing frequent short deliverables without Agile advantages
- Inadequate training or support for Agile Methods
- Failing to use automated testing and/or continuous integration
- Failing to change employee performance metrics
- Bad Agile training
- Failing to inspect and adapt

***Gathering Requirements*** 

- Three different approaches:
    - Traditional requirements - Plan Driven method requirements
    - Use Cases - RUP approach for capturing requirements
    - User Stories - Agile approach for capturing requirements
    

***Plan Driven Requirements***

- Gathering requirements is the first step in a plan driven SDLC
- Business Analyst interviews the customer to extract features required from the system
- Business Requirements Document (BRD)
    - Formal contract b/w the customer and the team delivering the product

***Business Requirements Document (BRD)***

- All requirements are gathered and reviewed by the business analysts before handing over to development
    - Little to no discussion b/w customers and developers
- Describes all of the features needed by the customer - functional and non-functional
- Limitations
    - Assumption of completeness
    - Difficult to change
    - Not created by developers and thrown over the wall to the developers

***Use Cases***

- Part of UML and RUP
- Each use case describes:
    - A scenario
    - The actors in the scenario
    - A sequence of actions between the actor and the system
    - An observable result of value to a particular actor
    - Actor’s intentions/what does the actor want?
- Use case method:
    1. Identify the actors
    2. Identify the use cases
    3. Identify actor/use case relationships
    4. Outline scenarios
- Must identify the actors:
    1. Who uses the system?
    2. Who get information from the system?
    3. Who provides information to the system?
    4. Who supports the system?
    5. What other systems interact with this system?
- Identify the use cases:
    1. What are the intentions of each actor with respect to the system?
        1. Give a descriptive name
            - Start with an action verb
            - Describe the goal or intent
        2. Give a one sentence description
- MSS: Identify the use cases
    - Use Case: Play song- user plays a song on a device
        - Example: The user should be able to play a song on her device and control playback with start, stop, pause, forward, back
            - ***This is very vague because the word device
- Identify Actor/Use Case Relationships in a Use Case Diagram
- Draw a diagram showing relationships between actors and use cases
    - But be sure to include a list of all things we are collecting (specific. unlike the picture below)

![https://i.gyazo.com/c4ab5e4f1fdf949800d32d207728d402.png](https://i.gyazo.com/c4ab5e4f1fdf949800d32d207728d402.png)

***Use Case Template***

1. Name
2. Brief description
3. Actors
4. Basic flow
5. Alternate flows

***Example Use Case:***

1. Name: Play song
2. Brief description: The user selects a song from MSS and plays the song
3. Actors: User
4. Basic Flow:
    1. User visits MSS home page
    2. User selects a song from available content
    3. User pushes start button
    4. Song is streamed to the user’s device
    5. Song plays on user’s device
5. Alternate flows:
    1. User selects song but doesn’t start playing
    2. Song selected by user selected is not available for streaming
    3. User fast forwards past first 30 seconds of song

***Use Case Summary***

- Use cases describe the scenarios in terms of actors and actions
- Specify “all possible” scenarios
- Typically include detailed instructions on how to accomplish those scenarios