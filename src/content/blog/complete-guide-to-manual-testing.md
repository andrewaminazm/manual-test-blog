---
title: The Complete Guide to Manual Testing (Start Here)
description: "Everything a manual tester needs to know — from fundamentals and ISTQB principles to test design, bug reporting, real-life scenarios, and career prep. One place, zero fluff."
pubDate: 2025-02-22
tags: [complete guide, basics, ISTQB, career]
---

Whether you are just starting out or preparing for a QA interview, this guide covers **everything** you need to know about manual testing — in a logical order, with links to detailed articles for each topic. Bookmark it and work through it at your own pace.

---

## Part 1 — Foundations

### What is manual testing?

Manual testing is when a human tester uses the software — clicking, entering data, observing behavior — to verify it works as expected. No scripts, just a tester with a plan and an eye for problems.

**Why it still matters:**
- Catches usability issues automation never sees.
- Flexible when the product changes fast.
- Provides the human judgment that automated checks cannot replace.

→ **Read:** [What Is Manual Testing? A Clear Definition for Beginners](/blog/what-is-manual-testing)

---

### The 7 principles of testing (ISTQB)

Before you write a single test case, understand the rules that govern testing:

1. **Testing shows presence of defects** — not their absence.
2. **Exhaustive testing is impossible** — use risk and techniques to prioritize.
3. **Early testing saves time and cost** — start as soon as there's something to review.
4. **Defects cluster** — a few modules usually hold most of the bugs.
5. **Pesticide paradox** — run the same tests forever and they stop finding bugs. Evolve them.
6. **Testing is context-dependent** — medical software ≠ e-commerce site.
7. **Absence of defects is a fallacy** — zero bugs doesn't mean fit for use.

→ **Read:** [Seven Principles of Testing (ISTQB)](/blog/seven-principles-of-testing-istqb)

---

### The Software Testing Life Cycle (STLC)

Testing isn't one activity — it's a sequence of phases. Understanding STLC tells you **what you're doing and when**:

| Phase | What happens |
|-------|-------------|
| Requirement analysis | Understand what to test; clarify gaps |
| Test planning | Define scope, approach, schedule, risks |
| Test design | Write test cases and prepare test data |
| Environment setup | Get the environment ready; run smoke |
| Test execution | Run tests, log results, report bugs, retest |
| Test closure | Summarize results, archive artifacts |

→ **Read:** [Software Testing Life Cycle (STLC) Explained](/blog/software-testing-life-cycle-stlc)

Also related — the **ISTQB generic test process** (planning → monitoring → analysis → design → implementation → execution → completion):

→ **Read:** [The Test Process — Planning to Completion (ISTQB)](/blog/test-process-activities-istqb)

---

### Testing throughout the software lifecycle

Testing adapts to the project model — Waterfall, Agile, or DevOps. In Agile you test every sprint. In Waterfall you have defined phases. In DevOps, testing is continuous.

→ **Read:** [Testing Throughout the Software Lifecycle (ISTQB)](/blog/testing-throughout-the-software-lifecycle)

---

## Part 2 — Types and Levels of Testing

### Test levels

There are four levels; as a manual tester you mostly work at **system** and **acceptance**:

| Level | Scope | Who |
|-------|-------|-----|
| Component (unit) | Single unit | Developer |
| Integration | Units working together | Dev / Tester |
| System | Complete system end-to-end | **Tester** |
| Acceptance (UAT) | Business fit for release | Business / User |

→ **Read:** [Test Levels — Component, Integration, System, Acceptance (ISTQB)](/blog/test-levels-component-integration-system-acceptance)

---

### Types of manual testing

Every project uses a mix of testing types. Here's the quick reference:

- **Functional** — Does it match requirements?
- **Regression** — Did the new build break existing features?
- **Smoke** — Is the build stable enough to test?
- **Sanity** — Does this specific fix work?
- **Exploratory** — Find unexpected issues without a script.
- **UAT** — Is it acceptable for the business?
- **Compatibility** — Works on target browsers and devices?
- **Usability** — Is it easy and pleasant to use?

