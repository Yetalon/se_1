# Software Engineering — Day 13
## Topic: Iterative (and Overlapping Iterative) — “Rapid Waterfall” 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**What Iterative is**](#objective-1--what-iterative-is-rapid-waterfall) | Iterative as “rapid waterfall,” possibly a bridge toward Agile | Explain iterative in 2–3 sentences |
| [**How Iterative works (cycles)**](#objective-2--how-iterative-works-sequential-waterfalls) | SDLC repeated per release; feedback loops | Draw 2 cycles and label the phases |
| [**Why Iterative helps**](#objective-3--why-iterative-helps-feedback-scope-and-rhythm) | Feedback, scoping, release rhythm, earlier value delivery | List 3 reasons it’s better than pure waterfall (in some cases) |
| [**Overlapping Iterative**](#objective-4--overlapping-iterative-concurrent-mini-big-bangs) | Shorter time between releases but more complexity | Identify when overlapping is risky |
| [**Up-front analysis & architecture**](#objective-5--what-iterative-still-needs-up-front) | Why upfront requirements + architecture matter even in iterative | Describe “scaffolding” in your own words |
| [**Iterative for risk reduction**](#objective-6--iterative-as-risk-reduction-and-prototyping) | Early releases as prototypes; learn unknowns safely | Explain how iterative can “feel like agile” |
| [**In-class exercises**](#in-class-exercises--calls-to-action) | Apply the model to a scenario | Choose a product and justify iterative vs waterfall |

---

## Main objectives
1) Understand Iterative as **“Rapid Waterfall”** that divides requirements into planned releases 
2) Understand that each release follows the SDLC (requirements → design → implementation → testing → release → maintenance) 
3) Learn how feedback from one release feeds into the next, and how scope/rhythm work 
4) Compare standard Iterative vs **Overlapping Iterative** (benefits and tradeoffs) 
5) Understand why up-front requirements analysis + architecture design still matter in iterative approaches 
6) Recognize Iterative as a **risk reduction** tool that can also serve as prototyping 

---

## Objective 1 — What Iterative is (“Rapid Waterfall”)
- Iterative is described as **“Rapid Waterfall”** and possibly a birthplace/bridge toward Agile thinking. 
- It follows the Waterfall method, **but divides the requirements into releases at the outset**. 
- Each release is a **functioning version** of the solution and enables customer/user feedback. 
- Highest priority items are done early. 
- Each release averages **6–9 months**, versus Waterfall projects that can take years. 

**Added context:** Iterative still “plans forward,” but it ships value sooner and learns from each release rather than betting everything on a single end release.

---

## Objective 2 — How Iterative works (sequential waterfalls)
- You can think of it as **sequential waterfalls**: each release repeats the SDLC phases. 
- The phases listed per release are:
  - Requirements
  - Design
  - Implementation
  - Testing
  - Release
  - Maintenance 

**Added context:** This means each release is a “mini project.” You still do requirements and design—just in smaller chunks.

---

## Objective 3 — Why Iterative helps (feedback, scope, rhythm)
Key benefits described:
- Feedback from release 1 is fed into the requirements/design of the next release. 
- Non–Priority One defects can be incorporated into the next release more easily. 
- Provides a **rhythm** to releases; contents are scoped to the selected time frame. 
- Releases are still “mini big bangs” and take months—just less extreme than a single multi-year waterfall. 
- Second cycle can start before the first ends → more even staff loading and less time between releases. 

**Added context:** Iterative is a compromise: still structured like waterfall (phases), but uses release cadence to reduce risk and deliver earlier.

---

## Objective 4 — Overlapping Iterative (concurrent mini-big-bangs)
Overlapping iterative is described as:
- Still has a release rhythm and time-scoped content 
- Can produce **very short time between releases** (weeks or a month) 
- Releases are still mini-big-bangs and take months (the work is large, but staggered) 
- Requires multiple teams working concurrently on the same product (different code bases) 
- Feedback can’t be incorporated for several releases because multiple releases are already “in flight.” 

**Added context:** Overlapping iterative reduces time-to-next-release but increases coordination complexity (integration, branching, testing, merging).

---

## Objective 5 — What Iterative still needs up front
Both Iterative and Overlapping Iterative work best when there is:
- **Up-front Requirements Analysis and Architecture Design** before starting the series of releases 
This provides:
- firm understanding of scope
- scaffolding for each release’s design
- early focus on highest priority / biggest ROI items
- reduced risk of a failed iteration (which can cascade in overlapping) 

**Added context:** This is the “don’t skip the foundations” message: even iterative benefits from a stable core architecture.

---

## Objective 6 — Iterative as risk reduction and prototyping
Iterative can also be used to:
- elicit requirements and reduce unknown risks
- put well-known high-value items in early releases
- use early releases as a **prototype** if there aren’t enough features for full production release 

The deck closes with the observation: “Kind of sounds like Agile doesn’t it.” 

**Added context:** The similarity is feedback-driven evolution. The difference (per this deck) is that Iterative still follows the SDLC “waterfall-style” per release, rather than continuously blending phases the way many Agile teams do.

---

## In-class exercises — Calls to action

### In-class exercise: choose the lifecycle model
Pick a product and justify whether Iterative (or Overlapping Iterative) fits better than Waterfall:
- What’s changing (requirements vs environment)?
- How soon do users need value?
- How risky is a late failure?
- Can you afford to wait years for the first real release? 

### In-class exercise: map releases to priority
Write a mini release plan:
- Release 1: highest priority + most certain items
- Release 2+: incorporate feedback + non-P1 defects
- Note how overlapping changes feedback timing 
