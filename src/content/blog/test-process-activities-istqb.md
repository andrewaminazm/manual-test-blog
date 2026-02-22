---
title: The Test Process — Planning to Completion (ISTQB)
description: "The generic test process from ISTQB — planning, monitoring and control, analysis, design, implementation, execution, and completion."
pubDate: 2025-01-26
tags: [ISTQB, process, test process]
---

The **ISTQB Foundation** describes a **generic test process** with main activities that can apply to any project or level of testing. As a manual tester, you take part in most of them. Here’s a clear overview.

## The test process activities

1. **Test planning**  
2. **Test monitoring and control**  
3. **Test analysis**  
4. **Test design**  
5. **Test implementation**  
6. **Test execution**  
7. **Test completion**

They don’t have to be strictly one-after-another; in Agile they often overlap and repeat in each iteration.

---

## 1. Test planning

**Goal:** Define what to test, how, when, and with what resources.

**Typical tasks:** Define scope and objectives, choose approach (e.g. types of testing, techniques), plan resources and schedule, identify risks, define entry/exit criteria, and decide deliverables (test plan, cases, reports).

**Output:** Test plan (or equivalent).

---

## 2. Test monitoring and control

**Goal:** Check progress against the plan and take action when needed.

**Monitoring:** Measure progress (e.g. tests run vs planned, pass/fail, defects, coverage) and compare to the plan.

**Control:** Take decisions — e.g. re-prioritize, add resources, change scope, or report that exit criteria are not met.

**Output:** Test progress reports, decisions (e.g. "we need one more week"), and possibly updated plan.

---

## 3. Test analysis

**Goal:** Decide **what** to test — identify test conditions from requirements, risks, and other work products.

**Typical tasks:** Analyze requirements, user stories, design, and risks; identify test conditions (testable aspects); and define what "done" looks like for test analysis.

**Output:** Test conditions (e.g. "User can log in with valid credentials", "Invalid password is rejected").

---

## 4. Test design

**Goal:** Turn test conditions into **concrete test cases** and high-level steps.

**Typical tasks:** Design test cases (steps, data, expected results) using test design techniques; prioritize; and identify test data and environment needs.

**Output:** Test cases (or test case specifications), test data needs, environment needs.

---

## 5. Test implementation

**Goal:** Get everything ready to **run** the tests.

**Typical tasks:** Develop and order test cases in detail (steps, data); prepare test data and environment; create test execution schedule; and set up traceability (e.g. requirements ↔ test cases).

**Output:** Ready-to-run test cases, test data, environment, execution schedule.

---

## 6. Test execution

**Goal:** Run the tests, record results, and report defects.

**Typical tasks:** Execute tests, compare actual vs expected, log pass/fail, report defects, re-run tests after fixes (retest), and update traceability.

**Output:** Test execution results, defect reports, test logs.

---

## 7. Test completion

**Goal:** Close the test cycle and capture lessons.

**Typical tasks:** Check that planned deliverables are done; archive test artifacts (cases, data, results); hand over to others if needed (e.g. UAT); write test summary report; and capture lessons learned for next time.

**Output:** Test summary report, archived artifacts, lessons learned.

---

## How this fits with STLC

The ISTQB test process is **generic**; the **STLC** (Software Testing Life Cycle) is one way to map it onto a project (e.g. requirement analysis → planning → design → environment → execution → closure). The ideas match: plan → analyze what to test → design cases → implement and run → complete and report. As a manual tester, you’ll recognize your daily work in these activities and use the same terms in ISTQB-style exams and in the workplace.