→ **Read:** [Types of Manual Testing Explained](/blog/types-of-manual-testing)

---

### Confirmation testing vs regression testing

Two things you do after every fix:

- **Confirmation (retest)** — Does the fixed bug stay fixed?
- **Regression** — Did the fix break anything else?

→ **Read:** [Confirmation Testing vs Regression Testing (ISTQB)](/blog/confirmation-testing-vs-regression-testing)

---

### User acceptance testing (UAT)

UAT is where business users validate the product before go-live. As a tester you prepare scenarios, environment, and data — then support users during execution.

→ **Read:** [User Acceptance Testing (UAT) — What It Is and Your Role](/blog/user-acceptance-testing-uat)

---

### Exploratory testing

No script. You learn and test simultaneously, guided by a **mission** and **time-box**. Essential for finding the bugs scripted tests miss.

→ **Read:** [Exploratory Testing Basics](/blog/exploratory-testing-basics)

---

## Part 3 — Requirements and Test Basis

### The BRD (Business Requirements Document)

The BRD defines what the business needs. As a tester, it's one of your primary **test bases** — the source from which you derive test conditions and test cases.

→ **Read:** [What Is a BRD (Business Requirements Document)?](/blog/what-is-a-brd-business-requirements-document)

---

### How to analyze a BRD for testing

Knowing a BRD exists isn't enough — you need to read it with a tester's eye:

1. Understand scope and objectives.
2. Extract testable requirements.
3. Flag ambiguous and vague language.
4. Identify gaps and missing edge cases.
5. Derive test conditions.

→ **Read:** [How to Analyze a BRD for Testing](/blog/how-to-analyze-a-brd-for-testing)

---

### Static testing — reviews and analysis

You can find defects **without running the software**. Reviews of requirements, test cases, and design documents catch problems early and cheaply.

Review types: informal → walkthrough → technical review → inspection (most formal).

→ **Read:** [Static Testing — Reviews and Static Analysis (ISTQB)](/blog/static-testing-reviews-and-static-analysis)

---

## Part 4 — Test Design

### How to write a test case

A test case is the core deliverable of a manual tester. Every good test case has:

- **ID** — unique reference.
- **Title** — what is being tested.
- **Preconditions** — what must be true before you start.
- **Steps** — numbered actions.
- **Test data** — exact inputs.
- **Expected result** — what "pass" looks like.
- **Actual result + status** — filled during execution.

→ **Read:** [How to Write a Test Case (Step-by-Step)](/blog/how-to-write-a-test-case)

---

### Test design techniques

Don't test every possible value — use techniques to get strong coverage with fewer cases:

| Technique | When to use |
|-----------|------------|
| Equivalence partitioning | Any input with valid/invalid groups |
| Boundary value analysis | Fields with ranges or limits |
| Decision table | Business rules with multiple conditions |
| State transition | Flows with clear states (login, order status) |
| Scenario / use case | End-to-end user journeys |

→ **Read:** [Test Design Techniques for Manual Testers](/blog/test-design-techniques)

---

### Black-box, white-box, and experience-based techniques (ISTQB)

ISTQB classifies all techniques into three families:

- **Black-box** — Based on spec (equivalence partitioning, BVA, decision table, state transition).
- **White-box** — Based on code structure (statement, branch, path coverage).
- **Experience-based** — Based on tester knowledge (exploratory, error guessing, checklist).

Manual testers primarily use **black-box** and **experience-based**.

→ **Read:** [Black-Box, White-Box, and Experience-Based Techniques (ISTQB)](/blog/black-box-white-box-experience-based-techniques-istqb)

---

### Practical example: testing a login page

Put design techniques into practice on one of the most common features — the login page. Covers functional, security (SQL injection, XSS, HTTPS), usability, and edge cases with a full checklist.

→ **Read:** [How to Test a Login Page — Complete Guide with Test Cases](/blog/how-to-test-a-login-page-complete-guide)

