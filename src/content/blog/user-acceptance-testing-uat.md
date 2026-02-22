---
title: User Acceptance Testing (UAT) — What It Is and Your Role
description: When and how UAT is done, who runs it, and how manual testers support and prepare for it.
pubDate: 2025-02-04
tags: [UAT, types, process]
---

**User Acceptance Testing (UAT)** is the phase where the product is tested to confirm it meets **business needs** and is **acceptable for release**. It’s usually done by or with the people who will use the system (business users, product owners, or customers), not only by the QA team. As a manual tester, you often **prepare** and **support** UAT.

## What is UAT?

- **Goal:** Validate that the system solves the real business problem and is ready for production use.
- **Focus:** Real-world scenarios, correct business rules, and "would we go live with this?"
- **Who runs it:** Typically business users, product owners, or key customers — not only QA.
- **When:** After system testing (functional, regression) is in a good state; often in a dedicated UAT environment that looks like production.

## UAT vs system / functional testing

| System / functional testing | UAT |
|-----------------------------|-----|
| "Does it meet the spec?"    | "Does it meet our business needs?" |
| Done by testers / QA         | Done by business users (with QA support) |
| Detailed test cases, edge cases | Real-life scenarios, workflows |
| Technical correctness        | Fitness for use, acceptance for release |

Both matter. QA ensures the product works as specified; UAT ensures it’s acceptable for the business.

## What manual testers do in UAT

**Before UAT**

- **Prepare UAT scenarios** — Turn business workflows into step-by-step scenarios (e.g. "Place an order as a retail customer and apply a discount").
- **Set up UAT environment** — Ensure the right build, data (e.g. test customers, products), and access for UAT users.
- **Prepare data and logins** — Provide test accounts and any instructions (e.g. "Use this customer for scenario 2").
- **Document how to log issues** — How to report bugs (tool, template, whom to assign).

**During UAT**

- **Support users** — Answer "How do I…?" and help with access or environment issues. You don’t run their tests for them; you unblock them.
- **Triage and clarify** — When they report something, help confirm if it’s a bug, a misunderstanding, or a change request. You might reproduce and log proper bug reports.
- **Track progress** — Note which scenarios are done, passed, or blocked, and help with retesting after fixes.

**After UAT**

- **Summarize results** — How many scenarios passed/failed, main issues found, and whether the product is accepted for release.
- **Hand over defects** — Ensure all UAT bugs are in the defect tracker with clear steps and severity.

## UAT success tips

- **Clear scenarios** — Write UAT scenarios in business language (no jargon), with expected outcome so users know when they’re done.
- **Stable build** — Don’t start UAT on a broken or changing build. Run smoke and critical regression first.
- **Realistic data** — Use data that mirrors production (e.g. real product names, realistic orders) so users can relate.
- **Sign-off** — Define who can sign off UAT (e.g. product owner) and what "accepted" means (e.g. all critical scenarios pass, no critical bugs open).

Understanding UAT helps you work with business users and prepare the right kind of tests and environment so the product gets a fair, clear acceptance check before go-live.
