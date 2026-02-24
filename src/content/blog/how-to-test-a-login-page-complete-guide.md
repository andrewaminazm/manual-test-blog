---
title: How to Test a Login Page — Complete Guide with Test Cases
description: Full guide to testing a login page — functional, security, usability, and edge case test cases every tester should know.
pubDate: 2025-01-01
tags: [test cases, login, functional, security]
---

The **login page** is one of the most tested features in any application. It's business-critical, often has complex rules, and is a common target for security issues. Here's a complete guide to testing it thoroughly as a manual tester.

## What makes a login page important?

- It's the **entry point** to the application — if it fails, nothing works.
- It handles **authentication** — wrong behavior can expose user accounts.
- It has many **edge cases**: empty fields, special characters, locked accounts, "remember me," "forgot password," and more.

---

## Functional test cases

**TC_L_01 — Valid login**

| Step | Action | Expected |
|------|--------|---------|
| 1 | Enter valid email and password | Fields accept input |
| 2 | Click Login | Redirect to dashboard; user name visible |

---

**TC_L_02 — Wrong password**

Enter correct email, wrong password → Error: "Invalid email or password." User stays on login page. No redirect.

---

**TC_L_03 — Wrong email**

Enter non-existent email, any password → Same generic error. (No "Email not found" — that reveals valid emails.)

---

**TC_L_04 — Empty email field**

Leave email blank, enter password, click Login → Inline validation: "Email is required." Form not submitted.

---

**TC_L_05 — Empty password field**

Enter email, leave password blank, click Login → "Password is required." Form not submitted.

---

**TC_L_06 — Both fields empty**

Click Login with empty form → Both fields show validation errors. No request sent.

---

**TC_L_07 — Account lockout after failed attempts**

Enter wrong password 5 times (or however many your policy allows) →
- After N failures: "Account locked. Try again after X minutes."
- Even correct password during lock period: still locked.
- After lock expires: correct password works again.

---

**TC_L_08 — Remember me checkbox (if present)**

Check "Remember me," log in, close browser, reopen → Session persists; user is still logged in (or token is valid).

Without "Remember me": close browser → user logged out.

---

**TC_L_09 — Forgot password link**

Click "Forgot password" → Navigates to reset flow; reset email sent to valid address; message doesn't reveal whether email exists.

---

**TC_L_10 — Redirect after login**

If user was redirected to login (e.g. tried to access a protected page) → After successful login, user lands on the originally requested page, not just the dashboard.

---

## Security test cases

**TC_LS_01 — Password is masked**

Type password → Characters are hidden (shown as dots/asterisks). No plain-text exposure in page source or network.

---

**TC_LS_02 — Generic error message**

Whether email is wrong or password is wrong → Same message, e.g. "Invalid email or password." Never say "email not found" or "wrong password" separately. This prevents **user enumeration**.

---

**TC_LS_03 — SQL injection attempt**

Enter `' OR '1'='1` as email or password → Login fails with normal error; app does not crash or expose data. No SQL error visible.

---

**TC_LS_04 — XSS attempt**

Enter `<script>alert('XSS')</script>` in fields → Script does not execute; input is treated as plain text or rejected.

---

**TC_LS_05 — HTTPS / secure transmission**

Inspect browser network tab → Login request is sent over **HTTPS**, not HTTP. Password is not visible in plain text in the request.

---

**TC_LS_06 — No credentials in URL**

After login, URL should not contain email, password, or token in plain text in the query string.

---

**TC_LS_07 — Brute force protection**

After N failed attempts → Rate limiting, CAPTCHA, or lockout kicks in. No unlimited retry.

---

## Usability test cases

**TC_LU_01 — Tab order**

Tab key moves: Email → Password → Login button (logical order, no skipping).

---

**TC_LU_02 — Enter key submits**

Fill email and password → Press Enter → Login submits. No need to click the button.

---

**TC_LU_03 — Visible error placement**

Errors are shown **near the relevant field**, not only at the top or bottom of the page.

---

**TC_LU_04 — Password show/hide toggle (if present)**

Click eye icon → Password becomes visible. Click again → Hidden. Works on both desktop and mobile.

---

**TC_LU_05 — Mobile responsiveness**

On a phone screen: fields are large enough to tap, keyboard does not hide fields, and email keyboard type shows `@`. Password field uses password keyboard.

---

## Edge case test cases

**TC_LE_01 — Long input**

Enter 500-character email and 500-character password → App handles gracefully (rejects or truncates); no crash or unhandled error.

---

**TC_LE_02 — Special characters in password**

Password with `!@#$%^&*()_+-=[]{}` → Login works if the password was set with these characters; app doesn't break.

---

**TC_LE_03 — Spaces in email**

Enter email with leading/trailing spaces (e.g. `" user@example.com "`) → App trims and accepts, or shows clear validation error. Spaces in the middle should be rejected.

---

**TC_LE_04 — Copy-paste credentials**

Copy email and password from a password manager, paste into fields → Login works (paste not blocked).

---

**TC_LE_05 — Concurrent sessions (if applicable)**

Log in on two browsers with the same account → Check policy: are both sessions allowed? Or does the second login log out the first?

---

## Checklist summary

Use this when assigned to test any login page:

- [ ] Valid login works and redirects correctly
- [ ] Invalid credentials show generic error
- [ ] Empty field validation works (each field and both together)
- [ ] Lockout after N failures with clear message
- [ ] "Remember me" / session persistence works per policy
- [ ] "Forgot password" link leads to reset
- [ ] Password is always masked (and toggle works if present)
- [ ] Same error for wrong email vs wrong password (no enumeration)
- [ ] SQL injection and XSS inputs handled safely
- [ ] Form submits via Enter key
- [ ] Tab order is logical
- [ ] Works on mobile (responsive, right keyboard types)
- [ ] HTTPS used; no credentials in URL

A login page test is a great example to show in interviews — it demonstrates functional, security, usability, and edge case thinking all in one feature.
