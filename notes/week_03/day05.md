# Software Engineering — Day 5
## Topic: Requirements (Processing, Elicitation, Specification, Analysis) 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**What a requirement is**](#objective-1--define-a-requirement-the-what-not-the-how) | “What” vs “How”, single-idea statements, mandatory vs optional | Rewrite 2 “bad” requirements into “good” ones |
| [**Functional vs non-functional**](#objective-2--separate-functional-and-non-functional-requirements) | Services vs constraints/qualities (“ilities”), examples | Tag sample requirements as FR vs NFR |
| [**Requirements engineering activities**](#objective-3--know-the-requirements-engineering-activities-and-artifacts) | Elicitation → documentation → analysis → validation → acceptance; artifacts list | Identify which artifact you’d produce next |
| [**Elicitation levels & problems**](#objective-4--elicitation-high-level-vs-detailed-and-why-it-goes-wrong) | High-level vs low-level; common failure modes | Use the “potential problems” list as a checklist |
| [**Elicitation techniques**](#objective-5--use-elicitation-techniques-interviews-observation-jad-prototypes) | Interviews, questionnaires, observation, document analysis, prototyping, JAD | Pick best technique for a scenario |
| [**Specification: TLR vs SRS**](#objective-6--write-the-right-kind-of-spec-tlr-vs-srs-and-what-makes-a-good-spec) | Organizing specs; IEEE 29148 SRS structure; “shall” statements | Draft 3 “shall” statements |
| [**Analysis & clustering**](#objective-7--analyze-cluster-and-prioritize-requirements) | Business flow clustering, VORD, prioritization | Practice grouping requirements (BF-1, IF-1.x, etc.) |
| [**Use cases & UML**](#objective-8--use-cases-scenarios-and-use-case-diagrams) | Use case parts, mistakes, include/extend/generalization | Sketch a use case + identify actors |
| [**Traceability (RTM)**](#objective-9--traceability-matrix-and-how-you-know-youre-done) | RTM as “done-ness” proof; testable/traceable/complete | Make a mini-RTM for 3 requirements |
| [**Exercises / homework**](#in-class-exercises--calls-to-action) | What to bring / what to do | Don’t miss the “games requirements” task |

---

## Main objectives
1) Define what a requirement is and keep it focused on the **WHAT**, not the **HOW** 
2) Distinguish **Functional** vs **Non-functional** requirements (and why NFRs are hard to specify precisely) 
3) Understand requirements engineering activities + common artifacts (TLR, SRS, use cases, user stories, etc.) 
4) Learn elicitation levels, pitfalls, and techniques (interviews, observation, questionnaires, prototyping, JAD) 
5) Learn requirements specification best practices + the idea of choosing the “right spec” (TLR vs SRS) 
6) Practice analysis: clustering, prioritization, use cases, UML use case diagrams, and traceability 

---

## Objective 1 — Define a requirement (the WHAT, not the HOW)
### Core definition
A requirement is a **single-sentence statement describing WHAT the solution will do**. 
Requirements describe the “what” — **NOT** the “how.” 

### SMART goals connection (why this appears here)
This deck links “requirements” to goal-setting ideas: goals should be **SMART** and positive (specific, measurable, achievable, relevant, timely). 
**Added context:** SMART is basically a “quality bar” so requirements become testable and less ambiguous.

### Common mistakes (and fixes)
- **Implementation detail disguised as a requirement**:  
  Bad: “The tool MUST bubble sort the results.”  
  Good: “The tool MUST sort the results in ascending order.”  
  (Unless bubble sort is a mandatory constraint.) 
- **Two requirements mashed into one** (conjunctions):  
  Bad: “The editor MUST support Undo and Repeat.”  
  Good: split into two requirements. 

---

## Objective 2 — Separate functional and non-functional requirements
### Functional requirements (FR)
Functional requirements specify **services the software must provide**, often stated as:  
> “The application shall …” 
Example: “The application shall allow a user to login with a username and password.” 

### Non-functional requirements (NFR)
Non-functional requirements specify constraints/qualities about services, not the service itself. 
Example: “The user’s account information shall display in less than 3 seconds.” 

The deck categories for NFRs include:
- **Qualities (“ilities”)**: reliability, availability, performance, security, portability 
- **Constraints**: accuracy, toolset, language 
- **Interfaces**: external interfaces, UI 
- **Error-handling**: ignore/warn/retry/log/default/shut down 

**Added context (the big pain):**  
The deck explicitly points out NFRs are hard because people say vague things like “user friendly” or “secure” without measurable criteria. 

---

## Objective 3 — Know the requirements engineering activities and artifacts
### Requirements engineering activities
- Elicitation
- Documentation and definition
- Specification
- Prototyping
- Analysis
- Review and validation
- Agreement and acceptance 

### Requirements artifacts (what you produce)
- Requirements reports
- Interview transcripts
- Questionnaire results
- Workflow models
- Top-Level Requirements (TLR) document
- Software Requirements Specification (SRS)
- Use cases
- User stories
- Other analysis models 

**Added context:** Artifacts exist so knowledge survives beyond one person’s memory and so teams can verify they built the right thing.

---

## Objective 4 — Elicitation: high-level vs detailed (and why it goes wrong)
### Requirements analysts need domain knowledge + communication
Users often **can’t state needs clearly**, so the analyst must listen and interpret. 

### Levels and modes
- High-level requirements: business rationale / justification 
- Low-level requirements: detailed user needs/desires 
Modes: verbal, written, online forms 

### High-level elicitation checklist
Opportunity/Need, Justifications, Major Constraints, Scope, Major Functionality, Success Factors, User Characteristics 

### Detailed requirements: “six dimensions”
- Individual functionality
- Business flow
- Data formats & information needs
- Interfaces with other systems
- User interfaces
- Other constraints (performance, reliability, security) 

### Potential problems (real-world reasons requirements fail)
- Devs don’t understand domain; users don’t know what they want
- Users can’t convey or won’t say needs
- Users can’t see big picture
- Devs don’t listen / “gold plating” (devs add requirements)
- Domain knowledge vs development knowledge are different 

---

## Objective 5 — Use elicitation techniques (interviews, observation, JAD, prototypes)
### Techniques list
Structured interviews, task-based interviews, open interviews, collaborative gathering, questionnaires, observation, document analysis, rapid prototyping, market analysis, JAD 

### Highlights (what matters)
- **Structured interviews**: pre-planned questions; avoid leading questions; don’t use jargon; expect contradictions 
- **Task-based interviews**: give a task and model their thought process 
- **Collaborative gathering**: group discussion, facilitator, avoid groupthink 
- **Questionnaires**: reach many users but less flexible; need tabulation; anonymous or not decision 
- **Observation & document analysis**: “walking around” + reviewing existing documents; good when replacing systems/paper processes 
- **Rapid prototyping**: early version (often throw-away) to validate feasibility/usefulness, especially UI; reveals inconsistencies 
- **JAD**: stakeholder sessions with facilitator and decision authority; produce minutes/action items/open issues 

---

## Objective 6 — Write the right kind of spec (TLR vs SRS) and what makes a good spec
### Two-sided understanding problem
Customer must understand what they asked for; developer must understand domain terminology. 

### What a good software specification must be
- Verifiable
- Clear (no ambiguity)
- Logical (no contradiction)
- Complete
- Free of implementation/design details
- In a standard format (e.g., “When <input>, the software shall <do X> and <output Y>.”) 

### “Right spec” depends on lifecycle model
Specs must be organized so customers see big picture and can search details; type depends on lifecycle. 

### TLR (Top-Level Requirements)
An overview for managers; includes exec summary, profiles, scope, system definition, diagram, FR/NFR, UI and data storage requirements. 

### SRS (Software Requirements Specification)
Based on IEEE 29148-2011 with sections: Intro, References, Specific Requirements, Verification, Appendices. 

**Added context:** The deck also notes SRS pros/cons: standardized and accepted, but rigid and hard to keep updated when requirements change. 

---

## Objective 7 — Analyze, cluster, and prioritize requirements
### Analysis is critical before design
The deck calls analysis “ABSOLUTELY critical” and notes one company even separated it as a contract to protect against impossible-to-build specs. 

Analysis ensures requirements are:
- Testable
- Traceable
- Complete
- Consistent
- Labeled mandatory vs optional 

### Clustering approaches
- By business flow (often start here) 
- Viewpoint-oriented requirements (VORD) 
- By use case 
- Prioritization (beware loudest voice; Delphi technique exists) 

### Business flow numbering scheme (example)
Pick BF-1, then associate related requirements:
- IF-1.x (individual functionality)
- DF-1.x (data formats)
- plus UI, IS (interfaces with systems), FC (constraints) labeled similarly 

---

## Objective 8 — Use cases, scenarios, and use case diagrams
### Use case definition + parts
Use case = a contract between stakeholder and system describing part of what the system must do. 
Parts: actors, pre/post-conditions, trigger, main success scenario, extensions. 

### Common mistakes
- Too low-level or too high-level
- Missing system responses
- Too much UI detail (remember: you’re getting requirements)
- Too many steps (means you need sub-use cases) 

### UML use case diagram basics
Actors (stick figure), use cases (oval), relationships; diagram does not show details. 

Relationships:
- `<<include>>` = A always invokes B
- `<<extend>>` = A sometimes invokes B
- `<<generalization>>` = inheritance relationship 

---

## Objective 9 — Traceability matrix and “how do you know you’re done?”
### RTM (Requirements Traceability Matrix)
RTM is a “to do list” across SDLC phases: verify every requirement is addressed in design, implemented, and proven complete. 

### Questions to ask during analysis (practical checklist)
- What problem/opportunity does this address?
- Who are the targeted users?
- Is there an existing comparable solution?
- What requirements connect closely? dependencies?
- Will it work if not in first release? (scope/priority)
- How does it add value to business/user?
- How will you know it’s met? (testable)
- Handle “ilities” precisely; avoid vague usability statements 

The deck ends with: “How do you know when you are done with the requirements phase?” 

**Added context:** The practical answer is “when stakeholders agree and every requirement is testable, traceable, consistent, and complete enough to start design with acceptable risk.”

---

## In-class exercises — Calls to action

### Homework (explicit call to action)
Bring requirements to class for a team exercise:
- Pick **3 games** your team chose earlier
- Write **at least 10 requirements for each game**
- Follow the guidelines to create SMART requirements
- Bring them to class as a starting point 

### In-class exercise (likely)
Use the requirements you brought to:
- cluster/group them (business flow or use case),
- label mandatory vs optional,
- and start a traceability approach (RTM). 