---

### Real-life business scenarios and test cases

Four domains, 15 ready-to-use test cases:

- **E-commerce** — Add to cart, checkout, coupon, guest validation.
- **Login and registration** — Valid login, lockout, duplicate email.
- **Banking** — Fund transfer within/over balance/daily limit.
- **Order returns** — Eligible item, expired window, partial return.

→ **Read:** [Real-Life Business Scenarios and Test Cases](/blog/real-life-business-scenarios-and-test-cases)

---

## Part 5 — Bug Reporting

### How to write a bug report that gets fixed

A great bug report includes:

1. **Title** — one-sentence summary.
2. **Environment** — OS, browser, app version.
3. **Steps to reproduce** — numbered, precise.
4. **Expected vs actual result** — the core of the report.
5. **Severity / priority** — how bad and how urgent.
6. **Attachments** — screenshot or recording.

→ **Read:** [How to Write a Bug Report That Gets Fixed](/blog/how-to-write-a-bug-report)

---

### The defect life cycle

A bug doesn't disappear when you log it. It goes through states:

```
New → Assigned → Open → Fixed → [Retest]
                                     ↓
                  Pass → Closed   |   Fail → Reopened → ...
```

Also: Deferred, Won't Fix, Duplicate.

→ **Read:** [Defect Life Cycle (Bug Life Cycle)](/blog/defect-life-cycle)

---

## Part 6 — Test Planning and Management

### Test planning and the test plan document

A test plan answers: What will we test? How? When? Who? With what? The main sections:

- Scope (in / out)
- Test strategy and approach
- Schedule and resources
- Entry / exit criteria
- Risks and mitigations

→ **Read:** [Test Planning and the Test Plan Document](/blog/test-planning-and-test-plan)

---

### Risk-based testing

You can't test everything — focus on **risk**. High likelihood × high impact = test first, most, and deepest.

Steps:
1. Identify product risks (what could go wrong?).
2. Assess likelihood and impact.
3. Prioritize test cases by risk.
4. Re-assess when things change.

→ **Read:** [Risk-Based Testing (ISTQB)](/blog/risk-based-testing-istqb)

---

### Test metrics and when to stop testing

What to measure: tests planned vs executed, pass/fail rate, defects by severity, coverage, open critical bugs.

When to stop: exit criteria are met — e.g. 100% P0/P1 run, pass rate ≥ 95%, no open critical bugs, stakeholder sign-off.

→ **Read:** [Test Metrics and When to Stop Testing (ISTQB)](/blog/test-metrics-and-when-to-stop-testing)

---

### Test documentation and traceability

Key documents: test plan, test cases, execution results, bug reports, test summary report, requirements traceability matrix (RTM).

The **RTM** maps: Requirement ID ↔ Test Case ID ↔ Bug (if any). Shows coverage and supports reporting.

→ **Read:** [Test Documentation and Traceability](/blog/test-documentation-and-traceability)

---

### Independent testing and test organization

Why independence matters and how it works. Levels of independence — from developer self-testing to fully independent test team. Roles: tester, test lead, test analyst.

→ **Read:** [Independent Testing and Test Organization (ISTQB)](/blog/independent-testing-and-test-organization)

---

### Test tools

The main tool categories every manual tester uses:

- **Test management** — TestRail, Zephyr, Xray (write and run test cases, record results).
- **Bug tracking** — Jira, Bugzilla, Azure DevOps (log and track defects).
- **API testing** — Postman (test REST APIs without UI).

→ **Read:** [Test Tools — Support for Testing (ISTQB)](/blog/test-tools-support-for-testing-istqb)

---

## Part 7 — API Testing

### API testing for manual testers

You don't need to be a developer to test APIs. With Postman you can:

- Send GET, POST, PUT, DELETE requests.
- Verify status codes (200, 201, 400, 401, 404, 500).
- Validate response body, data types, and error messages.
- Run negative cases (wrong credentials, missing fields, invalid format).

