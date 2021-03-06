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
* Making production deploys and changes routine
  * Dog fooding/dark launch: Deploy into production for internal employees and a small cohort of real users (feature flag)
  > This has many befinits: 
  > * Early feedbacks from real users allowing problems to be found and fixed quickly
  > * Generates learnings early in the process
  > * Hypothesis-driven culture: we do nothing without measuring and treating product development and process improvement as experiments.
  > This ensures we don't build feature that no one wants or don't spend time fixing things that aren't real problems
  > *"Repitition creates mastery"*
* Long-term teams focused on achieving clear goals
  * Keeping teams intact so they can keep iterating and improving using feeback learnings
* High-trust, collaborative culture where people are rewarded for taking risks
  * Blameless incident post mortems
  > *"We must see our problems in order to solve them"*
  * Management's main goal is to enable engineers and developers to create value by removing obstacles and creating a safe environment.
* All improvement made outside the constraint is an illusion
  > Theory of contraints: all system is bottlenecked by at least one contraint
  > To solve this, we must
  > 1. **Identify** the constraint (it can be people, process, program, etc.)
  > 2. Decide how to **exploit** the constraint
  > 3. Make the above (point 2) a top priority
  > 4. Elevate the system's constraint
  > 5. Loop back to first step (continuous improvement)
  > A constraint is broken (or solved) when it is no longer the system's limiting factor, increasing throughput, enabling the flow of work.
* Continuous improvement - Improvement Kata
  * Pay technical debt: choices and tradeoffs have to be made when implementing a change, usually ending in adding technical debt. A routine must be created to continuously reflect on what should be improved and fixed and allocate time and effort to implement it. 
  * Due do entropy, all systems will naturaly tend to disorder over time, requirement constant improvement to keep the same level of stability and performance.



