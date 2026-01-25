# Software Engineering — Day 8
## Topic: Testing Introduction + Testing Phase (Verification & Validation) 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**Why we test & what “quality” means**](#objective-1--why-we-test-and-what-quality-means) | Testing as evidence; quality = meets specs + fit for use | Write 2 reasons testing matters beyond “find bugs” |
| [**QA vs QC + static vs dynamic**](#objective-2--qa-vs-qc-and-static-vs-dynamic) | QA activities vs QC defect detection; docs vs code behavior | Classify examples as QA or QC |
| [**Key terms: error/defect/failure + risk**](#objective-3--core-terms-risk-error-defect-failure) | Shared vocabulary for talking about bugs | Make flashcards for definitions |
| [**Verification vs validation**](#objective-4--verification-vs-validation) | “Build it right” vs “build the right thing” | Tag activities as V or V&V |
| [**Testing levels: unit → system**](#objective-5--what-is-tested-levels-of-testing) | Unit/functional/integration/system | Identify what level a test belongs to |
| [**Testing purposes (acceptance, performance, regression, etc.)**](#objective-6--why-are-we-testing-types-of-testing-by-purpose) | Different testing goals beyond correctness | Pick which tests apply to an app scenario |
| [**Black-box vs white-box**](#objective-7--black-box-vs-white-box) | “No internals” vs “with internals” | Label example tests as black/white |
| [**Debugging vs testing**](#objective-8--testing-vs-debugging) | Showing behavior vs removing the error | Explain the difference in one sentence |
| [**Defect tracking & priorities**](#objective-9--defect-tracking-priorities-and-quality-metrics) | Why tracking matters; priority one; defect density | Describe what makes a defect “Priority One” |
| [**Test documentation & test suites**](#objective-10--test-plans-test-suites-and-validating-tests) | Test plan components; mutation/fault injection | List what belongs in a test plan |
| [**Lifecycle model impact**](#objective-11--how-testing-changes-in-waterfall-iterative-and-scrum) | Waterfall vs iterative vs Scrum testing cadence | Compare “big bang” vs “lesser bang” |
| [**In-class exercises**](#in-class-exercises--calls-to-action) | Practical prompts to apply concepts | Do the classification prompts |

---

## Main objectives
1) Understand why testing exists and how it relates to software quality 
2) Learn the difference between QA vs QC, and static vs dynamic quality techniques 
3) Use correct vocabulary: risk, error, defect/fault/bug, failure 
4) Distinguish verification vs validation and how they appear across the lifecycle 
5) Understand testing levels, testing purposes, black-box vs white-box, and the value of defect tracking/metrics 

---

## Objective 1 — Why we test and what “quality” means
- Goal of development: **high-quality software**—meets specifications and is **fit to use** 
- Testing is used to:
  - prove high quality
  - show the software meets requirements
  - find incorrect/undesirable behavior 
- Dijkstra quote: testing shows presence of errors, not absence 

**Added context:** Testing is evidence, not a guarantee. “Bug-free” is usually a claim you can’t honestly prove for non-trivial systems.

---

## Objective 2 — QA vs QC and static vs dynamic
### Quality Assurance (QA) vs Quality Control (QC)
- **QA:** activities designed to measure and improve quality; includes process, training, prep 
- **QC:** verification activities that detect defects and ensure they’re fixed before release 

### Static structure vs dynamic behavior
- Docs (requirements/design) are mostly **static structure**
- Running software exhibits **dynamic behavior** 

### QA techniques listed
- Testing (execute code, compare outputs) 
- Reviews/inspections (team-based critical look; labor intensive but effective) 
- Formal methods (math proof; rare in commercial business software) 
- Static analysis (automated structural checks for error-prone conditions) 

---

## Objective 3 — Core terms: risk, error, defect, failure
### Risk
- In software: probability the software has unexpected behavior 
- In general: anything that could affect successful system outcome 

### Error → Defect/Fault → Failure (chain)
- **Error:** human action that causes a failure (a mistake) 
- **Fault/Defect (bug):** condition that may cause failure; caused by an error 
- **Failure:** system can’t perform according to specs; result of a fault/defect 

**Added context:** This distinction matters for defect reports: failures are what you observe; defects are what you fix.

---

## Objective 4 — Verification vs validation
### Verification
- Activities showing a work product conforms to specs  
- “Are we building the product right?” 
- Can begin as early as requirements analysis (checking completeness/correctness of requirements) and continues through design review + traceability + code reviews/unit testing 

In the formal test phase, verification typically:
- starts with functional / low-level integration testing
- continues with subsystem/integration testing
- finishes with system testing 

### Validation
- Activities showing the product serves its purpose (customer requirements)
- “Are we building the right product?” 
- Often focused on customer-defined requirements and happy paths; customer signs off 

Example validation test case structure:
- **Precondition → Action → Postcondition** 

**Added context:** Verification can succeed even if the spec was wrong. Validation catches “meets spec but doesn’t solve the real problem.” 

---

## Objective 5 — What is tested: levels of testing
Defined levels:
- **Unit testing:** individual methods/classes 
- **Functional testing:** slightly higher; units working together 
- **Integration testing:** integrated functionality in context of system 
- **System testing:** all features work together; system as a whole 

Who tests:
- Programmers (often unit tests)
- Testers (often system tests)
- Users (acceptance testing) 

---

## Objective 6 — Why are we testing: types of testing by purpose
The decks list many testing goals:
- Acceptance testing (customer before accepting/paying; criteria set with requirements) 
- Conformance testing (standards/policies) 
- Configuration testing (different underlying configurations) 
- Performance testing (TPS, concurrent users) 
- Stress / load testing (degrades gracefully) 
- Usability testing (UI interaction) 
- Regression testing (still works after changes) 
- Installation testing (installs correctly) 
- Robustness testing (handles wide range of inputs, correct and incorrect) 

---

## Objective 7 — Black-box vs white-box
- **Black-box:** test without internal details; functional testing; can occur at multiple stages 
- **White-box:** test with knowledge of design/implementation details; normally unit testing; tests the code 

How to create test cases:
- Intuition, specification, code review (white-box), existing tests, missed faults (add tests based on what escaped) 

---

## Objective 8 — Testing vs debugging
- **Testing:** showing code behaves correctly; general granularity 
- **Debugging:** finding/removing an error; specific granularity 
- Testing is not a “cure”—there are common lies like “fully tested and bug-free” 

---

## Objective 9 — Defect tracking, priorities, and quality metrics
### Defect tracking (what counts as a defect)
Defects include:
- missing required functionality
- incorrect logic violating design/requirements
- boundary logic errors (happy path works but unhappy paths break) 

All defects should be tracked, even easy fixes, and prioritized in a customer-informed way (not dev preference). 

### Priority One defects
Reserved for defects that MUST be resolved before production:
- directly tied to a requirement
- prevent the happy path from running (example: network misconfiguration) 

### Measuring quality (examples)
- Defect density (where defects cluster)
- LOC written vs estimated
- number of defects fixed (careful interpreting)
- number of Priority One defects found (may imply lower quality if many) 

**Added context:** Metrics can be gamed. Use them to guide attention (where to invest QA effort), not to punish.

---

## Objective 10 — Test plans, test suites, and validating tests
### Test plan contents
Includes:
- define “units”
- types/extent of testing
- documentation of results
- input sources
- who tests
- resource estimates
- metrics to collect/analyze
- test results 

### Test suites must be valid
The deck notes: test suites can miss defects, so validate the suite by injecting faults:
- mutation testing (validates test suite, not code)
- fault injection (deliberately insert faults) 

---

## Objective 11 — How testing changes in Waterfall, Iterative, and Scrum
### Waterfall
- Test phase is formal schedule phase
- verification occurs across phases
- validation is “big bang” at end 

### Iterative
- verification happens in each iteration
- validation is a “lesser bang” at end of each iteration
- prior V&V repeated in later iterations 

### Scrum
- test phase integrated into each sprint
- verification/validation throughout sprint
- regression runs previous tests each sprint
- customer actively involved; automation repeated each sprint 

---

## In-class exercises — Calls to action

### In-class exercise: classify activities
For each activity, label **QA vs QC** and **Verification vs Validation**:
- requirements review 
- design review + traceability 
- unit tests + code review 
- system test run 
- customer acceptance test 

### In-class exercise: write a validation test case
Use **Precondition → Action → Postcondition** format for a simple feature (login example). 

### In-class exercise: list 5 “unhappy path” tests
Pick a function you’ve written recently and list 5 boundary/unhappy cases (nulls, invalid inputs, timeouts, permissions, etc.). 
