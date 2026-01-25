# Software Engineering — Day 12
## Topic: Waterfall (The “Big Bang” Lifecycle Model) 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**What Waterfall is**](#objective-1--what-waterfall-is) | Waterfall as the classic SE lifecycle model + “one stage at a time” idea | Be able to describe Waterfall in 2–3 sentences |
| [**How Waterfall works**](#objective-2--how-waterfall-works-stages-prepostconditions-verification) | Stages, pre/post-conditions, verification at each stage, minimal change mgmt | Identify preconditions/postconditions for 2 stages |
| [**When Waterfall is best**](#objective-3--when-waterfall-is-best) | The situations where Waterfall is the right tool | Match examples to “why Waterfall fits” |
| [**Tradeoffs and implications**](#objective-4--waterfall-tradeoffs-what-changes-in-projects) | More documentation, longer timelines, higher rigor, less flexibility | Explain 3 pros and 3 cons |
| [**Examples of Waterfall projects**](#objective-5--examples-of-waterfall-projects) | Real domains that commonly fit Waterfall | Classify a system as Waterfall vs not |
| [**Artifacts by stage**](#objective-6--waterfall-artifacts-what-you-produce) | What documents and deliverables exist per phase | Memorize the “artifact buckets” |
| [**In-class prompts**](#in-class-prompts--calls-to-action) | How to apply this model | Practice the “choose the model” justification |

---

## Main objectives
1) Understand Waterfall as a lifecycle model rooted in the 1970s and foundational to common SE phases 
2) Know how Waterfall progresses stage-by-stage with pre/post-conditions and verification activities at each stage 
3) Recognize when Waterfall is the best fit (mission/life-safety, rigorous requirements, difficult updates) 
4) Understand the tradeoffs: rigor, documentation, long timelines, reduced reliance on tribal knowledge, heavier validation 
5) Identify common Waterfall project examples and the typical artifacts produced in each stage 

---

## Objective 1 — What Waterfall is
- Waterfall is described as **“the Big Bang approach”** lifecycle model. 
- It dates back to the **1970s** and serves as the basis for the familiar SE lifecycle phases. 
- In its “pure” form, **only one stage is active at a time**. 

**Added context:** “Big Bang” here means you do a long build-up of phases and deliver a major release at the end, rather than shipping frequent incremental releases.

---

## Objective 2 — How Waterfall works (stages, pre/postconditions, verification)
- Each stage has **preconditions and postconditions** (similar framing to UML method design). 
- There are **verification activities for each stage**, not just at the end. 
- Change management is described as **minimal** compared to iterative models. 

**Added context:** Waterfall assumes requirements are stable enough that heavy up-front work won’t be invalidated by constant changes.

---

## Objective 3 — When Waterfall is best
Waterfall is best when:
- Projects are **mission critical / business critical / life safety** 
- Requirements are **rigorous and well-defined** 
- **All features must exist and must all work properly together** 
- Updates/upgrades/patches are **difficult** 
- Systems are **massive** (hundreds of developers) 
- **Completeness/correctness** are higher priority than cost or schedule 

---

## Objective 4 — Waterfall tradeoffs (what changes in projects)
The deck calls out that with Waterfall:
- Change management is minimal
- Verification at each stage is more rigorous
- Architecture doesn’t need to be as extensible/malleable
- Designs tend to be more complex
- Projects take **months or years** to complete
- There is **more documentation** and **less tribal knowledge**
- Validation becomes even more significant 

**Added context (practical takeaway):**
- Waterfall “buys” predictability and rigor by paying in time + flexibility.
- Documentation is not just bureaucracy—it’s how large or long-lived teams avoid knowledge loss.

---

## Objective 5 — Examples of Waterfall projects
Examples listed:
- Avionics, satellite, submarine, nuclear reactor, missile systems, self-driving cars 
- Healthcare devices/systems: pacemakers, CAT scan, cancer treatment, insulin pumps, dialysis machines 
- Embedded/remote systems: traffic signals (some becoming connected), electric substations/RTUs, vending machines (some becoming connected) 

**Added context:** These domains share a theme: failure is expensive/dangerous, and updates in the field may be hard or heavily regulated.

---

## Objective 6 — Waterfall artifacts (what you produce)
### Overarching (project-level) artifacts
- Overarching project plan/schedule
- Change management process/guidelines
- Risk management process/guidelines
- Standards and practices document (requirements/design/coding/scripting/docs)
- Staffing plan (sometimes part of project plan) 

### Requirements stage artifacts
- Requirements specification
- Functional and non-functional systems specification (may be a section)
- Acceptance criteria 

### Design stage artifacts
- Architectural design document
- External API specification
- Network design
- Systems design docs (one per system in the solution)
- Detailed design docs (one per system)
- System & integration test plans
- Acceptance test plan 

### Implementation stage artifacts
- Software including scripts/stored procedures/unit tests
- Network installation docs and scripts
- Acceptance/system/integration test cases documented 

### Test stage artifacts
- Release plan
- Acceptance/system/integration test results for all pre-production environments 

**Added context:** Notice how Waterfall heavily emphasizes artifacts that support verification/validation and repeatability across long timelines.

---

## In-class prompts — Calls to action
### In-class exercise: “Choose the model”
Given a system scenario, justify:
- Why Waterfall is appropriate (or not)
- Which factor is decisive (life safety? patch difficulty? requirements stability?) 

### Quick study question (good exam prompt)
- “Why is validation more significant in Waterfall?”  
Because you typically have a bigger end release (“big bang”), requirements are assumed stable, and the cost of discovering you built the wrong thing late is enormous. 
