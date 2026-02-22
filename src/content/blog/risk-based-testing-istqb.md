---
title: Risk-Based Testing (ISTQB)
description: How to prioritize testing using risk — product and project risks, risk analysis, and focusing effort where it matters most.
pubDate: 2025-01-18
tags: [ISTQB, risk, test management]
---

**Risk-based testing** means you **prioritize** what to test (and how much) based on **risk**. You focus more effort on high-risk areas and less on low-risk ones, so you use limited time and resources where they matter most. It’s a core idea in **ISTQB** test management.

## What is risk (in testing)?

**Risk** = possibility of something going wrong and the impact if it does.

In testing we often think about:

- **Product risk** — Something in the product could fail or not meet needs (e.g. payment bug, data loss, wrong calculation). Testing aims to reduce product risk by finding defects.
- **Project risk** — Something in the project could prevent testing or delivery (e.g. late requirements, unstable environment, key person leaving). These affect how we plan and execute tests.

Risk-based testing is mainly about **product risk**: we test the riskiest areas first and most.

---

## Why risk-based testing?

- **Limited time** — We can’t test everything; we need to choose.
- **Better use of effort** — More tests on critical features and likely failures; fewer on low-impact, low-likelihood areas.
- **Clear decisions** — When we say "we focused on high-risk areas," we can explain and justify our testing.

---

## How to do risk-based testing (in practice)

### 1. Identify product risks

Ask: "What could go wrong? What would hurt the user or business most?"

Examples: wrong payment amount, login failure, data loss, security breach, core feature broken, poor performance on critical path. You can get input from business, product, dev, and testers.

### 2. Assess likelihood and impact

For each risk (or area):

- **Likelihood** — How likely is a defect here? (e.g. new code, complex logic, many integrations → higher.)
- **Impact** — If it fails, how bad? (e.g. money, safety, reputation, number of users affected.)

You can use simple scales (e.g. 1–3 or Low/Medium/High) for both.

### 3. Prioritize tests

- **High risk** (high likelihood and/or high impact) → test first, more test cases, more techniques (e.g. boundaries, negative cases), maybe more regression.
- **Medium risk** → normal effort.
- **Low risk** → fewer tests, smoke or sanity may be enough.

So your test plan and test case selection are **driven by risk**, not only by "we have 100 requirements."

### 4. Re-assess when things change

Risks change when requirements, design, or code change. Revisit risks when you get new information (e.g. after a major change or incident).

---

## Risk and test process (ISTQB)

- **Test planning** — Risk analysis feeds into scope, approach, and what we test first.
- **Test design** — We design more (and more thorough) tests for high-risk areas.
- **Test execution** — We run high-risk tests first; if time runs out, we’ve at least covered the most important parts.
- **Test monitoring** — We report coverage and results **by risk** (e.g. "All high-risk areas tested; 2 medium-risk areas not yet covered").

---

## What you do as a manual tester

- **Participate in risk discussion** — Suggest areas that are complex, often changed, or critical to users.
- **Prioritize your test cases** — Tag or order by risk (e.g. P0/P1 for high risk) and run high-risk tests first.
- **Report by risk** — In status or summary reports, mention risk coverage (e.g. "High-risk areas: 100% executed; 2 failures in payment.")

Risk-based testing doesn’t mean "only test risky things" — it means **focus more where risk is higher**. That’s how ISTQB expects you to use limited test effort and how many teams operate in practice.
