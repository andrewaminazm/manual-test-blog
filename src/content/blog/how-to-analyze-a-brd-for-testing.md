---
title: How to Analyze a BRD for Testing
description: Practical steps and checklist for testers — how to read a BRD, find testable requirements, spot gaps and ambiguities, and prepare for test design.
pubDate: 2025-01-05
tags: [BRD, requirements, test analysis]
---

**Analyzing a BRD for testing** means reading the Business Requirements Document (and any linked specs or stories) to understand what to test, what’s missing or unclear, and what risks to cover. This is part of **test analysis** in the ISTQB test process. Here’s a practical way to do it.

## Why analyze the BRD?

- **Design the right tests** — You need to know *what* the system should do before you design test cases.
- **Find problems early** — Ambiguous or missing requirements cause rework and bugs; catching them in the BRD saves cost.
- **Build traceability** — You’ll link test cases to requirements; analyzing the BRD helps you list those requirements clearly.
- **Support reviews** — You can take part in requirement reviews (static testing) and suggest improvements from a tester’s perspective.

---

## Step 1: Understand context and scope

**Read first:**
- **Purpose and business objectives** — Why is this project happening? That helps you prioritize (e.g. compliance or revenue-critical areas get more test focus).
- **In scope / out of scope** — What you *must* test vs what is explicitly excluded. If something is out of scope, you don’t design tests for it (unless you’re asked to confirm it’s *not* implemented).
- **Assumptions and constraints** — They affect test environment, data, and what’s possible (e.g. “Assumption: users have Chrome or Edge” → you may test on those; “Constraint: go-live by March” → affects test schedule).

**Note:** List any requirement or area that’s vague (“TBD”, “to be defined”) so you can follow up or flag risk.

---

## Step 2: Extract and list testable requirements

**Identify each requirement** that describes behavior or a condition the system must meet. In a BRD they might be:
- Numbered (e.g. BR-001, BR-002),
- Under “Business requirements” or “Functional requirements,” or
- In process/functional areas.

**For each requirement, ask:**
- **Can we test this?** If it’s too high-level (e.g. “Improve customer satisfaction”), you need a more detailed spec or user story to derive test cases. Note: “Needs refinement for testability.”
- **What would “pass” look like?** If you can’t define pass/fail, the requirement is not testable yet — flag it.
- **Is it measurable or observable?** (e.g. “User can reset password in under 2 minutes” is testable; “User should feel confident” is not, unless defined in a testable way.)

**Output:** A list of **testable requirements** (or requirement IDs) and a list of items that need **clarification or refinement** before you can design tests.

---

## Step 3: Check for clarity and ambiguity

Unclear requirements lead to wrong tests and disputes. Look for:

**Vague words (examples):**
- “Appropriate,” “reasonable,” “as needed,” “user-friendly,” “fast,” “secure” — Ask: *What exactly must the system do?* Request concrete, testable criteria.
- “Sometimes,” “normally,” “usually” — When exactly? Under what conditions? Ask for clear rules.

**Missing details:**
- **Who** — Which user role? (e.g. “Admin” vs “Customer” — different tests.)
- **When / under what condition** — Triggers, preconditions, and business rules (e.g. “When balance &lt; 0, then …”).
- **What exactly** — Inputs, outputs, validation rules, error messages, and business logic (e.g. discount rules, rounding, limits).

**Contradictions:**
- Same topic described differently in different sections — Note and ask for one agreed version.

**Output:** A **clarification list** (questions, ambiguities, contradictions) to send to BA/product. Use this in requirement reviews (static testing).

---

## Step 4: Identify gaps and dependencies

**Gaps:**
- **Missing requirements** — Obvious flows or rules that aren’t stated (e.g. “What happens when session expires during checkout?” “Can the user cancel after payment?”). List as “Potential gap — confirm.”
- **Edge cases and exceptions** — Error handling, invalid input, timeouts, duplicate actions. BRDs often omit these; you’ll need to ask or derive from standards.

**Dependencies:**
- **Other systems or data** — “Depends on CRM” or “Uses pricing from ERP.” You need to know how you’ll test when those aren’t available (stubs, test environments, test data).
- **Order of implementation** — If Feature B depends on Feature A, your test order and environment setup depend on that.

**Output:** List of **gaps** and **dependencies**; discuss with BA/product and plan test data/environment accordingly.

---

## Step 5: Derive test conditions (test analysis)

For each testable requirement, write **test conditions** — short statements of *what* you want to test. They become the basis for test cases later.

**Example:**

| Requirement | Test condition |
|-------------|-----------------|
| BR-003: User can reset password via email link. | TCond-1: Valid email receives reset link. |
| | TCond-2: Reset link expires after 24 hours. |
| | TCond-3: Invalid or expired link shows clear message. |
| | TCond-4: Used link cannot be reused. |

**Cover:**
- **Happy path** — Normal, valid scenario.
- **Alternatives** — Other valid paths (e.g. reset via SMS if in scope).
- **Error/negative** — Invalid input, expired link, wrong user.
- **Boundaries** — Limits (e.g. link validity 24 hours → test just before and after).

**Output:** **Test conditions** (and optionally a first version of a **traceability matrix**: requirement ID ↔ test condition ID).

---

## Step 6: Use a simple BRD analysis checklist

You can run through this when reading any BRD:

- [ ] Scope (in/out) and assumptions/constraints are clear.
- [ ] Every requirement has a unique ID and is stated in one place.
- [ ] Each requirement is testable (observable, measurable, or has defined pass/fail).
- [ ] No vague terms without definition (or they’re in the glossary).
- [ ] User roles and actors are identified where relevant.
- [ ] Business rules (including calculations and validations) are explicit.
- [ ] Error behavior and edge cases are described or flagged for clarification.
- [ ] Dependencies (other systems, features, data) are identified.
- [ ] I have a list of questions/clarifications and a list of test conditions (or requirement IDs to cover).

---

## What you do with the results

- **Clarifications** → Send to BA/product; use in review meetings.
- **Test conditions** → Feed into **test design** (next step: design test cases with steps, data, expected results).
- **Traceability** → Keep requirement ID ↔ test condition (and later test case) in your test management tool or traceability matrix.
- **Risks** — If many requirements are unclear or out of scope, raise a **project/test risk** (e.g. “High risk of rework and missed defects if requirements not finalized by X date”).

Analyzing the BRD well makes test design easier, reduces rework, and helps you align tests with what the business actually needs — which is the goal of requirement-based testing.