→ **Read:** [API Testing for Manual Testers (With Postman)](/blog/api-testing-for-manual-testers)

---

## Part 8 — Career and Interviews

### Common manual testing interview questions

Prepared answers for the most common QA interview questions:

- What is manual testing vs automated?
- What are the types of testing you know?
- What is a test case / bug report?
- What is severity vs priority?
- What is regression / exploratory testing?
- What test design techniques do you know?
- What is STLC?
- When do you stop testing?

→ **Read:** [Common Manual Testing Interview Questions (And How to Answer)](/blog/manual-testing-interview-questions)

---

## Your learning roadmap

Use this order if you're starting from scratch:

```
1. What Is Manual Testing           →  understand the role
2. 7 Principles                     →  the mindset
3. STLC + Test Process              →  the structure
4. Types and Levels of Testing      →  what you test when
5. BRD and Static Testing           →  understand requirements
6. Write Test Cases                 →  core skill
7. Test Design Techniques           →  design smarter
8. Write Bug Reports + Defect LC    →  report clearly
9. Test Planning + Risk             →  think like a lead
10. Exploratory Testing             →  beyond scripted
11. UAT                             →  business perspective
12. API Testing (Postman)           →  broaden your skills
13. Metrics, Docs, Tools            →  professional habits
14. Interview Questions             →  career ready
```

---

## At a glance — complete topic index

| Topic | Article |
|-------|---------|
| What is manual testing | [Read →](/blog/what-is-manual-testing) |
| 7 Principles of testing | [Read →](/blog/seven-principles-of-testing-istqb) |
| STLC | [Read →](/blog/software-testing-life-cycle-stlc) |
| Test process (ISTQB) | [Read →](/blog/test-process-activities-istqb) |
| Testing in the lifecycle | [Read →](/blog/testing-throughout-the-software-lifecycle) |
| Test levels | [Read →](/blog/test-levels-component-integration-system-acceptance) |
| Types of manual testing | [Read →](/blog/types-of-manual-testing) |
| Confirmation vs regression | [Read →](/blog/confirmation-testing-vs-regression-testing) |
| UAT | [Read →](/blog/user-acceptance-testing-uat) |
| Exploratory testing | [Read →](/blog/exploratory-testing-basics) |
| BRD — what it is | [Read →](/blog/what-is-a-brd-business-requirements-document) |
| Analyze a BRD | [Read →](/blog/how-to-analyze-a-brd-for-testing) |
| Static testing | [Read →](/blog/static-testing-reviews-and-static-analysis) |
| Write a test case | [Read →](/blog/how-to-write-a-test-case) |
| Test design techniques | [Read →](/blog/test-design-techniques) |
| Black/white/experience-based | [Read →](/blog/black-box-white-box-experience-based-techniques-istqb) |
| Test a login page | [Read →](/blog/how-to-test-a-login-page-complete-guide) |
| Real-life scenarios & test cases | [Read →](/blog/real-life-business-scenarios-and-test-cases) |
| Write a bug report | [Read →](/blog/how-to-write-a-bug-report) |
| Defect life cycle | [Read →](/blog/defect-life-cycle) |
| Test plan | [Read →](/blog/test-planning-and-test-plan) |
| Risk-based testing | [Read →](/blog/risk-based-testing-istqb) |
| Test metrics and exit criteria | [Read →](/blog/test-metrics-and-when-to-stop-testing) |
| Test docs and traceability | [Read →](/blog/test-documentation-and-traceability) |
| Independent testing | [Read →](/blog/independent-testing-and-test-organization) |
| Test tools | [Read →](/blog/test-tools-support-for-testing-istqb) |
| API testing with Postman | [Read →](/blog/api-testing-for-manual-testers) |
| Interview questions | [Read →](/blog/manual-testing-interview-questions) |

---

*This guide is updated as new articles are added. If you find a topic missing or have a question, connect on [LinkedIn](https://www.linkedin.com/in/andrew-amin-48763a194/) — happy to help.*
