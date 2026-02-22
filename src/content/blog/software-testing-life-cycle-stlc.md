---
title: Software Testing Life Cycle (STLC) Explained
description: The phases of STLC from requirement analysis to test closure — and what manual testers do in each phase.
pubDate: 2025-02-08
tags: [STLC, process, basics]
---

The **Software Testing Life Cycle (STLC)** is the set of phases that testing goes through in a project. As a manual tester, you’ll take part in most of them. Here’s a simple breakdown.

## 1. Requirement analysis

**What:** Understand what must be tested. Review requirements, user stories, or specs; identify testable items and clarify ambiguities.

**Tester role:** Read requirements, ask questions in meetings, note what’s testable and what’s missing or unclear. No test cases yet — just understanding.

## 2. Test planning

**What:** Define scope, approach, schedule, resources, and risks. Produce the test plan.

**Tester role:** Test lead usually drives this. You may give input (e.g. effort, risks) and review the plan. You’ll use it later to know what to test and when.

## 3. Test case development / design

**What:** Design and write test cases (and test data) based on requirements and the test plan.

**Tester role:** Write test cases, apply test design techniques (equivalence partitioning, boundaries, etc.), get them reviewed, and store them in a test management tool or doc.

## 4. Test environment setup

**What:** Prepare environments where tests will run (e.g. dev, QA, UAT): install build, configure data, set up access.

**Tester role:** You might verify the environment (e.g. run a smoke test), report configuration issues, or work with dev/ops to get it ready.

## 5. Test execution

**What:** Run test cases, record results (pass/fail), log bugs, and retest after fixes.

**Tester role:** Execute tests, document actual vs expected results, report defects, and retest. This is where most of your day-to-day manual testing happens.

## 6. Test cycle closure / reporting

**What:** Summarize results: how many passed/failed, coverage, open bugs, and whether exit criteria are met. Share the test summary report and lessons learned.

**Tester role:** Update status of test cases, contribute to the report, and participate in closure meetings. You might also hand over to UAT or sign off for release.

## STLC in one view

| Phase                 | Main output              | Your focus as tester        |
|-----------------------|--------------------------|-----------------------------|
| Requirement analysis | Clarified requirements    | Understand & clarify         |
| Test planning        | Test plan                | Input & follow the plan     |
| Test case development| Test cases, data         | Write & review cases        |
| Environment setup    | Ready environment        | Verify & smoke              |
| Test execution       | Results, bug reports     | Run tests, log bugs, retest |
| Test closure         | Test summary, sign-off   | Report & lessons learned    |

STLC can be aligned with the development life cycle (e.g. Agile sprints): you analyze stories, plan tests, design cases, then execute and report within the sprint or release. Understanding STLC helps you know what to do at each stage and how testing fits into the project.
