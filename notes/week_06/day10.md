# Software Engineering — Day 10
## Topic: Software Project Management 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**What project management is**](#objective-1--what-software-project-management-is-and-why-it-matters) | PM as planning/organizing/monitoring + why projects fail | Be able to explain “WHAT/HOW/WHO/TIME are uncertain” |
| [**What SPM addresses**](#objective-2--what-spm-addresses-organization-tools-risk-estimation-scheduling) | Org structure, tools, risk, estimation, scheduling, monitoring | Turn this into a checklist for your next project |
| [**Who’s in charge**](#objective-3--roles-project-manager-vs-team-leader-and-scrum-split) | PM vs team leader; how Scrum splits responsibilities | Identify who owns what in each model |
| [**Team organization models**](#objective-4--organizational-structures-project-functional-matrix-agile) | Project-oriented, functional, matrix, agile orgs | Name 1 pro + 1 con for each |
| [**Team size & communication**](#objective-5--team-size-communication-and-brooks-law) | Why “add people” can slow you down | Use Brooks’ Law to argue against late staffing |
| [**Distributed teams**](#objective-6--geographically-distributed-teams-pros-cons) | Pros/cons + hidden costs of distribution | List 2 mitigations for the cons |
| [**Process: TSP & PSP concepts**](#objective-7--team-software-process-tsp-and-personal-software-process-psp) | Self-directed teams, roles, artifacts, estimation discipline | Know what artifacts exist at launch |
| [**Estimation & definition of done**](#objective-8--estimation-mistakes-cone-of-uncertainty-and-definition-of-done) | Estimation pitfalls + “done” mismatch | Write a concrete Definition of Done for a task |
| [**Progress & change management**](#objective-9--progress-reporting-and-change-management) | How to report progress + manage changes without surprises | Practice “options-first” reporting |
| [**Risk management**](#objective-10--risk-management-identify-analyze-prioritize-mitigate) | Project/product/business risks + conquest/avoidance | Draft 3 risks + mitigations |
| [**Tools**](#objective-11--project-tools-and-techniques) | Typical tools (schedule, CM, requirements, design, build, test) | Map tools you already use into these buckets |
| [**In-class exercises / actions**](#in-class-exercises--calls-to-action) | Practical prompts you can do right away | Be ready with examples |

---

## Main objectives
1) Understand software project management as the process of **planning, organizing, and monitoring** a software project 
2) Learn what SPM must address: **organization, tools, risk, estimation, scheduling, documentation/monitoring** 
3) Compare organizational structures (project, functional, matrix, agile) and how they affect teams 
4) Understand why team size and communication can make projects fail (Brooks’ Law) 
5) Build a practical mindset for **risk + change management**, and define DONE in a consistent, measurable way 

---

## Objective 1 — What software project management is (and why it matters)
Software Project Management (SPM) is the process of **planning, organizing, and monitoring** development from inception to completion. It’s an essential part of software engineering—good SPM can’t guarantee success, but bad SPM usually leads to failure. 

The other deck frames PM as a way of organizing people/tools/resources to accomplish a goal, and emphasizes why projects fail:
- We don’t fully know **WHAT** requirements are (so we gather/analyze),
- We don’t fully know **HOW** it should be done (architects take a stab),
- We don’t fully know **WHO** should be involved (use who’s available),
- We don’t fully know **TIME** it will take (often fix time + scale scope). 

**Added context:** This is basically “software is uncertainty management.” PM exists to reduce uncertainty (or at least keep it visible and controlled).

---

## Objective 2 — What SPM addresses: organization, tools, risk, estimation, scheduling
SPM addresses:
- **Organization** (how the team is structured)
- **Project management tools** (what supports planning/monitoring)
- **Risk management** (what could derail schedule/quality and how to respond)
- **Estimation** (how long it will take)
- **Scheduling** (dependencies, duration, assignment)
- **Documentation & monitoring** (tracking on-time/on-budget) 

Common challenges called out:
- Customers aren’t sure what they want and change their minds,
- Estimation is hard (especially early),
- Coordinating requirements to design is hard,
- Technical difficulties happen,
- Team dynamics complicate everything. 

---

## Objective 3 — Roles: Project Manager vs Team Leader (and Scrum split)
- **Project Manager:** plans/controls/monitors the team, schedules activities, and coordinates many tasks. 
- **Scrum note:** in Scrum, “PM responsibilities” are split between Product Owner, Scrum Master, and Developers. 
- **Team Leader:** basically a PM for a smaller team/subgroup. 

**Added context:** The point isn’t the title—it’s that someone must own coordination, communication, and decision-making.

---

## Objective 4 — Organizational structures: project, functional, matrix, agile
### Project-oriented organization
People are organized around projects; project manager is the boss; team is assembled from different expertise areas. 
- Pros: loyalty to project, fewer distractions  
- Cons: professional isolation, reduced code reuse, reduced idea sharing 

### Function-oriented organization
Company organized by function; functional managers control projects within their function and usually control hiring/firing. 
- Pros: clear chain of command, expertise focus  
- Cons: managers juggle multiple projects, limited attention, resource shifting harms other projects 

### Matrix organization
Cross between project and functional: employees belong to a functional group but are loaned to projects. Functional supervisor evaluates performance; project supervisor assigns tasks. 
- Pros: PM focuses on project; functional manager focuses on expertise; can find similarities across projects  
- Cons: confusion (who’s my supervisor), double management cost 

### Agile organization
Self-organizing technical teams; non-technical functions (finance/marketing) still matter and must also adapt because agile isn’t plan-driven. 
- Pros: forces good estimates, increases customer interaction, less classic management  
- Cons: may need modification for large teams/large projects 

---

## Objective 5 — Team size, communication, and Brooks’ Law
The “obvious” move (add devs to meet a shorter deadline) is not always correct. 
Brooks’ Law: “Adding manpower to a late software project makes it later.” Reasons:
- onboarding time to become productive
- communication overhead increases with team size 

Communication failures are a common root cause of project failure, and communication has a real cost. 

**Added context:** More people increases coordination paths dramatically; if your design/spec isn’t clear, you get duplicated work and integration errors.

---

## Objective 6 — Geographically distributed teams (pros/cons)
Distributed teams:
- Pros: “follow-the-sun” work, access to good talent, potential cost savings  
- Cons: harder to understand requirements, less informal chatter, time zone friction, surprises in skill sets 

**Added context:** Requirement clarity and written communication become non-negotiable when the hallway conversation disappears.

---

## Objective 7 — Team Software Process (TSP) and Personal Software Process (PSP)
TSP is presented as a guideline for building self-directed teams (3–20 engineers) that set goals/process/plans and track their work, while helping managers coach and sustain performance. 

TSP roles include:
- Team Leader, Development Manager, Planning Manager, Quality/Process Manager, Support Manager 

Artifacts at launch include:
- team goals, roles, process plan, quality plan, support plan, schedule, detailed per-engineer plans, risk assessment, status report 

PSP is described as an individual-level process to improve estimation/planning, quality, and defect reduction by tracking predictions vs actuals. 

---

## Objective 8 — Estimation mistakes, cone of uncertainty, and “Definition of Done”
The intro PM deck highlights:
- task dependencies and the need to break big tasks into small ones (estimates are better for short/simple tasks) 
- common estimation mistakes:
  - not accounting for someone else doing the work
  - not documenting the “words behind the words”
  - the software “telephone game” (customer → PM → architect → lead…) 

Most common progress reporting mistake: no consistent, quantifiable definition of DONE—different roles interpret “done” differently. 
Suggested approach: avoid subjective % complete; assign % to verifiable steps (code complete, checked-in & tested, docs updated, tools updated). 

---

## Objective 9 — Progress reporting and change management
Progress reporting guidance includes:
- front-load schedule for ramp-up
- avoid time-based progress (“time passed is irrelevant”)
- avoid task-count progress (tasks aren’t equal)
- don’t avoid confrontation—report problems with options
- manage communication flow 

Change management:
- change will happen; agree on how to manage it
- document every change and its impacts (cost/schedule/features)
- change requires agreement before work begins
- avoid surprises: define, discuss, detail, decide, do
- be open to barter 

---

## Objective 10 — Risk management
Risk management activities:
- identify risks (worst-case thinking)
- analyze impact
- prioritize
- deal with risks via **conquest** (prevent it) or **avoidance** (change plans so it won’t happen)
- make a plan to retire each risk 

Risk types:
- **Project risks** (schedule/resources)
- **Product risks** (quality/performance)
- **Business risks** (organizational/procurement impacts) 

Key theme repeated: be proactive—define done, break tasks down early, prioritize, plan for change, track risks, report progress/problems. 

---

## Objective 11 — Project tools and techniques
The SPM deck lists tool categories you’d expect:
- Scheduling (e.g., MS Project)
- Configuration management (e.g., TFS / git)
- Requirements management (wiki)
- Design management (UML tools)
- Build management (git/build tooling)
- Test case management (JUnit/SpecFlow/etc.) 

**Added context:** The specific tool matters less than having a consistent workflow the team follows.

---

## In-class exercises — Calls to action

### In-class exercise: define DONE for a task
Pick a task and write a measurable Definition of Done using verifiable steps (not “90% done”). 

### In-class exercise: Brooks’ Law scenario
Write a short explanation (3–5 sentences) for why adding people late can make a project later, and what you’d do instead (reduce scope, clarify interfaces, improve communication). 

### In-class exercise: risk list + mitigation
List 3 risks (one project, one product, one business) and write:
- impact
- likelihood
- mitigation plan (conquest or avoidance) 

---

## Homework / optional actions
- **Optional:** Consider PMI student membership (the deck mentions a student membership program and pricing info). 
(No explicit graded homework items are stated in these slides.)
