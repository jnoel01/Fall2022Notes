# M2.B2: Assignment: Homework Assignment 2: User Story

```
**Your consulting job with Driverless Cars from Homework 1 is going well, and they want to
proceed to the next step: Defining three features for the driver-free parking function 
that allows cars to park themselves without assistance from humans.

In this assignment, you will have the following deliverables:

Identify three features relevant to driver-free parking.
Describe each of the three features as a use case.
Describe each of the same features as user stories.
Describe the advantages and disadvantages of use cases and user stories for this task.**
```

***3 Features:***

1.) Pressing the park button to launch the process

2.) When the car has found spot, the car will “ding” 3 times to notify you that a spot has been found

3.) When the car begins parking, the words “PARKING” will appear on a driver dashboard until the process is finished

                                                                 ***Use Cases***

| Use Case 1 | Pressing the Park Button |
| --- | --- |
| Actor | Driver |
| Brief Description | Pressing the “Park” button in the drivers car will start the parking process from beginning-end, unless there is interference.  |
| Basic Flow | Everyday the driver pulls into the neighborhood parking lot. She presses the “Park” button on her car dashboard and the begins it’s parking process. |
| Alternate Flow | The driver does not press the parking button and the car remains in the current state that it is in |
| Alternate Flow | The driver pressing the “Park” button but then presses on the break. The parking process then disengages and to start it again the driver must press the “Park” button again |
| Alternate Flow | The driver pressing the “Park” button but then presses on the “Park” button once more. The parking process then disengages and to start it again the driver must press the “Park” button again |

| Use Case 3 | Parking In-Process Display |
| --- | --- |
| Actor | Driver |
| Brief Description | While the autonomous car has initiated the parking process, the driver dashboard will display “PARKING’. |
| Basic Flow | Everyday the driver pulls into the neighborhood parking lot and uses the autonomous parking feature to park her car. When the the parking process is initiated the driver dashboard displays the words “PARKING” to notify to the driver of the current process until it is finished (when the car is parked). |
| Alternate Flow | Everyday the driver pulls into the neighborhood parking lot and uses the autonomous parking feature to park her car. When the the parking process is initiated the driver dashboard displays the words “PARKING” to notify to the driver of the current process. The driver initiates the parking process but then steps on the break, the “PARKING” display on the dashboard will go away. |
| Alternate Flow | Everyday the driver pulls into the neighborhood parking lot and uses the autonomous parking feature to park her car. When the the parking process is initiated the driver dashboard displays the words “PARKING” to notify to the driver of the current process. The driver initiates the parking process but there is no spot found to park in, the “PARKING” display will go away. |

***User Stories***

**Title:** Press Parking Button

**Acceptance Test:** pressPark

**Priority:** 1

**Story Points:** 3

As a driver

I want to press a parking button in the car

so that I initiate the cars autonomous parking process

---

**Title: Car Spot Found Notification**

**Acceptance Test:** spotFoundSound

**Priority: 2**

**Story Points:** 1

As a driver

I want to hear a “ding” noise three times

so that I know when my car has found a spot to park in

---

**Title: Parking In-Progress Display**

**Acceptance Test:** displayParkingProg

**Priority: 2**

**Story Points:** 1

As a driver

I want to see “PARKING” displayed on my dashboard

so that I know when my car is in autonomous parking mode

• Describe the advantages and disadvantages of use cases and user stories for this task.

| Use Case 2 | Car Spot Found |
| --- | --- |
| Actor | Driver |
| Brief Description | Upon in starting the autonomous parking mode, the car will “ding” 3 times when a spot has been found. |
| Basic Flow | Everyday the driver pulls into the neighborhood parking lot and begins the automatic parking process.  The car utilizes its LIDAR sensors to find a parking spot. The car  drives around the neighborhood parking lot until it identifies a parking spot with no car occupying it, the car now plays a “ding” sound 3 times to notify the driver that an empty spot has been found. |
| Alternate Flow | Everyday the driver pulls into the neighborhood parking lot and begins the automatic parking process.  The car utilizes its LIDAR sensors to find a parking spot. The car  drives around the neighborhood parking lot but no empty spot is identified within the lot. The car notifies the user by audibly playing the “No Immediate Spot Found”. The car now prompt the user to go into Drive, by flashing the D on the user dashboard and on the gear stick dashboard. |

                                 ***Advantages & Disadvantages*** 

| Disadvantages - User Cases | Advantages - User Stories | Disadvantages - User Stories | Advantages - User Stories |
| --- | --- | --- | --- |
| There is little to no discussion between customers and developers, so the UI/UX & features may not be what the customer wants | The features for the autonomous parking process, which ultimately act as steps, as broken down in lower-level scenarios which come together, which make testing & validation easier | There is a lack of context which in a project like Driverless cars is not ideal. When the risk is that high it’s important to have very specific details | User stories are more flexible and easier to write so the SDLC can go faster |
| The information could be so detailed that it is confusing or ends up crossing over another feature without realization | Each use case has immense detail so the developers do not have to have as much communication with the stakeholders later on to clear things up | Gaps may arise as the user story and project continue to evolve | They focus more on the customer satisfaction and result which can be better for the business |
| Scenario management is difficult and it is expected to have all possible scenarios in the use case | Each use case offers an alternative flow, which can help to mitigate the high risks involved with the Driverless Car software. | User Stories are more ideal for smaller projects and building out an autonomous car’s software is a larger project | User Stories encourage creativity and discussion which may be better for the UI/UX of the car |