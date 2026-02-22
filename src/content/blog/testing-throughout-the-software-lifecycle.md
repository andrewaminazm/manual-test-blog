---
title: Testing Throughout the Software Lifecycle (ISTQB)
description: How testing fits into Waterfall, Agile, and other lifecycle models — test levels, test types, and when testing happens.
pubDate: 2025-01-12
tags: [ISTQB, lifecycle, Agile, Waterfall]
---

Testing is not a single phase at the end of a project. The **ISTQB** emphasizes that testing is **throughout the software lifecycle** and adapts to how the project is run — Waterfall, Agile, or hybrid. As a manual tester you need to know how your work fits into the lifecycle.

## Lifecycle models in short

**Sequential (e.g. Waterfall)** — Phases happen one after another: requirements → design → build → test → release. Testing often appears "late" but test planning and design can start early (e.g. after requirements). Test levels (component, integration, system, acceptance) still apply.

**Iterative / incremental** — The product is built in cycles; each cycle adds functionality. Testing happens in each iteration (design tests, execute, report). Regression grows over time.

**Agile** — Short iterations (sprints), working software frequently, close collaboration. Testing is **continuous** in the sprint: analyze stories, design and execute tests, log bugs, retest. Testers work alongside developers; there may still be a dedicated "release" or "hardening" phase for broader regression.

**DevOps / Continuous Delivery** — Code is integrated and deployed often; automated tests run in pipelines. Manual testing focuses on exploratory, UAT-like, or areas not automated. Testing is "everyone’s job" and happens throughout.

---

## Test levels in the lifecycle

Whatever the model, the **test levels** still apply (see the Test Levels post):

- **Component** — Usually in the build phase (developers).
- **Integration** — As components or systems are integrated.
- **System** — When a complete system or increment is available.
- **Acceptance** — When the product (or increment) is ready for business/user acceptance.

In **Waterfall**, these often map to phases. In **Agile**, you might do integration and system testing every sprint, and acceptance (e.g. UAT) at the end of a release or sprint.

---

## Test types in the lifecycle

**Test types** (functional, non-functional, etc.) can be run at different **levels**:

- **Functional** — At component, integration, system, and acceptance.
- **Non-functional** (e.g. performance, security) — Often at system level when the system is stable enough.
- **Regression** — After changes, at the level where the change was integrated (e.g. system regression before release).

So we think: "At this **level** (e.g. system), we run these **types** (e.g. functional, regression)."

---

## Testing in Agile (practical)

- **Every sprint** — Testers analyze user stories, design test cases, execute tests, log defects, and retest. You’re part of the team from the start of the sprint.
- **Definition of Done** — Often includes "tested" and "acceptance criteria met." Your tests and sign-off support that.
- **Continuous feedback** — Daily standups, demos, and retrospectives. Testing is visible and integrated.
- **Regression** — As the product grows, regression can be automated (e.g. CI) or a dedicated manual regression suite run before release.
- **Release / UAT** — Before a release there may be a short hardening period and UAT with business or users.

---

## What you do as a manual tester

- **Align with the lifecycle** — In Waterfall, follow the test plan and phases; in Agile, work in the sprint and adapt test design and execution to story size and timing.
- **Start early** — In any model, get involved as soon as there’s something to review or analyze (requirements, stories, design). Don’t wait for "test phase."
- **Know your test levels and types** — So you can say "we’re doing system functional testing this sprint" or "we’re in UAT for release 2."

ISTQB expects you to understand that testing is **not** only a phase at the end but an activity **throughout** the lifecycle, and that the way you do it depends on the lifecycle model your project uses.
