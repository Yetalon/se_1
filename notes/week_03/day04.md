# Software Engineering — Day 4
## Topics: Lifecycle Models + CMMI (Made Simple) 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**Lifecycle phases & “you’ve already done this”**](#objective-1--understand-the-software-lifecycle-and-realize-youve-already-used-it) | Requirements → Design → Implementation → Test → Release → Support → Upgrades | Map your past assignments to lifecycle phases |
| [**Deliverables & versioning**](#objective-2--understand-deliverables-artifacts-and-why-they-must-be-versioned) | What artifacts exist per phase + why they aren’t “static” | Learn the deliverable list; notice traceability |
| [**Verification in every phase**](#objective-3--verification-happens-throughout-the-lifecycle-not-just-testing) | Reviews and analysis at each phase | Identify what “verification” looks like per phase |
| [**Round-trip / reverse engineering**](#objective-4--360-engineering-round-trip-engineering-and-keeping-design-in-sync-with-code) | Why design/code drift happens and how tools regenerate diagrams | Remember: code evolves → diagrams must follow |
| [**Lifecycle models (Waterfall / Iterative / Agile)**](#objective-5--choose-the-right-lifecycle-model-for-the-right-kind-of-product) | Match product types to the right model | Practice categorizing examples |
| [**CMMI maturity levels**](#objective-6--understand-cmmi-as-an-organization-maturity-ladder) | What CMMI is + what each level “feels like” | Use the Bob’s Tire Repair analogy to remember levels |

---

## Main objectives
1) Understand the **software engineering lifecycle phases** and how they show up in class + real projects 
2) Learn what **deliverables/artifacts** exist in each phase and why they must be versioned 
3) Understand that **verification** happens in *every* phase (not just “testing at the end”) 
4) Compare common **lifecycle models**: Waterfall vs Iterative/Spiral vs Agile/Scrum 
5) Understand **CMMI** as a model of organizational process maturity 

---

## Objective 1 — Understand the software lifecycle (and realize you’ve already used it)
### Core lifecycle phases
The deck states that software goes through the same lifecycle:
**Requirements → Design → Implementation → Test → Release → Support/Maintenance → Upgrades/Updates** 

### “Stuff you’ve done” mapping (course-to-real-world translation)
You’ve already done each phase in school:
- Someone told you what to code = **Requirements** 
- You thought through how to do it = **Design** 
- You wrote the code = **Implementation** 
- You checked that it worked = **Test** 
- You turned it in = **Release** 
- You fixed issues from feedback = **Support/Maintenance** 
- You added features or reused it later = **Upgrades/Updates** 

**Added context:** The key shift “in the real world” is *scale and accountability*:
- stakeholders pay for it,
- teams specialize (architect, dev, QA, release, support),
- deliverables and documentation matter because work is shared across people/time. 

---

## Objective 2 — Understand deliverables (artifacts) and why they must be versioned
### Artifacts are not static
The deck emphasizes: deliverables are rarely static and must be **versioned along with releases**. 

### Example artifacts per phase
- **Requirements:** mandatory/optional; functional/non-functional 
- **Design:** architecture/high-level/detailed-level; traceability matrix 
- **Implementation:** code/scripts/hardware; traceability matrix 
- **Test:** test plan/test cases/traceability matrix 
- **Release:** release procedures/scripts/release notes 
- **Support/Maintenance:** usually bug fixes → mainly release notes updates or README changes 
- **Upgrades/Updates:** iterative cycle of the above 

**Added context (traceability matrix):**
A traceability matrix is basically “proof the chain exists”:
- requirement → design element → implemented component → test that validates it.
It prevents “we built something, but not what was asked.”

---

## Objective 3 — Verification happens throughout the lifecycle (not just testing)
The deck lists verification activities per phase:

- **Requirements:** requirements review and analysis 
- **Design:** design review and analysis 
- **Implementation:** code reviews, unit testing, static analysis, etc. 
- **Testing:** test plan/test case review and analysis 
- **Release:** release plan review and analysis 
- **Maintenance & upgrades:** “all of the above again” 

