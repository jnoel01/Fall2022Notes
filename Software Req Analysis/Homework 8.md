# Homework 8

> ************PROBLEM************
> 
> 
> Imagine you are a security engineer and have analyzed a software platform / app and uncovered a security vulnerability.
> 
> Your analysis has concluded following aspects --
> 
> - The vulnerability can be discovered through some reasonably simple network data analysis / traces, diagnostics
> - if exploited, it could affect some users but not all
> - it is not too difficult to exploit it as some malware / attack scripts may already exist
> - it can be reproduced / replicated with reasonable steps to show that it is real and can happen
> - the damage maybe to user data but not necessarily entire system wide
> 
> Answer the following:
> 
> 1. With this assessment, determine Risk score of this scenarios.
> 2. Write down specifically how you arrived at the Risk score

1.)

Using DREAD, developed by Microsoft I will determine the Risk Score

**D**amage potential: How great is the damage? 5

**R**eproducibility: How easy is it to reproduce the attack? 5

**E**xploitability: How easy is it to launch the attack? 5

**A**ffected users: How many users are affected? 5

**D**iscoverability: How easy is it to discover the vulnerability? 5

Risk = (D + R + E + A + D) /5

Risk = 5 + 5 + 5 + 5 + 5 → 25/5 → 5

RIsk = 5

2.)

To calculate the Risk score I used DREAD developed by Microsoft. DREAD stands for damage potential, reproducibility, exploitability, affected users and discoverability. For damage potential we must asses if a threat exploit occurs, how much damage will be caused, since only individual user data is compromised or affected and not the entire system the damage potential is 5. For reproducibility we must asses how easy it is to reproduce the threat that is being exploited, according to the problem it can be replicated with reasonable steps; because there are a few steps required and it is not just available from a web browser and address bar it’s ranked as a 5. For exploitability we must assess what an individual needs to exploit the threat. Again, the problem states that it is not difficult to reproduce and only needs some malware or existing attack scripts and not just a web browser, therefore it is ranked as a 5. For affected users we must asses how many users will be affected, as previously stated only a few users are affected, therefore it is ranked as a 5. Lastly, for discoverability we must asses how easy it is to discover the threat. In the problem it states that we can “discover it through some reasonably simple network data analysis / traces, diagnostics”. An individual can not discover it in the public domain and it is not visible in the web browser/address bar or form therefore it is ranked as a 5. With the corresponding numbers to each of the sections of DREAD we can calculate the risk by doing a simple equation: $Risk = (D+R+E+A+D)/5$. When plugging in the numbers I assessed we get $Risk = (5+5+5+5+5)/5$, simplifying this equation we will find that the Risk score is 5.