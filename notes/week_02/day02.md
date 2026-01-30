# Software Engineering — Day 2
## Topic: Problem Solving (a.k.a. “life”) 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | The big outcomes for Day 2 | Skim first to orient yourself |
| [**Task vs Problem**](#objective-1--problem-solving-is-more-than-having-steps) | How to recognize when you’re “executing steps” vs truly solving | Use the guiding questions to clarify ambiguity |
| [**Decomposition & recursion**](#objective-2--break-the-big-problem-into-smaller-solvable-problems) | How to break a problem down until each piece is solvable | Practice splitting problems + checking coverage (“union = original”) |
| [**SDLC mapping**](#objective-3--map-problem-solving-onto-the-sdlc) | How problem solving aligns with Requirements → Design → Implementation → Testing | Keep “what vs how” straight; note constraints |
| [**Testing as verification**](#objective-4--testing-is-unwinding-the-recursion-and-proving-you-solved-the-real-problem) | Why testing is “unwinding” your decomposition path | Think unit → subsystem → system |
| [**Your process (reflection)**](#objective-5--build-self-awareness-how-you-solve-problems) | Put your own approach into words | Write a short description of your process |
| [**Raptor activity**](#in-class-exercise--raptor-problem-solving-flowcharts) | Flowchart-based problem solving in Raptor | Install Raptor + be ready to solve a prompt |
| [**Warm-up puzzle**](#quick-warm-up-activity--the-peanut-in-the-test-tube-puzzle) | Reframing constraints and assumptions | Brainstorm before watching the demo |

## Main objectives
1) Distinguish “tasks” vs “problems” (and why that matters in software engineering) 
2) Practice breaking down ambiguous problems into solvable parts (recursion as a process) 
3) Connect problem-solving to the SDLC and the requirements → design → implementation → testing pipeline 
4) Reflect on your personal problem-solving process and prepare for a Raptor-based activity 

---

## Objective 1 — Problem solving is more than “having steps”
### Core ideas (classic framing)
A common “textbook” problem-solving loop looks like: **define the problem → list possible solutions → evaluate → test**. 

**Added context:** This works well when:
- the problem is already well-defined,
- solution options are known,
- the main risk is picking the *best* option rather than figuring out what’s even possible.

### What the instructor is emphasizing instead (task vs problem)
- If there’s an **obvious list of solutions**, it’s often a **task to complete**, not a “problem to solve.” 
- A real problem usually starts as “something without a clear solution,” so the first move is **understanding why it’s a problem**, not immediately “defining” it. 

**Added context:** In software engineering, a huge chunk of difficulty comes from ambiguity:
- vague goals (“make it faster / more user-friendly”),
- hidden constraints (deadline, tech stack, compliance),
- changing requirements (stakeholders learn what they want by seeing versions).

### Helpful “problem-understanding” questions
From the deck:
- What goal is being blocked?
- Who is involved and what resources exist?
- What’s been tried already?
- Is it similar to something solved before? 

**Added context:** These questions are basically “requirements discovery” in plain English.

---

## Objective 2 — Break the big problem into smaller solvable problems
### Core idea: decomposition + recursion
- Break the problem into **smaller, more solvable parts**.
- The parts should “add back up” to the original problem (coverage matters).
- If a part still has no obvious solution, repeat the process (recursion). 

**Added context (why “union equals the original problem” matters):**
It’s easy to decompose and accidentally *omit* something important (edge cases, non-functional needs like security/performance, operational concerns like logging/monitoring). “Union = original” is a reminder to avoid blind spots.

---

## Objective 3 — Map problem solving onto the SDLC
### SDLC phases (as framed in the deck)
Software engineering projects commonly move through:
- Problem Solving
- Requirements
- Design
- Implementation
- Test
- Release
- Support/Maintenance
- Upgrades/Updates 

**Added context:** Different books compress or rename phases, but the *idea* is consistent:
- start with uncertainty,
- progressively reduce it with documentation and decisions,
- validate the result,
- then keep it alive in the real world.

### Requirements vs Design (the “what” vs “how” split)
- **Requirements** document the problem: **what needs to be done**. 
- Requirements analysis breaks requirements down until they’re solvable. 
- **Design** documents the solution direction: **how it should be done**. 

**Added context: constraints**
The presenter notes mention an important exception: “requirements shouldn’t say *how*” — except for **constraints** (mandated language/stack/architecture, legal rules, safety constraints, etc.). Those are “non-negotiable how/shape” items that box in design choices.

### Designs also become problems (recursion continues)
- Designs are a solution to requirements, but also a new “problem” that must be solved into more detailed designs.
- Implementation is the solution to the design (software/hardware or both). 

**Added context:** This is how big systems get built without magic:
- high-level design (components + interactions),
- detailed design (interfaces + data + algorithms),
- implementation (actual code + infrastructure).

---

## Objective 4 — Testing is “unwinding” the recursion and proving you solved the real problem
### Testing as verification
- The full implementation is usually *intended* to be the solution, but it must be tested to verify it really solves the problem. 
- Testing is described as “unwinding the recursive path” that got us here. 

**Added context (what “unwinding” means):**
You broke the problem down into pieces to build it. Testing works outward:
- validate individual units,
- then validate groups of units,
- then validate the whole system against the original goals.

### Test levels (from presenter notes; terminology may vary by org)
- **Unit tests:** test an individual “unit” of code (often a function/class).
- **Subsystem / integration-ish tests:** test a group of units that together implement a bigger component.
- **System tests:** test the whole solution end-to-end.

**Added context:** Some orgs use different names (“integration tests”, “component tests”, “end-to-end tests”), but the scaling idea is the same: confidence grows as you test closer to real usage.

---

## Objective 5 — Build self-awareness: *how* you solve problems
The deck prompts you to articulate your own process:
- “Do you know how you do it?”
- “Try to describe in writing how you do it.” 

### In-class exercise (reflection)
Write a short description of your typical workflow when the solution isn’t obvious. Use prompts like:
- How do you clarify the goal?
- How do you split it into parts?
- How do you decide what to try first?
- How do you verify you’re done?

*(If your instructor treats this as a submission, it becomes homework—nothing in the slide explicitly says “due,” so I’m labeling it primarily as an in-class reflection.)* 

---

## In-class exercise — Raptor problem solving (flowcharts)
You’ll need **Raptor** (free) for the in-class activity. 

### In-class exercise (call to action)
- Download and install: https://raptor.martincarlisle.com/ 
- In class: you’ll select from a short list of problems and solve them using Raptor (flowchart-style programming).

**Added context:** Raptor is great for forcing clarity on:
- control flow (sequence/selection/iteration),
- algorithm steps,
- inputs/outputs and edge cases,
before you ever touch a “real” programming language.


## status report
- map lifecycle to other life experiences

- two requirements that are very important
    - mandatory
    - optional

- write problem solving methodology

---

## Quick warm-up activity — The “peanut in the test tube” puzzle
Prompt:
- Test tube is stuck vertically to a wall and can’t be moved.
- Peanut is inside at the bottom.
- Get it out; think of solutions *before* watching the video. 


### In-class exercise (call to action)
- Spend 2–3 minutes brainstorming solutions, then watch the demo video. 

**Added context (why this matters):**
This puzzle is about **reframing constraints** and using available resources. In software, the “peanut” is the goal, the “tube” is constraints, and the trick is often realizing you can change something you *assumed* was fixed (inputs, environment, representation, available tools).


### options

high low guessing game 1-10 ints at random solicites numbers from user. if the user put a number high than the user put it it needs to display lower. if they guess too lower it says higher. if they guess exactly the correct number it says correct. gamecycle if they guess correctly they have the option to play again. if they get it right again they get another option to play again and if they get it right the third time then the program exits. maximum guesses 5. instructions at the begining of the game. 

    - the band from 1 to 10 is inclusive
    - the doofus rule
        - if they input a string they are not following the instructions. keep track of that and if they guess same number multiple times or they guess 3 and it says higher and the go lower that is a doofus rule. if they do it 3 times in a row you tell them they are a doofus and the program exits. if they are a doofus twice but then do the rules their record is clear but if they do a doofus ever other valid guess and that is fine.

second option write a program that is a variant to the high low. No user the program it's self will generate a random guess. print out the guess with the approriate responses but there is no user. once the computer guesses the correct one that the computer came up with prompting for playing again up to 3 times. it should follow the instructions based on what has been provided to it.

third choice a program called 5 player poker deal. The program will take a standard deck of cards shuffle it and then deal 5 cards to each 5 players. list on the screen the cards that were delt each players cards are shown on a seperate line.

    - 4 suits of 13 cards.
    - 

fourth option is road trip. given a distance in miles and a average speed limit in miles per hour by a user. calculate how long it will take in time to reach the destination. then calculate how long it would take if you drove 5 hours over the limit. and then 10 miles over the speed limit. and then 15 miles over the speed limit. lastly 20 miles over the speed limit. the miles per hour over the speed limit can be a input. the time if its over 60 minutes display the number of hours and the number of minutes but not the seconds. if its less then 60 minutes then just give the minutes and drop the seconds on the floor. maximum of the combine speed limit and the amount over the speed limit cannot exceed 120 miles per hour.

    - upper limit around 3500 miles.
    - speed limit comes from the user and along side mileage.
    - lower bound of 25 mph
    - can be in console.

    - if there is a invalid input should they be reprompted
    - should the mph be a integer, should the distance be a integer.
    - 
