---
title: Static Testing — Reviews and Static Analysis (ISTQB)
description: What static testing is, types of reviews (walkthrough, inspection, etc.), and static analysis — no code execution.
pubDate: 2025-01-22
tags: [ISTQB, static testing, reviews]
---

**Static testing** means examining work products **without executing** the code or the system. You find defects in documents (requirements, design, test cases) or in code by **reading and analyzing** them. It’s a big part of the ISTQB syllabus and of real projects.

## Why static testing?

- **Early defect finding** — Problems in requirements or design are cheaper to fix before coding.
- **Fewer defects in code** — Better specs and designs lead to fewer bugs in implementation.
- **Better test basis** — Clear, reviewed requirements make test analysis and design easier.

Static testing is **complementary** to dynamic testing (running the software). You do both.

## Two main types of static testing

1. **Reviews** (of documents and sometimes code) — people check work products.
2. **Static analysis** (of code or models) — tools look for patterns, defects, or violations.

---

## Reviews

A **review** is a formal or informal examination of a work product (e.g. requirements, design, test plan, test cases) to find defects, improve quality, and build shared understanding.

### Types of reviews (ISTQB)

**Informal review** — No formal process. Author asks a colleague to look at the document and give feedback. Low overhead, good for quick checks.

**Walkthrough** — Author leads the meeting and **walks through** the document. Participants ask questions and suggest improvements. Purpose: learning and finding defects. Often no formal roles.

**Technical review** — **Peers** (e.g. devs, testers, architects) examine the document for technical correctness, gaps, and consistency. Led by a moderator. Output: list of findings and recommendations.

**Inspection** — The most **formal** type. Defined roles (author, moderator, reviewer, scribe), entry/exit criteria, and a defined process. Purpose: find defects and improve the document. Often used for critical or regulated work.

**As a manual tester:** You may participate in reviews of requirements (to spot ambiguities and testability issues), design (to see testability and integration points), and test cases (to improve coverage and clarity). Your focus: "Can we test this? Is it clear? What’s missing?"

---

## Static analysis

**Static analysis** is performed **by tools** on source code (or sometimes models), without executing the program. Tools look for:

- **Code standards** — Naming, formatting, complexity.
- **Potential defects** — Unreachable code, unused variables, possible null pointer use.
- **Security or safety issues** — Known vulnerable patterns.

**Who uses it:** Usually **developers** (e.g. in CI); testers may see results when investigating quality or when reviewing code for testability.

**Manual testers:** You don’t have to run static analysis yourself, but you should know it exists and that it finds defects without running the software. It supports "test early" by improving code quality before execution-based testing.

---

## What you do as a manual tester

- **Join reviews** of requirements, user stories, or design — look for unclear, missing, or untestable content and suggest improvements.
- **Review test cases** (yours or others’) — check clarity, coverage, and consistency with requirements.
- **Use findings** from static analysis (if shared with the team) to focus testing on risky or complex areas.

Static testing is a core ISTQB topic and a practical way to find defects early and improve the quality of what you test later.
