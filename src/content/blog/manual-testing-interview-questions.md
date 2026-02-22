---
title: Common Manual Testing Interview Questions (And How to Answer)
description: Typical QA and manual testing interview questions with clear, concise answers to help you prepare.
pubDate: 2025-02-02
tags: [career, interview, basics]
---

If you’re aiming to become a manual tester, interviews often cover the same topics. Here are **common questions** and **short, clear answers** you can adapt.

## 1. What is manual testing?

Manual testing is when a human tester checks the software by using it — following steps, entering data, and checking results — without automated scripts. You verify behavior, look for bugs, and report defects.

## 2. What is the difference between manual and automated testing?

- **Manual:** A person runs tests, observes the app, and decides. Good for exploration, UX, and when things change often.  
- **Automated:** Scripts run tests and compare results. Good for regression and repeated checks.  
Both are used; many testers start with manual and later work with or write automation.

## 3. What are the types of testing you know?

Name a few and give a one-line each: **functional** (does it work as specified?), **regression** (did we break anything?), **smoke** (is the build testable?), **UAT** (is it acceptable for the business?), **exploratory** (learning and testing without a script). You can add compatibility, usability, etc.

## 4. What is a test case? What does it contain?

A test case is a set of steps, data, and expected result to check one specific behavior. It usually has: ID, title, preconditions, steps, test data, expected result, and (when run) actual result and status (Pass/Fail).

## 5. What is a bug report? What should it include?

A bug report describes a defect so developers can reproduce and fix it. It should include: short title, environment, steps to reproduce, expected vs actual result, severity/priority, and screenshots or logs if they help.

## 6. What is severity vs priority?

- **Severity** = impact of the bug (e.g. crash = critical, typo = minor).  
- **Priority** = when to fix it (e.g. before release vs next sprint).  
A typo might be low severity but high priority if it’s on the homepage.

## 7. What is the difference between smoke and sanity testing?

- **Smoke:** Quick check of the main flows after a new build to see if it’s stable enough to test. Broad but shallow.  
- **Sanity:** Narrow check after a small change (e.g. one bug fix) to confirm that area still works.  
Smoke = "Is the build OK?" Sanity = "Is this fix OK?"

## 8. What is regression testing?

Re-running existing tests to ensure new or changed code didn’t break existing functionality. Done after fixes or new features. Can be manual (run a set of test cases) or automated (run a suite).

## 9. What is exploratory testing?

Testing where you design and run tests at the same time — no full script. You explore the product, try things, and look for issues. Good for learning the product and finding unexpected bugs.

## 10. What test design techniques do you know?

- **Equivalence partitioning** — Group inputs that behave the same; test one from each group.  
- **Boundary value analysis** — Test values at and around limits (e.g. min, max, just below, just above).  
- **Decision table** — List combinations of conditions and expected results.  
- **State transition** — Test different states and transitions (e.g. login, lockout).  
Give a short example (e.g. "For a field 1–100, I’d test 0, 1, 100, 101 and one valid value like 50").

## 11. What is STLC?

Software Testing Life Cycle: the phases of testing — requirement analysis, test planning, test case development, environment setup, test execution, and test closure. You can say what you do in each (e.g. "In execution I run test cases, log bugs, and retest fixes").

## 12. When do you stop testing?

When exit criteria are met: e.g. planned tests executed, critical/high bugs fixed, test summary done, and the team (or test lead) agrees to release or to hand over to UAT. Time or budget can also stop testing, but that’s a risk decision.

## Tips for the interview

- Use **simple, concrete examples** (e.g. "For a login field I’d test valid credentials, wrong password, empty fields").  
- Mention **real experience** if you have it (coursework, personal projects, or internships).  
- Show you care about **clear communication** (good bug reports, understandable test cases).  
- Ask **one or two questions** at the end (e.g. "What does a typical release cycle look like?" or "How does the team use manual vs automated testing?").

Use this as a base; adapt answers to your own words and experience so you sound natural and confident.
