---
title: How to Write a Bug Report That Gets Fixed
description: Structure and tips for clear, actionable bug reports. What to include and how to write steps and expected vs actual results.
pubDate: 2025-02-14
tags: [bugs, reporting, basics]
---

A good **bug report** helps developers reproduce and fix the issue quickly. Vague or incomplete reports slow everyone down. Here’s how to write one that works.

## What to include in a bug report

1. **Title / Summary** — One short sentence describing the problem.
2. **Environment** — OS, browser/device, app version, and any relevant settings.
3. **Steps to reproduce** — Numbered list of actions that lead to the bug.
4. **Expected result** — What should happen according to requirements or common sense.
5. **Actual result** — What actually happened (including error messages or screenshots).
6. **Severity / Priority** — How bad is it? How soon should it be fixed?
7. **Attachments** — Screenshots, screen recordings, or logs if they help.

## Example of a good bug report

**Title:** Login fails with valid credentials when "Remember me" is checked

**Environment:** Windows 11, Chrome 120, app version 2.1.0

**Steps to reproduce:**
1. Open the login page.
2. Enter valid username `testuser` and password `Test@123`.
3. Check the "Remember me" checkbox.
4. Click "Log in".

**Expected result:** User is logged in and redirected to the dashboard.

**Actual result:** Page shows "Invalid credentials" and user is not logged in. Same credentials work when "Remember me" is unchecked.

**Severity:** High (blocks users who use "Remember me").

**Attachment:** [Screenshot of error message]

## Tips for better bug reports

- **One bug per report** — Don’t mix multiple issues; split them so each can be tracked and fixed separately.
- **Be specific** — "Clicking Save does nothing" is vague; "Clicking Save on Edit Profile leaves form unchanged and shows no message" is better.
- **Neutral tone** — Describe what happens; avoid blaming or judging.
- **Reproducible steps** — If developers can’t reproduce it, they often can’t fix it. Include exact data (e.g. which user, which item) if it matters.
- **Use severity and priority** — Severity = impact (e.g. crash vs typo). Priority = when to fix (e.g. before release vs next sprint). Your team may have definitions for these.

## Severity in a nutshell

- **Critical** — System down, data loss, or major feature completely broken.
- **Major** — Important feature broken or workaround is difficult.
- **Minor** — Small error, cosmetic issue, or easy workaround.
- **Trivial** — Typo, tiny UI glitch, no real impact.

Writing clear bug reports is one of the most important skills for a manual tester. Good reports build trust with developers and get issues fixed faster.