**Added context:** Verification early is cheaper than debugging late:
- catching a misunderstood requirement early saves rework,
- catching a design flaw before coding saves weeks,
- code review catches defects before they become production incidents.

---

## Objective 4 — 360 engineering (round-trip engineering) and keeping design in sync with code
The deck describes:
- “Round Trip Engineering” / “Reverse Engineering”
- A feature of OO development tools
- A common failure: **detailed design documents drift from the code** because implementation evolves
- Many IDEs can **regenerate detailed design diagrams** from code 

**Added context:** This is why “documentation debt” happens:
- design is written once,
- code changes 20 times,
- diagram lies.
Round-trip tools reduce drift by making diagrams derivable from the codebase.

---

## Objective 5 — Choose the right lifecycle model for the right kind of product
The deck uses examples to highlight three common models.

### Waterfall model
Characteristics:
- single pass through lifecycle with one big release 
- used when features must work together at once and updates are infrequent or impossible 
- not “evil/old” — it has a purpose 

Examples given (type of products):
Airplane, satellite, Mars rover, microwave, car, pre-internet TurboTax-style product 

**Added context:** Waterfall fits high-risk, high-cost-of-failure systems where change is expensive and deployment is rare.

### Iterative / Spiral model
Characteristics:
- first release may resemble waterfall but with a minimum feature set 
- expectation of periodic upgrades/updates with fixes + new features 

Examples:
Operating system, downloadable game, accounting software, ERP (PeopleSoft/SAP) 

**Added context:** Iterative is common when you can ship “v1” and improve on a predictable cadence (patches/releases).

### Agile / Scrum model
Characteristics:
- highly involved/available customer 
- environment supports frequent updates/upgrades 
- incremental changes won’t disrupt customers; product evolves naturally 

Examples:
Web portal, cloud-based solutions (Google/Facebook/TikTok), custom solutions for involved client, web-enabled devices that accept downloads 

**Added context:** Agile is less about “no plan” and more about:
- planning in shorter cycles,
- tight feedback loops,
- and accepting that requirements evolve.

### Meta-point: companies tailor models
The deck says most companies adapt/tailor models to their needs; understanding common models helps you adapt faster. 

---

## Objective 6 — Understand CMMI as an organization maturity ladder
### What CMMI is (as introduced here)
- **CMMI = Capability Maturity Model Integration** 
- The lifecycle deck suggests this is a good time to read the CMMI materials (in a separate presentation) 
- It loosely relates to organizational development (Tuckman: forming, storming, norming, performing) 

### “CMMI Made Simple” analogy (Bob’s Tire Repair)
This deck expresses levels through naming maturity:

- **Level 0:** Bob’s Tire Repair 
- **Level 1:** Bob’s Auto Tire Repair 
- **Level 2:** Bob’s Reliable Auto Tire Repair 
- **Level 3:** Reliable Auto Tire Repair 
- **Level 4:** Speedy, Reliable Tire Repair 
- **Level 5:** Speedy, Reliable Tire Repair & Sales, Inc 

**Added context (how to remember this):**
- As the level increases, the name implies more **consistency**, **predictability**, and **organizational maturity** (reliability, speed, expanded capabilities).
- Think: “from informal → managed → defined → measured → optimizing” (common maturity ladder idea), but the deck’s key is the easy-to-recall “Bob’s…” evolution. 

---

## In-class exercises — Calls to action

### In-class exercise: Map your past work to lifecycle phases
Pick a past coding assignment and label:
- requirements (what the teacher asked),
- design (how you planned it),
- implementation (code),
- test (how you validated),
- release (submission),
- maintenance (fixes after feedback),
- upgrade (features added later). 

### In-class exercise: Classify products by lifecycle model
Use the provided examples and justify why they fit:
- Airplane / rover → Waterfall
- OS / downloadable game → Iterative
- web portal / cloud app → Agile 

---

## Homework
No explicit “due” items were stated in these decks. If your instructor assigns:
- “read the CMMI materials” as a graded task, or
- requires a lifecycle-model classification writeup,
then those would become homework—but the slides themselves only suggest timing (“great place… to read CMMI materials”). 
