# M5.B1: Homework 5 Paired Programming

```
We discussed pair programming in the lecture, and this assignment offers you a 
chance to try it.

Choose two user stories from your GEDCOM backlog.
Choose a pair programming partner from your GEDCOM team, along with one of your two GEDCOM user stories. Sit together, either physically together in the same 
place or virtually together using a screen sharing program such as Google 
Hangouts. (A single person may pair a program with more than one person if your GEDCOM has an odd number of people.)
As a team, pick three user stories. For each team member, implement one of the 
two user stories by yourself, noting the time it takes for you to solve the 
problem. The second user story implements it using the pair programming 
technique. Each person should be sure to fill the role of both driver and 
navigator. Note the time you spent implementing the user stories while working 
independently and while pair programming.

**Deliverables:**

Describe your experience implementing the two user stories, including the 
following details:

Identify your pair programming partner.
Identify the user story you implemented alone.
Describe your experience working alone on the user story. How long did it take 
to implement and test the story?
Describe your experience working with a pair programming partner on the user 
story. How long did it take to implement and test the story?
Describe the advantages and disadvantages for you and your teammate while pair 
programming. What worked well? What didn't work well?
Would you recommend pair programming? Why or why not?
Will you use pair programming on future GEDCOM user stories? Why or why not?
```

My paired programmer partner was Brendan Probst. I started by implementing a user story that asserted ones death must be before 150 years after their birth. Because this user story was fairly simple it took me about 3 minutes to code and 2 minutes to test alone- it was a 3 line function total. The next story that I worked out was the fathers death must be after the conception of his child; I pair programmed this user story. This story took more time than the one I did alone both because it was harder and because Brendan and I have different ways of thinking. My approach was to import relativedate so that I could subtract and add dates, but his approach was utilizing the already made dictionary from last Sprint. The way I code is always to find the shortest way to do it, especially if it’s in python where there are tons of built in function to use. Brendans way seems to be “don’t use any libraries I’m not familiar with”. Though Brendan helped me to finish the code, about 4 of the 9 minutes were spent explaining our different logic to one another. Overall it took 15 minutes to code and test which was longer than when I coded alone. I think pair programming can be advantageous though when an assignment is difficult and multiple view points are necessary. This is why I would recommend pair programming to a friend. However, personally I will not use pair programming in the future GEDCOM sprints, mainly because we all have different ways we’d solve a problem (and one way might be more efficient) but with an assignment like this where time complexity is not important there is no point spending extra time explaining our thought processes then coding. Besides, our group tends to code in a VSCode live share so if anyone runs into any confusion while coding, we will help that person.