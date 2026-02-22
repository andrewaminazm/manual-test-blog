---
title: Test Metrics and When to Stop Testing (ISTQB)
description: What to measure during testing, how to report progress, and how exit criteria help decide when to stop.
pubDate: 2025-01-16
tags: [ISTQB, metrics, test management]
---

**Test metrics** help you see progress, report status, and support decisions. **Exit criteria** define when testing can stop. Both are part of **test monitoring and control** in the ISTQB test process. Here’s a practical view for manual testers.

## Why metrics?

- **Progress** — Are we on track? How many tests run vs planned?
- **Quality** — How many pass/fail? How many defects? Trends?
- **Decisions** — Do we need more time? Can we release? Should we fix more bugs first?

Metrics should be **simple, useful, and agreed** with the team — not collected for the sake of it.

---

## Common test metrics

**Progress**

- **Planned vs executed** — Number (or %) of test cases planned vs run.
- **Test execution rate** — Tests run per day or per sprint.
- **Schedule** — Are we on time? (e.g. "80% of tests run, 2 days left.")

**Results**

- **Pass / fail counts** — How many tests passed, failed, blocked?
- **Pass rate** — e.g. 95% of run tests passed.
- **Defects found** — Total open, by severity, by module; trend over time (e.g. fewer new bugs this week).

**Coverage**

- **Requirements coverage** — % of requirements covered by at least one test case.
- **Test execution coverage** — % of test cases executed (and passed vs failed).
- **Risk coverage** — e.g. "All high-risk areas have been tested."

**Defects**

- **Open defects** — By severity (critical, major, minor).
- **Defect find rate** — Defects found per day or per phase.
- **Defect fix / retest** — How many fixed, how many retested, how many reopened.

You don’t need all of these; pick a few that your project and stakeholders care about (e.g. tests executed, pass rate, critical defects open).

---

## Test reporting

**Test progress report** (during testing) — Short update: tests planned vs run, pass/fail, defects, blockers, and any risks (e.g. "We may not finish regression by Friday").

**Test summary report** (at completion) — What was tested, what was not, results summary, defects summary, and whether **exit criteria** were met. Often used for release or phase sign-off.

As a manual tester you’ll often **fill in** the numbers (from your test runs and defect tool) and contribute to or write these reports.

---

## Exit criteria — when to stop testing

**Exit criteria** are conditions that must be met before we **stop testing** (for this phase or release). They are defined in the **test plan** and checked during **test completion**.

Typical examples:

- **Planned tests executed** — e.g. 100% of planned test cases executed (or agreed subset, e.g. all P0/P1).
- **Pass rate** — e.g. at least 95% of executed tests passed.
- **Critical/high defects** — e.g. no critical defects open; high defects either fixed or accepted with documented justification.
- **Coverage** — e.g. all high-risk areas tested; requirements coverage above X%.
- **Stakeholder agreement** — Test lead or product owner agrees to release (or to hand over to UAT) based on the summary report.

**When we stop:** When the **exit criteria are met** (and we’ve written the test summary report and closed the test cycle). If we stop **without** meeting them (e.g. due to deadline), that’s a **business decision** with accepted risk — it should be explicit, not implicit.

---

## What you do as a manual tester

- **Record results** — Log pass/fail and defects so metrics are accurate.
- **Update progress** — Mark test cases executed, link defects to tests, support your lead with numbers for reports.
- **Report blockers** — If you can’t run tests (environment, build, missing data), say so so that "tests not run" is visible.
- **Respect exit criteria** — Don’t say "testing is done" unless the agreed criteria are met or the business explicitly accepts the risk.

Metrics and exit criteria are how ISTQB ties **test monitoring and control** and **test completion** to real decisions: how we’re doing and when we can stop.
