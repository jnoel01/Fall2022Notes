# Introduction

- Requirements Engineering - The branch of software engineering concerned with the *real-world goals for functions of and constraints* on software systems.
    - It is also concerned with the *relationship of these factors to precist specifications of software behavior,* and to their *evolution over time* and across software families
- At the core of any software system is User Requirements
    - There are also System requirements where we decide which systems to use
    - Software design specifications are built with both User Requirements and System Requirements,
- There are 3 levels of abstraction
    
    1.) User requirements
    
    2.) System requirements
    
    3.) Software design specifications
    

***Exemplar System I***

- Airline baggage handling
    - Embedded, real-time
    - Moves baggage from a central loading point and redirects to one of many conveyors based on bag id
- Denver International Airport tried such a system
- System used PCs, thousands of remote-controlled carts, 21-mile-long track
- Carts move along the track, carrying luggage from check-in counters to sorting areas and then straight to the flights waiting at airport gates
- Each piece of baggage has a special bar-coded tage
- After spending 230 million over 10 year project, it was cancelled

**Why was it cancelled?**

**The upfront requirements were not thought through and were not spent enough time on**

***Breakdown of Airline Bagging Handling***

- **User Requirement**: The system should be able to handle 20 bags per minute
- System Requirements
    - Each bag processed shall trigger a baggage event
    - The system shall be able to handle 20 baggage events per minute
- Software Specification
    - 1.2 The system shall be able to process 20 baggage events per minute in operational mode
    - 1.2.1 If more than 20 baggage events occur in an a one minute interval, then the system shall…
    - 1.2.2 More exception handling…
- Functional Requirements:
    - 1.1 The system shall handle up to 20 bags per minute
    - 1.4 When the system is in idle mode, the conveyor belt shall not move
    - 1.8 If main power fails, the system shall shut down in an orderly fashion within 5 seconds
    - 1.4 If the conveyor belt motor fails, the system shall shut the input feed mechanism within 3 seconds

***Functional Requirements***

- The services the system should provide
- How it will react to inputs
- Need to explicitly state what the system should not do
- Can be high-level and general (user requirements) or detailed, expressing inputs, outputs, exceptions, etc. (system requirements)
- Many forms of representation from natural language and visual models, to formal methods

**IMPORTANT** ***Functional vs Nonfunctional Requirements***

- NOTE IF THE BELOW IS ACCURATE? PROFESSOR MOVED TOO FAST BUT THIS WILL BE ON QUIZ
- Functional: How the system will do it
- Nonfunctional: What the system will do

***Example of non-functional requirements for Baggage Example***

- Product requirements
    - Efficiency
        - Performance (e.g. number of bags per minute)
        - Space (e.g. physical size of system, amount of memory, power consumption)
    - Reliability (MTBF,MTFF)
    - Portability (e.g. can it be used with other hardware?)
    - Usability (amount of training required)
- Organizational requirements
    - Delivery (e.g., date of delivery, fully operational, training sessions, updates)
    - Implementation (e.g, full capability in first roll-out or phased)
    - Standard (if there are industry  standards for handling systems)
- External Requirements
    - Interoperability (e.g., with other equipment, communications, standards, etc.)
    - Ethical (e.g., security clearance for RE’s professional certification)
    - Legislative
        - Privacy (HIPAA, FERPA)
        - Safety (OSHA)
    

***Goal vs. Requirements***

- Some Nonfunctional requirements are difficult to define precisely, making them difficult to verify
- Should distinguish goals from NFRs
    - Goal - A general intention of a stakeholder
        - The system should be easy to use by experienced operators
    - Verifiable NFR - statement using some objective measure
        - Experienced operators shall be able to use all the system functions after 2 hours of training
        

***Domain Requirements***

- Derived from the application domain
- May be:
    - New functional requirements
    - Constraints on existing functional requirements
    - Specify how particular computations must be performed

***Domain Requirements for Baggage Example***

- For the baggage handling system, various domain realities create requirements
    - Industry standards (you wouldn’t want the new system to underperform versus other airlines’ systems)
    - Constraints imposed by existing hardware available (e.g., conveyor systems)
    - Union contracts (there may be constraints based on collective bargaining agreements)