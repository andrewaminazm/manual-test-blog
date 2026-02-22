---
title: Test Levels — Component, Integration, System, Acceptance (ISTQB)
description: "The four test levels from ISTQB — what each level tests, who typically does it, and how they fit together."
pubDate: 2025-01-24
tags: [ISTQB, test levels, integration, system]
---

**Test levels** are stages of testing that correspond to different levels of the system or different stages of delivery. The **ISTQB Foundation** describes four main levels. As a manual tester you’ll mostly work at **integration**, **system**, and **acceptance**; understanding all four helps you see where your work fits.

## 1. Component testing (unit testing)

**What:** Testing individual **components** (modules, units, classes) in isolation, often with stubs or mocks for dependencies.

**Who:** Usually **developers** (sometimes with testers supporting or reviewing).

**Focus:** Correctness of the component’s behavior in isolation — logic, boundaries, error handling.

**Manual testers:** You may rarely run component tests yourself; they’re often automated. You should know they exist and that they run early, before integration.

---

## 2. Integration testing

**What:** Testing how **components or systems work together** — interfaces, data flow, and interaction between modules or services.

**Who:** Developers and/or testers.

**Focus:** Interfaces, APIs, data passed between parts, and behavior when several components are combined. Can be "component integration" (multiple components) or "system integration" (multiple systems).

**Manual testers:** You may run integration tests manually (e.g. via UI or API tools), check that data flows correctly between modules, or verify that one system’s output is correctly used by another.

---

## 3. System testing

**What:** Testing the **complete, integrated system** end-to-end as a whole. Usually against the system requirement specification or similar.

**Who:** **Testers** (often independent of the development team).

**Focus:** Functional and non-functional behavior of the whole system: does it meet requirements? Behavior, usability, performance (if in scope), etc. Environment is as close to production as practical.

**Manual testers:** This is where much of your work lives — running functional test cases, regression, smoke, exploratory testing on the full system.

---

## 4. Acceptance testing

**What:** Testing to determine whether the system is **acceptable for delivery** and meets business and user needs. Can be contract or user acceptance.

**Who:** **Business users**, **product owners**, or **customers**, often with **tester support** (you prepare scenarios, environment, and support execution).

**Focus:** Real business scenarios, fitness for use, and "ready for production" from a business perspective. Not only "does it meet the spec?" but "do we accept it?"

**Manual testers:** You prepare UAT scenarios, environment, and data; support users during UAT; and help log and triage issues. (See the UAT post for more.)

---

## How the levels relate

| Level        | Scope              | Typical executor   | Main question                          |
|-------------|--------------------|--------------------|----------------------------------------|
| Component   | Single unit        | Developer          | Does this unit behave correctly?       |
| Integration | Units/systems together | Dev / Tester   | Do they work together correctly?       |
| System      | Whole system       | Tester             | Does the system meet requirements?     |
| Acceptance  | Business use       | Business / User    | Is it acceptable for release?          |

They’re often done in this order, but in Agile they can overlap or repeat per iteration. As a manual tester you’ll mainly work at **system** and **acceptance** level and sometimes **integration**; knowing all four levels helps you align with ISTQB and with how your team talks about testing.
