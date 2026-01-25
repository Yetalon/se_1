# Software Engineering — Day 15
## Topics: Scrum (Framework) + Scrum Requirements (User Stories / Backlog) 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first |
| [**What Scrum is**](#objective-1--what-scrum-is) | Scrum as an agile framework based on empiricism | Explain transparency/inspection/adaptation |
| [**Why use Scrum (and when not to)**](#objective-2--why-use-scrum-and-when-not-to) | What problems Scrum addresses + Cynefin guidance | Decide which domain your project fits |
| [**Scrum roles**](#objective-3--scrum-roles-po-sm-dev-team) | Product Owner, Scrum Master, Dev Team responsibilities | Know who owns what (and what they don’t own) |
| [**Scrum artifacts**](#objective-4--scrum-artifacts) | Product backlog, sprint backlog, sprint board, increment | Identify artifacts in a real workflow |
| [**Scrum events**](#objective-5--scrum-events-sprint-and-ceremonies) | Sprint planning, daily scrum, review, retrospective | Be able to describe each event’s goal |
| [**Scrum requirements: the “just enough / just in time” mindset**](#objective-6--scrum-requirements-just-enough-just-in-time) | Requirements as adjustable; cut scope when time/money low | Summarize Scrum reqs vs sequential |
| [**User stories (Card / Conversation / Confirmation)**](#objective-7--user-stories-and-acceptance-criteria) | Story template + acceptance criteria / conditions of satisfaction | Write 3 stories with acceptance criteria |
| [**Story sizing and refinement**](#objective-8--progressive-refinement-epics-features-stories-tasks) | Epics → features → stories → tasks; themes | Classify examples correctly |
| [**Writing good stories (INVEST)**](#objective-9--writing-good-stories-invest) | Independent, Negotiable, Valuable, Estimable, Small, Testable | Evaluate a story against INVEST |
| [**Elicitation techniques**](#objective-10--gathering-stories-workshops-and-story-mapping) | Workshops, roles/personas, story mapping (Patton) | Draft a simple story map |
| [**Homework / readings**](#homework--readings) | Assigned + optional reading | Do the assigned decks reading |

---

## Main objectives
1) Understand Scrum as an agile approach/framework for delivering products in timeboxed sprints 
2) Know Scrum’s empirical foundations: transparency, inspection, adaptation 
3) Learn Scrum roles, artifacts, and events (and who owns what) 
4) Understand how requirements are treated differently in Scrum: negotiated continuously, just-in-time, just-enough 
5) Learn user stories, acceptance criteria (conditions of satisfaction), and progressive refinement (epic→feature→story→task) 

---

## Objective 1 — What Scrum is
- Scrum is “an agile approach for developing innovative products and services” and centers on:
  - A prioritized **product backlog**
  - Working on highest-priority items first
  - Short, timeboxed iterations called **sprints** (1 week to 1 month)
  - A self-organizing, cross-functional team doing design/code/build/test/deploy 
- Scrum is described as agile, lightweight, simple to understand, created in the early 1990s, and founded on empirical process control:
  - **Transparency**: process visible with common evaluation standard
  - **Inspection**: frequent review of artifacts/progress
  - **Adaptation**: adjust when product is at risk 

**Added context:** Scrum is a framework—teams still choose engineering practices (CI, TDD, code review) inside it.

---

## Objective 2 — Why use Scrum (and when not to)
### Why Scrum
Motivations listed include:
- Classic approaches aren’t working; projects are late; time-to-market issues
- Environment is dynamic; unknowns exist; adapting to change matters
- Big up-front architecture may be unnecessary
- Teams are not cross-functional → too many handoffs 

### When not to use Scrum (Cynefin guidance)
- **Complex**: explore/learn and adapt → Scrum fits well
- **Chaotic**: crisis response, can’t prioritize → Scrum doesn’t work well
- **Complicated**: expert diagnosis with quantitative approaches → Scrum may not be best
- **Simple**: best practices exist → plan-driven models may be best (Scrum okay but not necessary)
- **Disorder**: you don’t know which domain you’re in → first work to get out of disorder
- **Interrupt-driven work** (e.g., help desk): Scrum struggles; **Kanban** may fit better 

**Added context:** Scrum needs some predictability and prioritization. If the work is pure firefighting, flow-based systems win.

---

## Objective 3 — Scrum roles (PO, SM, Dev Team)
### Product Owner (PO)
- Responsible for maximizing product value and managing the **Product Backlog**
- Orders backlog items (priority), keeps it visible/transparent
- Ensures Dev Team understands backlog items
- Writes acceptance tests for user stories
- One person (not a committee); organization respects PO decisions; Dev Team follows PO priorities 
- PO **does NOT** manage sprint backlog, estimate effort, or decide sprint delivery contents 

### Development Team (Developers)
- Professionals who deliver a potentially releasable increment each sprint
- Self-organizing, cross-functional, no sub-teams, “Developer” title only
- Team size 3–9
- Own estimation and sprint backlog 

### Scrum Master (SM)
- Ensures Scrum is understood and used
- Coaches PO and Dev Team; facilitates Scrum events; removes impediments
- Does **NOT** act as project manager or tell the team how to do their work 

---

## Objective 4 — Scrum artifacts
Artifacts called out:
- **Product Backlog**: prioritized list of work; continuously evolving; PO owns content/order 
- **Sprint Backlog**: tasks for a single sprint; owned by Dev Team 
- **Sprint Board**: tracks progress on sprint tasks 
- **Potentially Shippable Product Increment**: what is produced each sprint 
- **Burn-down chart**: compares estimated time to actual time (tools: Azure DevOps, Jira, Trello) 

---

## Objective 5 — Scrum events (Sprint and ceremonies)
### Sprint (timeboxed iteration)
- Time limit: one month or less
- Goal: completed, usable increment
- Rules: no changes that endanger sprint goal; priorities remain constant; quality doesn’t drop; scope can be clarified/renegotiated with PO+Dev Team 

Sprint cancellation:
- Only PO can cancel; only if sprint goal becomes obsolete; uncommon; “do not cancel a sprint in this course.” 

### Sprint Planning
- Sets sprint goal
- Selects high-priority backlog items team can accomplish at sustainable pace
- May break down into tasks / refine stories 

### Daily Scrum (during sprint execution)
Each member answers:
- What did I accomplish since last daily scrum?
- What will I do before next?
- What obstacles/impediments block me? 

### Definition of “Done”
- End of sprint: potentially shippable increment
- “Done” includes designed, built, integrated, tested, documented (shippable ≠ deployed) 

### Sprint Review
- Inspect product, adapt understanding
- Stakeholders + scrum team; info flows both ways 

### Sprint Retrospective
- Inspect process; continuous improvement
- Commit to a practical number of improvement actions for next sprint 

---

## Objective 6 — Scrum requirements: just enough, just in time
Scrum vs sequential requirements:
- Scrum negotiates details continuously
- Through conversations
- Just in time / just enough
- Requirements are an adjustable degree of freedom: if time/money low, cut low-value requirements 

Historical context point:
- Working longer/harder up front won’t produce complete requirements/designs
- Instead: do just enough to start, refine as you go
- For uncertain items: create a Product Backlog Item representing desired business value 

**Added context:** Scrum treats scope as flexible so time/cost can stay controlled; this is the opposite of “fixed scope, fixed date” thinking.

---

## Objective 7 — User stories and acceptance criteria
User stories:
- Express desired business value for features/backlog items
- Plain English, easy to refine, placeholder for conversations 

Template:
- “As a <user role>, I want <goal>, so that <benefit>.” 

Card/Conversation/Confirmation idea:
- A story is not the full spec; it prompts conversations and confirmation criteria 

Conditions of Satisfaction / Acceptance Criteria:
- Clarify desired behavior and guide acceptance-test-driven development 

**Added context:** Acceptance criteria are your “validation” hook: they explain what makes the PO say “yes, it’s done.”

---

## Objective 8 — Progressive refinement: epics, features, stories, tasks
Key ideas:
- Don’t force the same detail on all requirements; it wastes time and kills conversation 
Sizes:
- **Epic**: spans entire release or multiple releases (big picture)
- **Feature**: weeks to complete (not sprint-able)
- **Story**: sprint-able (days)
- **Task**: how to build the item (hours); tasks are not stories 

Grouping:
- **Theme**: collection of related stories; helps organization 

---

## Objective 9 — Writing good stories (INVEST)
Bill Wake’s criteria:
- **Independent** (minimize dependencies)
- **Negotiable** (details via conversation; avoids fights)
- **Valuable** (to user/customer; tech stories require business justification)
- **Estimable** (team can size it; otherwise refine/decompose)
- **Small** (fits within sprint; no 2-week stories in a 2-week sprint)
- **Testable** (clear pass/fail criteria; acceptance criteria) 

**Added context:** INVEST is a fast “quality check” for backlog health.

---

## Objective 10 — Gathering stories: workshops and story mapping
The deck emphasizes users often change their minds; therefore:
- include users in writing stories
- run story-writing workshops (hours to days; not aiming for “complete set”)
- use roles/personas to sharpen “As a …” (e.g., persona example “Cletus…”) 

Story mapping (Patton):
- decompose user activity into workflow → tasks → subtasks
- map: Activity (epic) → Task (theme) → Subtask (sprint-able story) 

---

## In-class exercises — Calls to action
### In-class exercise: Scrum practice for the semester
The class plan calls out:
- You’ll do in-class exercises until comfortable
- Then organize teams
- Then run week-long sprints
- Daily standups in class
- Expected work outside class: at least 2 hours/week; more = exceeding expectations 

### In-class exercise: “Where’s Waldo?”
A reference sheet is provided; you’re asked to find what major element of Scrum is missing. 

---

## Homework / readings
### Homework (assigned reading)
- Read Dr. Bennett’s two slide decks:
  - 04_Scrum.pptx
  - 05_Scrum_Requirements.pptx 

### Optional reading
- Tutorialspoint Scrum quick guide (optional)
- KnowledgeHut Scrum dev team tutorial (optional) 
