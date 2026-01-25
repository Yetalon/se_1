# Software Engineering — Day 6
## Topic: Design + Design Patterns 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**Design fundamentals: the “HOW”**](#design-fundamentals-the-how) | What “design” means in SE, and why we do it | Identify what design artifacts you’d produce |
| [**Design levels**](#design-levels-architecture--high--mid--detailed) | Architecture → High → Mid → Detailed design | Map an example system across levels |
| [**Keeping design useful**](#keeping-design-useful-not-shelfware) | Avoid “too much,” “too little,” and “stale” designs | Note what must be version-controlled |
| [**Design patterns primer**](#design-patterns-primer) | Why patterns exist (benefits + risks) | Don’t cargo-cult; focus on intent |
| [**The 7 patterns to know**](#the-7-patterns-to-know) | Singleton, Factory, Strategy, Observer, Builder, Adapter, State | Write a 1-sentence “when to use” each |
| [**In-class discussion**](#in-class-discussion) | “How do you know you’re done with design?” | Bring a criterion-based answer |

---

## Main objectives
1) Understand design as the bridge from requirements (“what”) to implementation (“code”) 
2) Learn the four design levels and what each focuses on (architecture → detailed) 
3) Know common pitfalls: over-design (waterfall) vs under/unstated design (misread agile) 
4) Get a working mental model for design patterns and seven commonly useful patterns (from the provided reading)  

---

## Design fundamentals: the HOW
- **Design** turns requirements into a plan for implementation—recursively adding detail until the solution can be built. 
- The course frames design as documenting **how the problem will be solved**, usually with diagrams/models like UML. 
- A key design action is **breaking down the big problem** into smaller solvable parts. 

**Added context:** Design is also communication. It prevents different developers from making incompatible assumptions.

---

## Design levels: Architecture → High → Mid → Detailed

### Architecture design
- Focus: interactions between applications/systems; often starts from a known architecture (e.g., client/server) and tailors it. 
- Addresses major “ilities” like **scalability** and **security**, shared data model, and usage profiles to help size hardware needs. 

**Added context:** This is where big tradeoffs happen (e.g., monolith vs microservices) because they constrain everything below.

### High-level design
- Focus: interactions within a system/application (data, control, communication). 
- Identifies modules/packages/services/subsystems; often use-case driven. 

### Mid-level design
- Focus: interactions within a module/service/subsystem; bridges high-level and detailed. 
- Often uses design patterns here; may identify classes but not full class detail. 

### Detailed design
- Focus: class-level details (UML class diagrams, ERDs, method design). 
- Tooling can reverse engineer diagrams from code. 

---

## Keeping design useful (not shelfware)
- **Waterfall risk:** spending too much time designing. 
- **Iterative/agile risk:** designs don’t get updated as iterations change the system; older designs aren’t maintained in version control. 
- **Agile misread:** “just enough design” ≠ “no design.” 

**Added context (practical rule):** Write down decisions that would be expensive to rediscover: interfaces, core data model assumptions, and the riskiest flows.

---

## Design patterns primer
From the provided reading, patterns help because they:
- prevent reinventing the wheel,
- provide a shared team vocabulary,
- help you solve recurring design problems—**if you understand why/how**, not just the name. (source: learningdaily.dev link)

**Added context:** Patterns add indirection. Use them when the flexibility/decoupling benefit is worth the complexity cost.

---

## The 7 patterns to know
(From the provided reading: Singleton, Factory Method, Strategy, Observer, Builder, Adapter, State.)

### 1) Singleton
- Intent: one instance + global access (e.g., shared resources like caches/registries).
- Risk: accidental global state (harder testing, hidden coupling).

### 2) Factory Method
- Intent: create objects without binding code to concrete classes.
- Use when: creation logic varies by type/config/environment.

### 3) Strategy
- Intent: swap algorithms/policies without changing the client.
- Use when: multiple ways to do the same job (pricing rules, routing, sorting policy).

### 4) Observer
- Intent: one-to-many updates; subscribers notified when subject changes.
- Use when: event-driven updates (UI listeners, pub/sub).

### 5) Builder
- Intent: construct complex objects step-by-step (many optional params).
- Use when: object creation becomes messy with constructors.

### 6) Adapter
- Intent: translate one interface to another so incompatible parts can work together.
- Use when: integrating external libs/systems with mismatched APIs.

### 7) State
- Intent: change behavior based on internal state; avoid giant if/else ladders.
- Use when: workflow/state machines (connection states, UI states).

---

## In-class discussion
Prompt from the slide deck:
- **How do you know you are done with the Design phase?** 

**Answer frame (bring to class):**
- You’re “done” when the design covers requirements at the needed detail, key risks are resolved, and implementation can be estimated and assigned without major unknowns.
