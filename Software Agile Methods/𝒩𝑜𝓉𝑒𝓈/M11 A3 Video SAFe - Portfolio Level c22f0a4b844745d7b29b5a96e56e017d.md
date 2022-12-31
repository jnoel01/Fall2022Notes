# M11.A3: Video: SAFe - Portfolio Level

```
The SAFe describes goals and plans at several levels of abstraction:

-Investment themes
-Epics
-Features
-Stories
-Tasks

Describe examples of each of these for a company like Driverless Software that produces software and services for self-driving cars. That is, start with a new strategic 
direction for Driverless Software, a high-level direction that will sustain and grow 
Driverless Software for the next 2-4 years. Describe the new strategic direction as an 
Epic and create a strategic plan for delivering that direction.
Drill down into that Epic and give specific examples of themes, features, stories, and 
tasks that might be used in planning and developing software that supports that 
strategic direction. Specifically, identify the new strategic direction and describe at least 2 software releases to deliver that direction. Then break down those 2 releases into at least 5 user stories for each release and describe at least 1 task for each user 
story.
```

***Investment Themes***

***Existing Offerings:*** Driverless Cars prioritizes safety first. Currently Driverless Cars utilizes the best sensors to allow for safe braking, automatic parking, lane switching and object monitoring. These functionalities have been tested in rural and urban atmospheres to ensure proper functionality and coverage in all terrains. 

***New Offerings:*** Driverless Cars ultimate aim is to become a fully autonomous vehicle, meaning passengers can enjoy their ride without the stressors of actually driving. To do this Driverless Cars is planning on implementing numerous enhancements such as speed regulation and ingestion, pilot alertness monitoring, and automatic blinkers. Driverless Cars is pushing for the betterment of our product and comfort of our customers so we are working closely with the best Subject Matter Experts and business partners to ensure we can fund and release the most reliable product. 

**EPIC** 

Theme: Data Ingestion and Speed regulation. As Driverless Cars pushes to make vehicles more autonomous, the implementation of sensors and location data reading to determine the cars speed is essential. This will allow operators to be more hands off.

Software Release 1: In this software release we will implement sensor ingestion of speed limit signs, ingestion of new speed limits laws that are checked frequently based on car location/state, automatic data ingestion of current up to date speed limit, monitor noise if a users if above the speed limit and noise if the user is below the average speed of surrounding cars.

As a product manager, I want to simplify the driving experience for users by monitoring and automatically setting speed so that we can increase the number of people who purchase our vehicle

**UserStory1**

Title: Reading Speed Limit Signs

Acceptance Test: speedLimitSign

Priority: 1

Estimate: 10 months

Description: As a user I want the car to be able to read speed limit signs within a 60 feet distance so that I can adhere to traffic law

Task: Meet with SME and ML scientists on sensors understand number recognition and ingestion

**UserStory2**

Title: Traffic Laws for State

Acceptance Test: trafficLaw

Priority: 1

Estimate: 12 months

Description: As a user I want to be able to know the traffic law for each state that I am in so that I can follow traffic laws and flow with traffic, such as right on red

Task: Research different traffic regulations to see if feasible 

**UserStory3**

Title: Speed Traffic Flow

Acceptance Test: trafficFlowSpeed

Priority: 2

Estimate: 5 months

Description: As a user I want to be able to know the average surrounding traffic speed so that I am up to that speed to ensure no accidents due to my speed

Task: Meet with SME’s to understand sensor input for surrounding traffic

**UserStory4**

Title: Notifying Below Average Speed

Acceptance Test: belowAvgSpeed

Priority: 2

Estimate: 5 months

Description: As a user I want to be notified by a “beep” noise when I am below the average speed limit so that I can manually increase my speed and prevent a potential accident.

Task: Meet with clients to see if they would like this feature to be optional to turn on and off

**UserStory5**

Title: Notifying if Speeding

Acceptance Test: speedingTest

Priority: 1

Estimate: 4 months

Description: As a user I want to be notified by a “beep” noise when I am above the speed limit so that I can drive at a safe speed and avoid traffic violation

Task: Meet with clients to see if they would like this feature to be optional to turn on and off

Software Release2: In this software release we will create the UI/UX for all of the speed related visualizations so that users can be alert when they are violating a traffic law and if there is any malfunction with the cars preset speed settings the pilot can manually pilot and send a diagnostic error to Driverless Cars.

**UserStory1**

Title: Speed Limit Alertness

Acceptance Test: alertSpeedLimit

Priority: 3

Estimate: 6 months

Description: As a user I want to be able to be alerted of any speed limit changes, I want the speed limit changes to appear on my middle dashboard with the speed limit number as well as any change in speed limit read out loud so that I can avoid traffic violations.

Task: Meet with UI/UX design team to get sugestions on the best way to alert of speed limit changes

**UserStory2**

Title: trafficLawAlert

Acceptance Test: alertLaws

Priority: 2

Estimate: 12 months

Description: As a user I want to be able to hear **major** traffic law changes when crossing any state boarders, for example right on red in NJ, to avoid traffic violation. These laws should be announced outloud and display on the driver dash by the wheel.

Task: Meet with customer to see if they would like to hear major traffic law changes depending on state and how they would like us to implement this type of feature

**UserStory3**

Title: trafficFlowAlert

Acceptance Test: alertOfFlow

Priority: 3

Estimate: 5 months

Description: As a user I want to see the traffic flow of each car around me on the dashboard so I know how fast the surrounding cars are going. Cars over the speed limit will be shown in red, cars in the speed limit will be shown in green and cars below the speed limit will be shown in blue to ensure that I am aware of my surrounding vehicles.

Task: Meet with UI/UX team and customers to see if this type of display would be appropriate or if colors is not the most efficient way to get this across

**UserStory4**

Title: Read Caution Signs

Acceptance Test: readCautionSigns

Priority: 1

Estimate: 5 months

Description: As a user I want the car to be able to ingest different road signs, specifically the “slow down” yellow sign when approaching sharp turns. I would like the alert to be said out loud and the sign to flash on the wheel dash this way I can avoid any accidents while turning sharp turns.

Task: Research all potential caution signs and how they vary per state to ensure the sensors will be able to read them

**UserStory5**

Title: Reading Yellow Light

Acceptance Test: readYellowLights

Priority: 1

Estimate: 4 months

Description: As a user I want the car to be able to detect yellow lights, whether they be flashing yellow lights or a normal yellow light, so that the car knows when to slow down. If the light is a yellow flashing light I would like an alert to show on the wheel dash to instruct cautionary speed so that I can avoid any potential accidents. 

Task: Implement feature and test the slow down rates per vehicle on both flashing yellow lights and stationary yellow lights to ensure the car can differentiate between both types of yellow lights