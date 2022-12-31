# Homework 7

> ***************PROBLEM***************
> 
> 
> Define 2 use case for a bike ride sharing system/app. You may research NYC's Citibike as a model (or any other bike ride sharing you maybe familiar with).
> 
> Please provide adequate details especially in items 3 to 7 below. Use the following template (also shown in the class) to provide your answer:
> 
> 1. Name
> 2. Brief Description
> 3. Actors
> 4. Basic Flow
> 5. Alternate Flows
> 6. Pre-Conditions
> 7. Post-Conditions
> 8. Special Requirements

*********USE CASE 1*********

1.) Share Ride

2.) The user must be able to share their start and end time during their biking trip through the bike app with selected phone contacts, the updates from when the user started and ended will be sent via SMS to the contacts number.

3.) Bike User, Contact(s)

4.) BASIC FLOW: The user will open the app and unlock a bike at the bike terminals, when the bike is unlocked the user can go to the app and press “share ride”. A form will open prompting bike users to select which contact or contacts they would like to share their ride with. The app will send an SMS to the selected contacts sharing that [bike users name] has started a ride from [location] at [time]. When the bike user re-locks their bike at a bike terminal another SMS will be sent to the previously selected contacts that states [bike users name] has ended a ride at [location] at [time].

5.) FIRST ALTERNATE FLOW: The user will open the app and unlock a bike at the bike terminals, when the bike is unlocked the user can go to the app and press “share ride”. A form will open prompting bike users to select which contact or contacts they would like to share their ride with. The user chooses to not share their ride with anyone and presses an “X” at the top right of the form. The user can choose to reopen this form and send to contacts at anytime during their ride prior to locking the bike at their destination terminal.

SECOND ALTERNATE FLOW: The user will open the app and unlock a bike at the bike terminals, when the bike is unlocked the user can go to the app and press “share ride”. A form will open prompting bike users to select which contact or contacts they would like to share their ride with. The app will send an SMS to the selected contacts sharing that [bike users name] has started a ride from [location] at [time]. The user, now wants to stop sharing their ride with the previously selected users. The user can open the app, press “currently sharing with” button at the bottom left and then deselect the contact(s) they are sharing with. The user is no longer sharing their ride details with the contact.

6.) The user must have the bike ride sharing app installed and a user account.

The user must have allowed the bike ride sharing app access to their contacts

The user must be unlocking a bike and having a ride in process

The contact selected must have a valid SMS number to send the ride notification to

7.) The user must have re-locked the bike at a destination terminal

The contact has received the notification via SMS from the bike ride sharing app that the biking user has finished their ride

8.) The user must have a valid credit card inputted into the app to be accepted as payment

The user must have a compatible operating system on their phone to have the bike ride sharing app

The user must have the contacts that they want to share their ride with already in their phone as contacts

The user must allow access  full phone access to the ride sharing app

******USE CASE 2******

1.) Re-Locking Bike

2.) Once a user is done using their bike they must find a bike hub/terminal to re-lock the bike. When relocking the bike the terminal will beep and flash a green light to show that the bike has been locked or a red light to show that there has been an error when attempting to relock the bike

3.) Bike User Bike

4.) BASIC FLOW: The user who has an unlocked bike is finished with their ride and at a bike hub/terminal to return their bike. The user will put the bike in a bike-rack slot and wait for the terminal to beep and a light to flash green to ensure that the bike has been properly locked. The user will receive an SMS to let them know that the ride is over (the bike was securely returned), how much they were charged and how long their ride was.

5.) FIRST ALTERNATE FLOW: The user who has an unlocked bike is finished with their ride and at a bike hub/terminal to return their bike. The user will put the bike in a bike-rack slot, but the light turns red. The user is aware that the bike was not re-locked and attempts to lock the bike again. After attempting again the light turns green and the terminal beeps to notify the user that the bike has been properly locked. The user will receive an SMS to let them know that the ride is over (the bike was securely returned), how much they were charged and how long their ride was.

SECOND ALTERNATE FLOW: The user who has an unlocked bike is finished with their ride and at a bike hub/terminal to return their bike. The user will put the bike in a bike-rack slot, but the light turns red. The user is aware that the bike was not re-locked and attempts to lock the bike again. After attempting again the light still does not turn red. The user believes that the terminal is faulty and opens the app to call for “Bike Support”. An employee on call will arrive at the site to assist them and address any errors. The bike is manually inserted into the bike sharing system as “returned” by the employee and the user receives an SMS to let them know that the ride is over (the bike was securely returned), how much they were charged and how long their ride was.

6.) The user must have the bike ride sharing app installed and a user account.

The user must be in an active bike ride/ have a bike unlocked

The user must have a valid SMS number to send the ride notification to

7.) The user must have re-locked the bike at a destination terminal OR an bike employee has came to manually re-lock the bike as per the system

The user has received the notification via SMS from the bike ride sharing app that the biking user has finished their ride

8.) The user must have a valid credit card inputted into the app to be accepted as payment

The user must have a compatible operating system on their phone to have the bike ride sharing app

The user must have the contacts that they want to share their ride with already in their phone as contacts

The user must allow access  full phone access to the ride sharing app