---
title: How to Write a Test Case (Step-by-Step)
description: Learn how to write clear, reusable test cases. Includes structure, examples, and tips for manual testers.
pubDate: 2025-02-18
tags: [test design, test cases, basics]
---

A **test case** is a set of steps, data, and expected results used to check one specific behavior. Good test cases are clear, repeatable, and easy for anyone on the team to follow.

## Basic structure of a test case

A typical test case includes:

1. **ID** — Unique identifier (e.g. TC_LOGIN_01).
2. **Title / Summary** — Short description of what you’re testing.
3. **Preconditions** — What must be true before you start (e.g. user is logged out, browser is on the login page).
4. **Test steps** — Numbered actions the tester performs.
5. **Test data** — Inputs used (e.g. username `testuser`, password `Test@123`).
6. **Expected result** — What should happen after the steps.
7. **Actual result** — What actually happened (filled during execution).
8. **Status** — Pass / Fail / Blocked.

## Example: Login test case

| Field | Value |
|-------|--------|
| **ID** | TC_LOGIN_01 |
| **Title** | Valid user can log in with correct credentials |
| **Preconditions** | User is on the login page; account `testuser` exists. |
| **Steps** | 1. Enter username: `testuser`<br>2. Enter password: `Test@123`<br>3. Click "Log in" |
| **Expected result** | User is redirected to the dashboard; welcome message is shown. |
| **Actual result** | _(filled when running the test)_ |
| **Status** | _(Pass / Fail / Blocked)_ |

## Tips for writing better test cases

- **One behavior per case** — If you mix multiple checks, failures become hard to interpret.
- **Steps should be repeatable** — Another tester (or you later) should get the same result.
- **Expected result must be specific** — Prefer “Dashboard shows ‘Welcome, testuser’” over “Login works.”
- **Use realistic data** — Avoid “asdf” or “123”; use data that matches rules (e.g. valid email, password policy).

Once you’re comfortable writing cases like this, you can add more (invalid login, empty fields, locked account, etc.) and reuse the same structure for any feature.
