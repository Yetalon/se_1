# Software Engineering — Day 11
## Topic: Source Control (Version Control Systems / Configuration Management) 

## Overview

| section | what you’ll learn | do this |
|---|---|---|
| [**Main objectives**](#main-objectives) | What you should walk away with today | Skim first to orient yourself |
| [**Why source control matters**](#objective-1--why-source-control-matters) | Real pain it prevents (lost work, broken demos, overwrites) | Write 3 “source control horror stories” you’ve experienced |
| [**Types of VCS**](#objective-2--types-of-version-control-systems) | Local vs centralized vs distributed (user perspective: similar) | Identify which model Git is |
| [**Core concepts: repo, checkout, commit, merge**](#objective-3--core-concepts-and-how-collaboration-works) | Repos as DBs, parallel edits, merge conflicts | Explain what a merge conflict is |
| [**Working with releases & versioning**](#objective-4--releases-tagging-and-semantic-versioning) | Why prod is separated; tags; semver; patch propagation | Describe Major/Minor/Patch using the SHAZAAM example |
| [**Common terms (the “library” analogy)**](#objective-5--common-terms-with-the-library-analogy) | Branch, commit, PR, merge, baseline, trunk | Translate analogy ↔ Git terms |
| [**Branching workflow examples**](#objective-6--branching-workflows-the-shazaam-examples) | Concurrent features + post-release minor updates | Be able to narrate the workflow in plain English |
| [**Scrum connection**](#objective-7--scrum-frequent-releases-and-why-versioning-explodes) | Why frequent releases reduce conflicts but create tracking burden | Explain why SaaS makes this easier |
| [**Readings / prep**](#readings--prep) | Required + optional reading links from slides | Do the required tutorial before the in-class exercise |

---

## Main objectives
1) Understand what source control is and the problems it solves 
2) Learn key VCS concepts (repo, checkout, commit, branch, merge, PR, baseline) 
3) Understand versioning and release management basics (semantic versioning, tags, patch propagation) 
4) Understand how source control supports teamwork and frequent releases (Scrum) 

---

## Objective 1 — Why source control matters
The deck opens with common “pain” scenarios:
- You changed something right before a demo and it broke everything
- A teammate overwrote your changes and they’re gone
- You wish you could go back to code from two weeks ago
- You copied a program to extend it, but then had to fix the same bug in multiple places 

Source control helps solve these issues and becomes essential once more than one person touches the same code (or docs). 

---

## Objective 2 — Types of version control systems
Source Control = Version Control System (VCS). The deck lists three types:
- Local
- Centralized
- Distributed  
From a user perspective, they function similarly. 

**Added context:** Git is a distributed VCS. GitHub is a hosting/collaboration platform on top of Git.

---

## Objective 3 — Core concepts and how collaboration works
### Repository and check-in/out model
- VCS stores code/files in a **repository** (a database).
- You **check out** a file, modify it, then **check it back in**.
- Unlike a library, multiple people can check out the same file at the same time.
- The VCS tries to reconcile changes when checking in; if it can’t → **merge conflicts**. 

### Version-aware behavior
- VCS supports multiple versions of a codebase (example given: Windows 10 vs 11 sharing code + differences).
- You check out a file from a specific version, check it back into that version, and may later pull changes forward. 

---

## Objective 4 — Releases, tagging, and semantic versioning
### Why releases complicate everything
- After first release, production must remain separate from development.
- As releases accumulate, you must track and support them.
- Bug fixes in earlier versions often must be propagated forward because the bug likely exists in later versions too. 

### Semantic versioning (SemVer)
Production code is tagged/versioned with a release process. Typical format described:
`NAME_Major#_Minor#_PATCH#` (SemVer style). 

Version meanings:
- **Major**: major new features; possibly drastic UX changes (note: deck mentions Scrum sometimes maps major# to sprint#).
- **Minor**: minor features + bug fixes
- **Patch**: small number of changes, primarily high-priority bug fixes 

### Patch propagation example (Portal)
The deck’s example:
- Release `Portal_1_0_0`
- Begin new work `Portal_1_1_0`
- Discover critical flaw in `Portal_1_0_0` → release patch `Portal_1_0_1`
- Pull that fix into `Portal_1_1_0` (unreleased), so no version change needed there
- Key rule: you don’t modify a released version; you ship a new version 

---

## Objective 5 — Common terms with the “library” analogy
The deck maps terms like this:
- Repository = city with lots of libraries
- Branch = a single library with lots of books
- Files = a book with multiple editions
- Commit = checking a book into the local library
- Pull Request = asking someone to read a book you like
- Merge = reconciling differences between two versions
- Baseline = like a published edition 

**Added context:** In Git vocabulary you’ll also hear:
- “main” / “trunk” as the primary branch,
- “tag” as a named pointer to a commit used for releases.

---

## Objective 6 — Branching workflows: the SHAZAAM examples
### Concurrent feature work (dependency between devs)
Scenario: you and Bobby work on features concurrently; Bobby depends on your partial results.
Workflow described:
- You branch off main labeled `SHAZAAM_1_0_0_Dev`
- Bobby branches off same baseline
- You commit changes; merge back to main via pull request
- Bobby pulls your changes, merges into his, finishes work, then merges back 

### Post-release minor update workflow
After releasing `SHAZAAM_1_0_0`, you start a minor update:
- Create `SHAZAAM_1_1_0_Dev` off trunk
- Branch again for a smaller work stream (e.g., `SHAZAAM_1_1_0_Dev_minor`)
- Make changes → merge back → commit
- No impact to production version 

---

## Objective 7 — Scrum: frequent releases and why versioning explodes
Scrum expectations listed:
- frequent releases (monthly, sometimes daily)
- small teams (5–9), which helps avoid merge conflicts
But frequent releases create lots of versions to track:
- great for a single customer
- hard if deploying to hundreds/thousands of places
- great for cloud SaaS (one deployed copy, many customers) 

**Added context:** This is one reason modern teams invest heavily in CI/CD and automated testing—release frequency only works if you can ship safely.

---

## Readings / prep
### Required reading (before the in-class exercise)
- A Git/GitHub team workflow tutorial is explicitly marked as required reading in the slides. 

### Optional reading (now; recommended later for projects)
- GitHub “Managing releases in a repository” is listed as optional now, but highly recommended when you start doing releases for the semester project. 

---

## In-class exercises — Calls to action
### In-class exercise (implied by the deck)
Be ready to perform the team workflow:
- branch
- commit
- pull request
- merge
- pull changes
…and deal with merge conflicts if they occur. 
