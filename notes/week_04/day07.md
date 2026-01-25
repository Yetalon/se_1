# Software Engineering — Day 7
## Topic: Implementation (More than “just coding”) 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**What “implementation” really includes**](#objective-1--implementation-is-more-than-just-writing-code) | All the non-code work that still counts as implementation | Make a checklist for your next project |
| [**Agile vs non-agile implementation timing**](#objective-2--agile-vs-non-agile-when-implementation-starts) | When you start coding and why it differs by lifecycle | Explain the tradeoff in 2–3 sentences |
| [**Characteristics of good implementation**](#objective-3--what-good-implementation-looks-like) | Readable, maintainable, traceable, correct, complete | Self-review your last assignment against this list |
| [**Coding standards & commenting**](#objective-4--coding-standards-and-comments-that-help-not-hurt) | Naming, spacing, comment types, avoiding “obvious” comments | Pick one standard and apply it consistently |
| [**Building robust code**](#objective-5--dont-just-code-the-happy-path) | Devil’s advocate thinking, validation, null checks, initialization | Add at least 3 “bad input” tests to a function |
| [**Reviews, testing, and TDD**](#objective-6--unit-testing-tdd-and-code-reviews) | Unit tests, TDD mindset, inspections/pair programming | Draft a small review checklist |
| [**Config management & version control habits**](#objective-7--configuration-management-versioning-and-working-on-a-team) | Version mgmt, integration/builds, defect tracking; pull often | Form a daily “pull/merge” habit |
| [**Defensive programming & contracts**](#objective-8--design-by-contract-and-defensive-programming) | Preconditions/postconditions/invariants vs defensive handling | Identify which methods assume vs enforce preconditions |
| [**Code reuse**](#objective-9--reuse-strategies-and-tradeoffs) | Abstraction/object/component/system-level reuse; costs/benefits | Decide when reuse beats rewriting |
| [**Host-target development**](#objective-10--host-target-development) | Developing on one platform, deploying on another | List what must match between host and target |
| [**Implementing for the cloud**](#objective-11--implementing-for-the-cloud) | IaaS / PaaS / FaaS + pros/cons + dev services | Categorize common tools you use (GitHub, S3, etc.) |
| [**In-class prompts / optional material**](#in-class-prompts--optional-material) | “When are you done?” + extra resource | Be ready to answer the “done” question |

---

## Main objectives
1) Understand implementation as the act of turning detailed design into a working program (and everything that comes with it) 
2) Compare how implementation starts in Agile vs non-Agile models 
3) Learn what “good implementation” means (readability, maintainability, performance, traceability, correctness, completeness) 
4) Adopt practical coding habits: standards, meaningful comments, avoid happy-path-only code, unit testing, reviews, version control discipline 
5) Understand broader implementation issues: design-by-contract, defensive programming, reuse, config management, host/target, and cloud implementation 

---

## Objective 1 — Implementation is more than just writing code
Implementation includes much more than typing code:
- Writing code
- Desk checking / standards compliance
- Debugging
- Testing
- Code reviews
- Configuration management + version control 

The deck also explicitly calls out “more than just coding” tasks such as:
- DB stored procedures, scripts, permissions, file structures
- Populating reference/resource files
- Documentation (user/installation guides)
- Setting up source control (if not already done)
- Ensuring the code is complete/correct 

**Added context:** In real projects, these “non-code” tasks are often what make software *deployable*, *maintainable*, and *supportable*.

---

## Objective 2 — Agile vs non-Agile: when implementation starts
### Agile implementation
- Begins **as soon as the developer understands the first user story**
- Implementation helps you understand the app; refactoring lets design + code evolve together 

### Non-Agile (traditional) implementation
- Waits until all requirements are gathered/specified/verified
- Waits until architecture/class/functional design exists
- Input is the low-level detailed design docs 

**Added context:** Iterative models can still discover design issues during coding—then you loop back and refine design (instead of pretending design was perfect).

---

## Objective 3 — What good implementation looks like
Characteristics the deck lists:
- **Readability**: others can understand it
- **Maintainability**: easy to modify
- **Performance**: as fast as possible when other goals are equal
- **Traceability**: code corresponds to design + requirements
- **Correctness**: does what it’s intended to do
- **Completeness**: all system requirements are met 

**Added context:** Traceability is a recurring theme across the course: requirements ↔ design ↔ code ↔ tests.

---

## Objective 4 — Coding standards and comments that help (not hurt)
### Language choice factors
- **Constrained**: company requirements, customer requirements, environment requirements
- **Unconstrained**: language features vs product needs, libraries, programmer expertise 

### Coding standards: why they matter
Benefits highlighted:
- discipline, readability, portability
- faster understanding of others’ code
- fewer merge conflicts
- better long-term maintenance 

Common standard elements:
- naming conventions, indentation/whitespace, method/file sizes, commenting conventions, error-handling style 

### Commenting guidance
- Write for the maintainer (future you or another developer)
- Don’t state the obvious
- If you must “explain the code,” consider rewriting for clarity
- Use TODO markers for incomplete items (source control tracks authorship anyway)
- Keep comments updated 

**Added context:** “Good naming is part of commenting/documentation.” (The deck directly frames naming as “self-documenting code.”) 

---

## Objective 5 — Don’t just code the happy path
### Happy path warning
A common entry-level mistake is coding only the “everything goes right” path. You need to:
- validate parameters
- check for null/ownership (where applicable)
- initialize variables at declaration 

### “Devil’s advocate”
Actively ask: “What could go wrong?”—for your code and when reviewing others’ code. 

**Added context:** This mindset is basically pre-baked risk analysis at the code level.

---

## Objective 6 — Unit testing, TDD, and code reviews
### Unit testing
- Test that a unit does what it should (happy path)
- More importantly: test the ways it can go wrong (devil’s advocate)
- Closed-box or open-box approaches 

### Test Driven Development (TDD)
- Write the unit test **before** writing the code
- Tests fail first, then pass as you implement 

### Code inspections / reviews and pair programming
- Reviews catch errors fast; should happen before committing/merging; reviewers do multiple passes (standards, design match, maintainability, OO practices)
- Pair programming = real-time code inspection; observer plays devil’s advocate; swap roles regularly 

---

## Objective 7 — Configuration management, versioning, and team habits
Configuration management = managing a changing software system, including:
- **Version management** (source + docs)
- **System integration** (builds; tracking component versions in a build)
- **Defect tracking** (issues tied to versions/builds) 

Team habit callout:
- Pull code down often to reduce “big bang” merge conflicts 

---

## Objective 8 — Design-by-contract and defensive programming
### Design-by-contract
- Assume preconditions are true; guarantee postconditions; maintain class invariants 

### Defensive programming
- Expect unpredictable errors; don’t assume preconditions are guaranteed
- Error handling options: wait for legal value, set defaults, reuse previous result, log, throw exception, abort 
- Exception-handling guidance: throw/catch specific exceptions; handle what you can; rethrow when needed; continue if possible 

“Enforce intentions” guidance:
- Use qualifiers (final/const/static/etc.)
- Localize constraints and scope
- Restrict access (private/protected + accessors)
- Encapsulate legal values in types when possible 

---

## Objective 9 — Reuse strategies and tradeoffs
Levels of reuse:
- **Abstraction-level** (reuse ideas/patterns)
- **Object-level** (reuse modules/objects from libraries)
- **Component-level** (reuse collections of objects; often requires adaptation)
- **System-level** (reuse whole applications; configure COTS) 

Benefits:
- faster development, reduced risk, more reliable code (already tested), sometimes lower cost 

Costs:
- research, purchase, adaptation, integration (“rarely plug-and-play”) 

---

## Objective 10 — Host-target development
- **Host**: where developers code
- **Target**: where software runs
- Platforms include development platform (OS + IDE/compiler/debugger) and execution platform (OS + supporting software, typically no IDE) 
- Host and target should match as much as possible 

---

## Objective 11 — Implementing for the cloud
Cloud implementation topics covered:
- **IaaS**: infrastructure you can spin up quickly; scaling (vertical/horizontal) 
- **PaaS**: platform to run apps (web server, DB, file hosting, email services) 
- **FaaS**: small functions that run on-demand and die after execution (e.g., AWS Lambda) 
- Cloud application services: storage (S3), SQL/NoSQL DBs, email, notifications 
- Cloud developer services: repos (GitHub), project tools (Trello/Jira), chat (Slack/Discord) 

Advantages:
- flexibility/scalability, less effort to manage services, fewer startup costs, possibly lower TCO 

Disadvantages:
- still must manage, less control, legal issues (data residency), higher costs if charged per-use 

---

## In-class prompts / optional material

### In-class discussion prompt
- **When are you done implementing?**
  - When you run out of time?
  - When you get it to work?
  - When all requirements are satisfied? 

**Added context (strong answer to bring):**
You’re done when the code meets requirements, passes tests (including edge cases), meets standards, and is integrated/versioned in a releasable state.

### Optional material
- Optional YouTube link is provided in the deck 
- Logging/monitoring resource is referenced (AWS prescriptive guidance link) 
