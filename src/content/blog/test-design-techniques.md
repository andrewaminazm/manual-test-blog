---
title: Test Design Techniques for Manual Testers
description: Equivalence partitioning, boundary value analysis, decision tables, and state transition — with simple examples you can use every day.
pubDate: 2025-02-12
tags: [test design, techniques, black box]
---

**Test design techniques** help you choose **what** to test so you get good coverage without testing every possible value. Here are the main ones you’ll use as a manual tester.

## Equivalence partitioning

**Idea:** Inputs that are treated the same by the system can be grouped into one **partition**. Test one representative from each partition instead of every value.

**Example:** A field accepts age 18–65.

- Partition 1: Invalid (e.g. 17) → expect error  
- Partition 2: Valid (e.g. 30) → expect accept  
- Partition 3: Invalid (e.g. 66) → expect error  

You pick one value per partition (e.g. 17, 30, 66) instead of testing 18, 19, 20, … 65.

## Boundary value analysis (BVA)

**Idea:** Bugs often appear at **boundaries** (min, max, just below, just above). So test values at and around the limits.

**Example:** Age 18–65.

Test: 17, 18, 19 (around lower boundary) and 64, 65, 66 (around upper boundary).

| Value | Expected |
|-------|----------|
| 17    | Rejected |
| 18    | Accepted |
| 19    | Accepted |
| 64    | Accepted |
| 65    | Accepted |
| 66    | Rejected |

Combining equivalence partitioning and BVA gives strong coverage with few test cases.

## Decision table testing

**Idea:** When behavior depends on several **conditions** (e.g. checkboxes, rules), list all combinations and define expected results in a table. Each row is one test case.

**Example:** Discount rules.

- Condition 1: Is the user a member? (Y/N)  
- Condition 2: Order total ≥ $100? (Y/N)  

| Member? | Order ≥ $100? | Discount    |
|---------|----------------|-------------|
| No      | No             | 0%          |
| No      | Yes            | 5%          |
| Yes     | No             | 10%         |
| Yes     | Yes            | 15%         |

You design one test per row so no combination is missed.

## State transition testing

**Idea:** The system behaves differently in different **states**. You draw states (e.g. Logged out, Logged in, Locked) and transitions (e.g. Login, Logout, Wrong password x3). You then test valid and invalid paths.

**Example:** Login.

- States: Logged out, Logged in, Locked (after 3 failed attempts).  
- Transitions: correct password → Logged in; wrong password → stay Logged out (or move to Locked after 3); Logout → Logged out.

You design tests for: valid login, invalid login, lockout after 3 failures, and unlock (e.g. after 15 minutes or reset).

## Use case / scenario-based testing

**Idea:** Test **end-to-end user scenarios** (user stories or real workflows) instead of only single fields or single actions.

**Example:** "As a customer, I add a product to the cart, apply a coupon, and complete checkout." You run through the full flow with realistic data and check results at each step.

## When to use which

- **Equivalence partitioning + BVA** — Any input with ranges or sets of valid/invalid values (age, amount, quantity).  
- **Decision table** — Business rules with multiple conditions (discounts, eligibility, validation).  
- **State transition** — Workflows with clear states (login, order status, wizard steps).  
- **Scenario-based** — Full user journeys and acceptance criteria.

Using these techniques helps you design fewer, smarter test cases and find more bugs.
