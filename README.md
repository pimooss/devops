# DevOps Principles and Resouces

This humble repository contains some personal notes and ideas on DevOps principles and methods.

My main sources of inspiration for this content are
* The Phoenix Project by Gene Kim, Kevin Behr and George Spafford (If you haven't read it yet, I'd suggest to do so, it's a great book)
* The DevOps Handbook
* The Unicorn Project by Gene Kim
* My work at TradeMe as a Senior System Engineer for the past 4 years
* 18 years of experience in IT, from the small startup to the $10B per year pharmaceutical corporation.

## Cheat Sheets

### Jargon (in the IT context)

* Technical Debt: describes how decisions we make lead to problems that get increasingly more difficult to fix over time (on top of natural entropy)
* Entropy: constant gradual decline into disorder
* 

### The Problem

Competing goals of **development** and **IT operations**:
* Development: Respond quickly to the market by creating features and deploying them into production.
* IT Operations: Provide stable, reliale and secure service to the customer making it difficult to introduce change in production.

Over time, the above configuration creates a downward spiral resulting in slowing down product delivery cicles, feedback loop and fragilises infrastructure.

### A Better Way

Key points and examples
* Fast feedback loop (fail fast) on every step: I am immediatly able to the see the effect of my action.
  * Everything is in code into version control (infrastructure as code)
  * Automated tests in production-like envirement at each commit
  * Telemetry both in code and infrastructure environments to ensure problems are detected and corrected quickly
  * Self service platforms (removing IT operation's "gate keeper" unwanted role)
  > In my mind it is a similar principle I use when I'm writing a script or a program, I would run it at almost every step of the way to check it is giving the desired outcome. On the same level, I would check for execution time and resource usage (memory/cpu) to ensure I didn't introduce an undesired/unecessary load intensive element.
  > 
* Making production deploys and changes routine
  * Dog fooding/dark launch: Deploy into production for internal employees and a small cohort of real users (feature flag)
  > This has many befinits: 
  > * Early feedbacks from real users allowing problems to be found and fixed quickly
  > * Generates learnings early in the process
  > * Hypothesis-driven culture: we do nothing without measuring and treating product development and process improvement as experiments.
  > This ensures we don't build feature that no one wants or don't spend time fixing things that aren't real problems
* Long-term teams focused on achieving clear goals
  * Keeping teams impact
* High-trust, collaborative culture where people are rewarded for taking risks
  * Blameless incident post mortems
  > *"We must see our problems in order to solve them"*


