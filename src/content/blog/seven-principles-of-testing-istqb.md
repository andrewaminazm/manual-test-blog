---
title: Seven Principles of Testing (ISTQB)
description: The seven key principles of software testing from ISTQB Foundation — and what they mean for manual testers.
pubDate: 2025-01-28
tags: [ISTQB, fundamentals, principles]
---

The **ISTQB Foundation Level** syllabus defines **seven principles of testing**. They guide how we think about testing and what we can and cannot expect. Here they are in plain language.

## 1. Testing shows the presence of defects, not their absence

Testing can find bugs and reduce the risk of defects remaining — but **passing tests do not prove the software is defect-free**. There may always be undiscovered issues. So we say "we found no critical bugs in this area" rather than "this area has no bugs."

## 2. Exhaustive testing is impossible

You cannot test **every** combination of inputs, data, paths, and environments (except in trivial cases). So we use **risk**, **priority**, and **test techniques** to choose what to test. We focus on important features, likely defects, and techniques like equivalence partitioning and boundary value analysis to get good coverage with limited tests.

## 3. Early testing saves time and cost

Finding and fixing defects **early** (e.g. in requirements or design) is cheaper and faster than finding them in production. So testing activities should start as soon as we have testable work products — **static testing** (reviews) of requirements and design, and **dynamic testing** as soon as code is available. "Test early" is a principle, not only a slogan.

## 4. Defects cluster together

Defects are often **not spread evenly**. A small number of modules or areas often contain most of the bugs (e.g. complex code, often-changed code). As a tester, focus more on risky and complex areas; a few modules may deserve most of your test effort.

## 5. Pesticide paradox

If you **always run the same tests**, you stop finding new bugs in the same place — like using the same pesticide until bugs become resistant. You need to **review and update tests**: add new cases, change data, try new techniques (e.g. exploratory), and adjust when the product or risks change.

## 6. Testing is context-dependent

Testing is done differently depending on **context**: type of system (e.g. medical, e‑commerce, mobile), project (e.g. safety-critical vs internal tool), and constraints (time, budget, regulations). There is no single "right" way to test; approach and rigor depend on the context.

## 7. Absence-of-defects is a fallacy

A system with **no known defects** is not necessarily **ready for use**. It might not meet user needs, be usable, or fit the business. So we test not only for "no bugs" but for **fitness for purpose** — which is why UAT and business acceptance matter.

---

**Summary:** Testing reveals defects but can’t prove their absence; we can’t test everything, so we prioritize; early testing pays off; defects cluster; we must evolve our tests; testing depends on context; and no defects ≠ fit for use. These principles underpin the ISTQB view of testing and help you explain and justify your work as a manual tester.
