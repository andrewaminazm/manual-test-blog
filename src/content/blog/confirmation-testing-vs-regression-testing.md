---
title: Confirmation Testing vs Regression Testing (ISTQB)
description: Retesting a fix (confirmation testing) versus re-running tests to catch side effects (regression) — and why both matter.
pubDate: 2025-01-08
tags: [ISTQB, regression, retest]
---

**Confirmation testing** and **regression testing** are two different activities that often happen after a defect is fixed. The **ISTQB** distinguishes them clearly. As a manual tester you do both; here’s the difference.

## Confirmation testing (re-testing)

**What:** After a developer **fixes a defect**, you **re-run the test(s) that failed** (or the steps that found the bug) to check that the fix works and the **original issue is gone**.

**Goal:** Confirm the specific defect is fixed.

**Scope:** Only the test case(s) or scenario(s) related to that bug.

**Example:** Bug "Login fails when Remember me is checked." Developer fixes it. You run the same steps again (valid login + Remember me) and verify login now works. That’s confirmation testing.

**When:** Every time a bug is marked "Fixed" and sent for retest. It’s part of the defect life cycle.

---

## Regression testing

**What:** Re-run **existing tests** (often a larger set) to check that the **fix or any other change didn’t break something else**. You’re not only checking the fixed bug; you’re checking that the rest of the system still works.

**Goal:** Find regressions — unintended side effects or old bugs coming back.

**Scope:** A set of tests (e.g. critical path, full regression suite, or tests for affected area). Usually broader than one test case.

**Example:** After the login fix, you run not only the "Remember me" test but also: normal login, logout, password reset, and maybe a few other auth-related tests. If the team runs a full regression, you run the whole suite.

**When:** After fixes, after new features are integrated, or before release. Can be manual or automated.

---

## Side by side

|                     | Confirmation testing       | Regression testing              |
|---------------------|----------------------------|---------------------------------|
| **Trigger**         | A defect was fixed         | A change (fix or new feature)   |
| **Question**        | Is this bug fixed?         | Did we break anything else?     |
| **Scope**           | The test(s) for that bug   | A set of existing tests         |
| **Frequency**       | Every fix (retest)         | After changes / before release  |

---

## In practice

1. Developer fixes bug → you do **confirmation testing** (re-run the failing test). If it passes, you close the bug. If it fails, you reopen.
2. After one or more fixes (or a new build), you run **regression testing** on the agreed set of tests to catch regressions.
3. Confirmation is **mandatory** for every fix you retest. Regression is **scheduled** (e.g. end of sprint, before release) and may be partly automated.

ISTQB exam questions often ask: "After a fix, the tester re-runs the test that failed. What is this?" Answer: **confirmation testing** (re-testing). If they re-run a **suite** of tests to check for side effects, that’s **regression testing**. Knowing the difference helps you use the right terms and plan your work correctly.
