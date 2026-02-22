---
title: Test Documentation and Traceability
description: Test artifacts, traceability matrix, and why documenting tests matters for manual testers.
pubDate: 2025-02-01
tags: [documentation, traceability, test plan]
---

Good **test documentation** helps the team know what was tested, what passed or failed, and how tests link to requirements. As a manual tester, you create and use these artifacts every day.

## Common test deliverables

**Test plan** — Describes scope, approach, schedule, and criteria for testing (see the Test Planning post).

**Test cases** — The actual cases: steps, data, expected results. Stored in a tool (Jira, TestRail, Zephyr, etc.) or in spreadsheets/docs.

**Test data** — Data used for testing (e.g. user accounts, product IDs). May be documented in a sheet or in the test case itself.

**Bug reports** — Defects you log with steps, expected vs actual, severity, and status.

**Test execution results** — Which test cases were run, pass/fail, date, environment, and tester name. Usually in the same tool as test cases.

**Test summary report** — A short report at the end of a cycle: how many tests run, pass/fail counts, critical bugs, and whether exit criteria are met.

**Traceability matrix** — A mapping between requirements and test cases (and sometimes bugs). Shows "which tests cover which requirement."

## What is a traceability matrix?

A **traceability matrix** (RTM — Requirements Traceability Matrix) is a table that links:

- **Requirements** (or user stories) ↔ **Test cases** ↔ optionally **Bugs**

Example:

| Requirement ID | Requirement description   | Test case IDs   | Status    |
|----------------|---------------------------|-----------------|-----------|
| REQ_001        | User can log in with email| TC_LOGIN_01–05  | Executed  |
| REQ_002        | User can reset password   | TC_PWD_01–03    | Executed  |

**Why it’s useful:**

- **Coverage** — You see which requirements have test cases and which don’t.
- **Impact** — When a requirement changes, you know which test cases to update or run.
- **Reporting** — You can say "We have N requirements and M test cases; X% of requirements are covered and Y% passed."

You might maintain it in Excel/Sheets or in a test management tool that supports requirement-to-test linking.

## Good habits for test documentation

- **Keep test cases up to date** — When the feature changes, update steps and expected results.
- **Use clear IDs** — Consistent naming (e.g. TC_MODULE_01) makes traceability and reporting easier.
- **Record results as you run** — Log pass/fail and actual result right after execution so you don’t forget.
- **Link bugs to test cases** — When a test fails, link the bug to that test case so you can track "fixed and retested."

Understanding test documentation and traceability helps you work in a structured way and show stakeholders what was tested and how it ties back to requirements.
