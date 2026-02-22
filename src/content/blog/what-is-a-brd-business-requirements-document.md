---
title: What Is a BRD (Business Requirements Document)?
description: Purpose of a BRD, typical sections, who writes it, and how it fits into the project and testing.
pubDate: 2025-01-06
tags: [BRD, requirements, documentation]
---

A **BRD (Business Requirements Document)** is a document that describes **what** the business needs from a project or product — the goals, scope, and high-level requirements from a **business** perspective. As a manual tester, you’ll often use the BRD (or derived specs) as a **test basis** to design tests. Here’s what a BRD is and what it usually contains.

## Purpose of a BRD

- **Align stakeholders** — Business, product, and delivery agree on *what* we’re building and *why*.
- **Define scope** — What is in scope and what is out of scope for the project or release.
- **Serve as a foundation** — Other documents (functional specs, user stories, acceptance criteria) are derived from or trace back to the BRD.
- **Support testing** — Testers use it (directly or via downstream docs) to understand what to test and to analyze requirements for testability.

The BRD is usually written **before** or **early** in development; it’s not a technical design document.

---

## Who typically creates a BRD?

- **Business analysts (BA)** — Most common.
- **Product owners** or **product managers** — Especially in Agile.
- **Project sponsors** or **business stakeholders** — With input from BAs or product.

Testers **don’t usually write** the BRD, but they **read and analyze** it (and documents derived from it) to do test analysis and design.

---

## Typical sections of a BRD

Structure varies by organization; below is a common pattern.

**1. Introduction / Overview**
- Purpose of the document and the project.
- Target audience (e.g. business, development, testing).

**2. Business objectives / goals**
- Why we’re doing this (e.g. increase sales, reduce errors, comply with regulation).
- Success criteria from a business perspective.

**3. Scope**
- **In scope** — Features, processes, or user groups included.
- **Out of scope** — Explicitly excluded (so there’s no doubt later).
- **Assumptions** — What we assume to be true (e.g. “Users have internet access”).
- **Constraints** — Limits (e.g. budget, time, technology).

**4. Stakeholders**
- Who is affected (users, departments, customers, partners).
- Who has authority to approve or sign off.

**5. Business requirements**
- High-level **what** the solution must do, often numbered (e.g. BR-001, BR-002).
- Written in business language, not technical implementation.
- Example: “The system shall allow customers to view order history for the last 24 months.”

**6. Functional areas / processes**
- Breakdown by business process or area (e.g. Order management, User management, Reporting).
- May reference or list requirements per area.

**7. Non-functional needs (high-level)**
- Performance, security, availability, or compliance needs at a high level (e.g. “System must be available 99.9% during business hours”).
- Detailed non-functional requirements are often in a separate document or backlog.

**8. Glossary / definitions**
- Key business terms so everyone uses the same meaning (e.g. “Order” means a customer purchase order, not an internal work order).

**9. References**
- Related documents (e.g. existing BRDs, policies, regulations).

**10. Approvals**
- Who reviewed and approved the BRD and when.

---

## BRD vs other documents

| Document | Focus | Typical author |
|---------|--------|-----------------|
| **BRD** | Business needs, goals, scope, high-level requirements | BA, Product |
| **Functional specification (FS)** / **SRS** | Detailed functional behavior, rules, screens, flows | BA, Tech lead |
| **User stories** | User need + acceptance criteria (often derived from BRD) | Product, BA |
| **Technical design** | How it will be built (architecture, components) | Development |

The BRD sits at the **business** level; testers use it together with functional specs or user stories to understand *what* to test and *why*.

---

## Why testers care about the BRD

- **Test basis** — You derive test conditions and test cases from requirements; the BRD (or requirements traced to it) is part of that basis.
- **Scope** — In-scope vs out-of-scope in the BRD tells you what you’re expected to test and what you’re not.
- **Objectives** — Business goals help you prioritize tests (e.g. focus on revenue-related or compliance-related flows).
- **Traceability** — Linking tests back to BRD requirements (or to items that trace to the BRD) supports coverage and reporting.

Understanding what a BRD is and what it contains is the first step; the next is **how to analyze a BRD** for testing — covered in the follow-up post.
