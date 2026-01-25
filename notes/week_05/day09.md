# Software Engineering — Day 9
## Topics: Software Maintenance + Release Management 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**Why maintenance dominates cost**](#objective-1--why-worry-about-maintenance) | Maintenance as the largest % of lifecycle cost; why fixes are expensive later | Be able to explain the “2x–3x development cost” point |
| [**Types of maintenance**](#objective-2--types-of-software-maintenance) | Corrective, adaptive, perfective, preventative + how they affect complexity | Classify 6 examples into types |
| [**Maintenance challenges**](#objective-3--maintenance-challenges-management-process-technical) | Why maintenance is hard (people + process + tech) | Write 3 risks you’d expect in a maintenance project |
| [**Maintenance process & artifacts**](#objective-4--maintenance-process-trouble-tickets-change-requests-and-the-ccb) | Trouble tickets vs change requests; CCB role; impact analysis | Trace a request through the process |
| [**Patch releases**](#objective-5--patch-releases-and-workarounds) | Temporary fixes vs permanent replacements | Explain when a patch workaround is justified |
| [**Software evolution & legacy systems**](#objective-6--software-evolution-legacy-systems-and-reverse-engineering) | Why legacy systems get messy; reverse engineering; reengineering | Compare redocumentation vs design recovery |
| [**Release management basics**](#objective-7--release-management-and-production-realities) | Production/staging, user impact, dark releases, distributed prod | Describe why staging is “as close as possible” to prod |
| [**Who’s involved in releases**](#objective-8--who-is-involved-in-a-release) | Dev/IT/QA/Sec/Support and why | List 4 roles and what they do during release |
| [**Practice + agile connection**](#objective-9--practice-makes-perfect-and-why-agile-caresh) | Release plans, rehearsal, small deltas, automation | Identify why “small deltas” reduce risk |
| [**In-class exercises**](#in-class-exercises--calls-to-action) | 3–5 minute speech activity | Prepare a short talk outline |

---

## Main objectives
1) Define maintenance and understand why it’s the biggest long-term cost 
2) Identify and differentiate the four maintenance types and their impacts 
3) Understand the maintenance workflow (tickets/CCB/impact analysis/patches) 
4) Understand release management realities: production vs staging, minimizing user impact, planning and rehearsal 
5) Recognize that real releases involve many teams and benefit from automation and frequent small releases 

---

## Objective 1 — Why worry about maintenance?
### What is maintenance?
Maintenance = any activity performed on a product **after it has passed acceptance testing / been released**. 
IEEE definition: modifying software after delivery to:
- correct faults
- improve performance/attributes
- adapt to a changed environment 

### Why it matters (the cost reality)
- Maintenance is the largest percentage of total system cost — **2x to 3x development cost**. 
- The cost to find/fix faults during maintenance is the greatest compared to earlier phases. 

**Added context:** Once software is in production, you’re paying for:
- investigations across real data + real users,
- coordination/approvals,
- regression risk,
- and time-sensitive expectations.

---

## Objective 2 — Types of software maintenance
### Repair-based maintenance
- **Corrective:** identify/remove defects (usually discovered by customers); repair relative to existing requirements 
- **Adaptive:** adapt software to changes in environment (new OS version, new hardware) 

### Enhancement-based maintenance
- **Perfective:** implement user requests/new features; “Lehman’s first law” (systems must adapt or become less useful) 
- **Preventative:** improve maintainability (refactoring, updating internal/external docs) 

### Complexity note
- Corrective/adaptive/perfective tend to **increase complexity**
- Preventative attempts to **decrease complexity** 

**Added context:** This is why preventative work (refactoring, docs) is often “invisible” but critical—without it, every future change costs more.

---

## Objective 3 — Maintenance challenges: management, process, technical
### Management challenges (who/what/why)
- Management likes delivering new products and ROI; maintenance is expensive so they prefer charging for it 
- Ethical question raised: which maintenance types can you charge for? 
- Maintenance resources may be allocated to newbies/less-competent devs, which can be risky 
- Involves cost-benefit analysis, personnel, resource allocation 

### Process challenges
- Requires coordination
- Documentation must be updated (otherwise “you have a mess”)
- Source changes can ripple to design, requirements, and test plan 

### Technical challenges
- Maintenance repeats dev process **but must preserve existing required functionality**
- Either you add onto an existing design (risk: unacceptable design) or redesign (risk: disturb working stuff) 

---

## Objective 4 — Maintenance process: trouble tickets, change requests, and the CCB
### Basic workflow
- Customer reports → help desk creates trouble ticket / maintenance report (stored in DB)
- **Change Control Board (CCB)** reviews maintenance requests (approve/reject)
- Maintenance programmer receives request + documentation
- Fix is implemented and maintenance completed 

### Key artifacts
- **Maintenance report / trouble ticket**: typically defects
- **Change orders / change requests**: adaptive or perfective changes 

### Change Control Board (CCB)
- Includes stakeholders from multiple groups (development, users, documentation, marketing, QA, customer support)
- Each group contributes to impact analysis (docs team identifies manuals needing updates, etc.) 

### Impact analysis
- **Maximal impact:** affects all SDLC phases (requirements → architecture → detailed design → code)
- **Minimal impact:** affects only source code 

CCB decisions:
- Max impact: deny / defer / do
- Min impact: defer / do 

Other considerations listed:
- release cycle timing, testing ability, request criticality, legacy systems 

---

## Objective 5 — Patch releases and workarounds
Two methods for getting fixes to users:
- Permanent replacements
- Electronic patches applied in customer environment 

Why patches happen:
- defect takes long to fix and customers can’t use system properly
- workaround patch can reduce impact until permanent solution is ready 

---

## Objective 6 — Software evolution, legacy systems, and reverse engineering
### Legacy systems
Systems maintained for a long time often show:
- high complexity (continuous maintenance)
- inefficiencies due to old tech
- lack of accurate documentation
- original developers not available 

### Reverse engineering
When docs are out of date or missing:
- start with source code
- recreate the design (time-consuming but doable)
- recreate specs (extremely difficult)
- if only executable exists, it’s even harder 

Reverse engineering components:
- **Redocumentation:** generate docs from source code
- **Design recovery:** understand/rebuild design (tools can convert source to UML) 

### Reengineering
Periodically revisit architecture/design top-down to reduce complexity and cost; may mirror old system but incorporate new requirements 

---

## Objective 7 — Release management and production realities
### Production environment
Goal is “go live,” but production is complicated:
- failover, scaling, resource management
- many apps running together
- upgrades are harder when customers are actively using the system
- existing data may require conversion; tables modified; new connections made 

### Staging environment
- Should exist if possible
- Should be as close a replica of production as you can get
- Used to practice deployments and reduce risk
- Used for testing (load/stress, smoke testing) 

### Distributed vs single production
- Distributed production: multiple environments (load balancing) + failover strategy can make upgrades smoother if planned 
- Single production: likely do a **dark release**, or schedule downtime window and notify users; reminders increase as window approaches; possible redirection/broker 

### Minimize user impact
User impact is a major release risk; sometimes there are explicit cutover requirements; otherwise designers should still think about cutover 

---

## Objective 8 — Who is involved in a release?
Real releases involve many roles:
- Development (devs/PM often present or on call)
- IT/Operations (owns environment)
- QA (verify right thing deployed and working)
- Security (prevent unauthorized production impact)
- Support (handle customer impacts)
- Release managers may be a permanent role (often under IT) 

---

## Objective 9 — Practice makes perfect (and why Agile cares)
- Have a release plan
- Practice in staging until releases are smooth and quick
- Bigger delta (bigger changes) = harder release
- Complexity of release management helped drive Agile: frequent releases with small deltas
- Automation via scripts pays dividends with Agile; even infrequent releases benefit from scripts to reduce mistakes 

---

## In-class exercises — Calls to action

### In-class exercise: 3–5 minute speech (no slides)
Instructor will pick someone randomly to give a short talk on one topic:
- Requirements
- Design
- Implementation 

How to volunteer:
- in-person: hand a notecard with your name + topic at start of class
- online: put your name + topic in chat at start 

Reminder: a course learning outcome includes writing and orally communicating about SE. 

**Suggested prep (quick outline you can memorize):**
- 1 sentence definition (what it is)
- 2–3 key activities
- 1 real example
- 1 “how do you know you’re done?” criterion
