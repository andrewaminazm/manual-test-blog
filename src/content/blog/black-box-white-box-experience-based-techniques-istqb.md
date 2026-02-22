---
title: Black-Box, White-Box, and Experience-Based Techniques (ISTQB)
description: How ISTQB classifies test design techniques and when to use each category as a manual tester.
pubDate: 2025-01-20
tags: [ISTQB, test design, black box, white box]
---

The **ISTQB Foundation** groups test design techniques into **black-box**, **white-box**, and **experience-based**. As a manual tester you’ll use mainly **black-box** and **experience-based**; knowing all three helps you choose the right technique and speak the ISTQB language.

## Black-box test techniques

**Idea:** You design tests from the **specification (or behavior)** of the system, **without** looking at internal structure (code, architecture). You treat the system as a "black box": input in, output out.

**Typical techniques (ISTQB):**

- **Equivalence partitioning** — Group inputs that should be treated the same; test one from each partition.
- **Boundary value analysis** — Test at and around boundaries (min, max, just below, just above).
- **Decision table testing** — Conditions and actions in a table; one test per combination.
- **State transition testing** — Test states and transitions (e.g. login, lockout).
- **Use case testing** — Test scenarios based on use cases or user flows.

**When to use:** For functional requirements, business rules, inputs and outputs. This is the bread and butter of manual test design. (See the "Test Design Techniques" post for examples.)

---

## White-box test techniques

**Idea:** You design tests using knowledge of the **internal structure** of the system — code, control flow, branches, conditions. You aim for coverage of statements, branches, or paths.

**Typical techniques:**

- **Statement coverage** — Every statement executed at least once.
- **Branch/decision coverage** — Every decision (true and false) taken at least once.
- **Condition coverage** — Every condition in a decision evaluated true and false.
- **Path coverage** — Cover specific paths through the code (often only partial due to complexity).

**Who uses them:** Mostly **developers** (unit testing, code coverage). As a **manual tester** you usually don’t design white-box tests directly, but you may use **coverage reports** to see what code was exercised and where to add or focus black-box tests.

---

## Experience-based test techniques

**Idea:** Tests are based on **tester (or user) experience, intuition, and knowledge** of the product, domain, or typical failures — not only on a written specification or code structure.

**Typical techniques:**

- **Exploratory testing** — Simultaneous learning, test design, and execution; no pre-written script. (See the Exploratory Testing post.)
- **Error guessing** — Use experience to guess where defects might be (e.g. empty input, special characters, first/last item in a list) and design tests for those.
- **Checklist-based testing** — Use checklists (e.g. "typical failure modes", "what usually breaks") to guide what to test; the checklist comes from experience.

**When to use:** When specs are vague or missing, when you need to find unexpected issues, or to complement specification-based techniques. Very useful for manual testers.

---

## Summary (ISTQB view)

| Category            | Basis for tests              | Typical user      | Manual tester use        |
|---------------------|-----------------------------|-------------------|---------------------------|
| Black-box           | Specification, behavior     | Testers           | Main way you design tests |
| White-box           | Internal structure, code    | Developers        | Use coverage info, not design |
| Experience-based    | Experience, intuition        | Testers           | Exploratory, error guessing |

In practice you **combine** them: black-box for requirements-based cases, experience-based for exploratory and risk areas, and (if available) white-box coverage to see gaps. ISTQB exams often ask which technique is black-box vs white-box vs experience-based — this table helps you classify them.
