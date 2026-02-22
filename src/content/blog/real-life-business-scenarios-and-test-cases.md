---
title: Real-Life Business Scenarios and Test Cases
description: "Practical examples — e-commerce checkout, login and registration, fund transfer, and order returns with full test cases you can use or adapt."
pubDate: 2025-01-04
tags: [test cases, scenarios, e-commerce, banking, real life]
---

Real-life **business scenarios** are end-to-end flows that users actually perform. Designing **test cases** from these scenarios is how you verify that the system supports the business. Below are four common scenarios with **concrete test cases** you can use as templates or adapt to your project.

---

## Scenario 1: E-commerce — Add to Cart and Checkout

**Business flow:** Customer browses products, adds items to cart, applies a coupon (optional), and completes checkout with payment.

**Actors:** Customer (guest or logged-in), Payment gateway.

### Test cases

**TC_EC_01 — Add single item to cart (logged-in user)**

| Field | Value |
|-------|--------|
| **ID** | TC_EC_01 |
| **Title** | Logged-in user can add one product to cart and see updated count |
| **Preconditions** | User is logged in; product "Wireless Mouse" (SKU: WM-001) is in stock, qty ≥ 1. |
| **Steps** | 1. Open product page for "Wireless Mouse".<br>2. Set quantity to 1.<br>3. Click "Add to Cart".<br>4. Open cart (icon or Cart page). |
| **Test data** | User: customer@test.com; Product: WM-001, Qty: 1. |
| **Expected result** | Cart shows 1 item "Wireless Mouse", qty 1; cart icon shows count 1; unit price and subtotal are correct. |

---

**TC_EC_02 — Add quantity more than available stock**

| Field | Value |
|-------|--------|
| **ID** | TC_EC_02 |
| **Title** | System prevents adding quantity greater than available stock |
| **Preconditions** | Product "Wireless Mouse" has available stock = 2. User on product page. |
| **Steps** | 1. Set quantity to 5.<br>2. Click "Add to Cart". |
| **Test data** | Product: WM-001, Stock: 2, Entered qty: 5. |
| **Expected result** | Message like "Only 2 available" or quantity is capped at 2; user cannot add 5. Cart shows max 2. |

---

**TC_EC_03 — Checkout with valid coupon**

| Field | Value |
|-------|--------|
| **ID** | TC_EC_03 |
| **Title** | Valid discount coupon reduces order total at checkout |
| **Preconditions** | Cart has 2 items; subtotal $100. Coupon "SAVE10" exists, 10% off, not expired. |
| **Steps** | 1. Go to Checkout.<br>2. Enter coupon code "SAVE10".<br>3. Click "Apply".<br>4. Proceed to payment summary. |
| **Test data** | Coupon: SAVE10, 10%; Subtotal: $100. |
| **Expected result** | Coupon applied; discount $10 shown; order total = $90. Summary shows discount line. |

---

**TC_EC_04 — Guest checkout with required fields validation**

| Field | Value |
|-------|--------|
| **ID** | TC_EC_04 |
| **Title** | Guest checkout validates required fields and shows clear errors |
| **Preconditions** | User is not logged in; cart has at least one item. On checkout page. |
| **Steps** | 1. Leave Email empty.<br>2. Fill valid Shipping address.<br>3. Click "Place Order" (or "Continue to Payment"). |
| **Test data** | Email: (empty); Address: valid. |
| **Expected result** | Order is not placed; error message near Email (e.g. "Email is required"); focus on Email field; no payment charged. |

---

---

## Scenario 2: User Login and Registration

**Business flow:** New user registers; existing user logs in; system handles invalid credentials and account lockout.

**Actors:** User, System.

### Test cases

**TC_LOGIN_01 — Successful login with valid credentials**

| Field | Value |
|-------|--------|
| **ID** | TC_LOGIN_01 |
| **Title** | User logs in successfully with correct email and password |
| **Preconditions** | Account exists: user@example.com / Test@123; account not locked. |
| **Steps** | 1. Open Login page.<br>2. Enter email: user@example.com.<br>3. Enter password: Test@123.<br>4. Click "Log in". |
| **Test data** | user@example.com, Test@123. |
| **Expected result** | User is logged in; redirected to dashboard or home; user name/avatar visible; session persists until logout. |

---

**TC_LOGIN_02 — Login fails with wrong password; error message shown**

| Field | Value |
|-------|--------|
| **ID** | TC_LOGIN_02 |
| **Title** | Invalid password shows generic error and does not reveal if email exists |
| **Preconditions** | Account user@example.com exists. |
| **Steps** | 1. Open Login page.<br>2. Enter email: user@example.com.<br>3. Enter password: WrongPass1.<br>4. Click "Log in". |
| **Test data** | user@example.com, WrongPass1. |
| **Expected result** | Login fails; message like "Invalid email or password" (no "email not found" or "wrong password" alone). No redirect; user stays on login page. |

---

**TC_LOGIN_03 — Account locked after N failed attempts**

| Field | Value |
|-------|--------|
| **ID** | TC_LOGIN_03 |
| **Title** | Account locked after 5 failed login attempts; user informed and lockout duration applied |
| **Preconditions** | Account user@example.com exists; lockout policy: 5 attempts, lock 15 minutes. |
| **Steps** | 1. On Login page, enter user@example.com and wrong password.<br>2. Click "Log in". Repeat 5 times (total 5 failed attempts).<br>3. On 6th attempt enter correct password and submit. |
| **Test data** | user@example.com; wrong password x5; then correct password. |
| **Expected result** | After 5th failure, message e.g. "Account locked. Try again after 15 minutes." 6th attempt (even with correct password) fails with same lock message. After 15 min, correct password works. |

---

**TC_REG_01 — New user registration with valid data**

| Field | Value |
|-------|--------|
| **ID** | TC_REG_01 |
| **Title** | New user can register with valid email, password, and required fields |
| **Preconditions** | Registration page available; email not already registered. |
| **Steps** | 1. Open Registration page.<br>2. Enter Email: newuser@test.com.<br>3. Enter Password: Test@123 (meets policy).<br>4. Enter Confirm password: Test@123.<br>5. Enter Name: Test User.<br>6. Accept terms (if checkbox).<br>7. Click "Register". |
| **Test data** | newuser@test.com, Test@123, Test User. |
| **Expected result** | Account created; message "Registration successful" or redirect to login/dashboard; user can log in with new credentials. |

---

**TC_REG_02 — Registration rejects duplicate email**

| Field | Value |
|-------|--------|
| **ID** | TC_REG_02 |
| **Title** | Duplicate email shows error and does not overwrite existing account |
| **Preconditions** | user@example.com already registered. |
| **Steps** | 1. Open Registration page.<br>2. Enter Email: user@example.com and other valid details.<br>3. Click "Register". |
| **Test data** | user@example.com (existing), other fields valid. |
| **Expected result** | Registration fails; message e.g. "Email already registered"; no new account; existing account unchanged. |

---

---

## Scenario 3: Online Banking — Fund Transfer

**Business flow:** Logged-in user transfers money from own account to another account (own or beneficiary); system validates balance, limits, and shows confirmation.

**Actors:** Customer, System.

### Test cases

**TC_FT_01 — Successful transfer within limit to saved beneficiary**

| Field | Value |
|-------|--------|
| **ID** | TC_FT_01 |
| **Title** | User completes transfer to saved beneficiary within daily limit |
| **Preconditions** | User logged in; balance ≥ $500; beneficiary "John Doe" saved, account valid; daily transfer limit $2000; no prior transfers today. |
| **Steps** | 1. Go to Transfer / Send Money.<br>2. Select "To saved beneficiary" → John Doe.<br>3. Enter Amount: 500.<br>4. Enter optional Reference: "Rent".<br>5. Confirm and submit (e.g. OTP if required). |
| **Test data** | From: User account; To: John Doe; Amount: 500; Balance before: 5000. |
| **Expected result** | Success message; transaction ID shown; balance reduced by 500; transaction appears in history; beneficiary receives 500. |

---

**TC_FT_02 — Transfer rejected when amount exceeds balance**

| Field | Value |
|-------|--------|
| **ID** | TC_FT_02 |
| **Title** | Transfer fails when amount is greater than available balance |
| **Preconditions** | User logged in; available balance $200. |
| **Steps** | 1. Go to Transfer.<br>2. Select beneficiary and enter Amount: 500.<br>3. Submit transfer. |
| **Test data** | Balance: 200; Amount: 500. |
| **Expected result** | Transfer rejected; message e.g. "Insufficient balance"; no debit; balance remains 200; no transaction in history. |

---

**TC_FT_03 — Transfer rejected when exceeding daily limit**

| Field | Value |
|-------|--------|
| **ID** | TC_FT_03 |
| **Title** | System blocks transfer that would exceed daily limit |
| **Preconditions** | Daily limit $2000; user already transferred $1800 today; balance ≥ 500. |
| **Steps** | 1. Go to Transfer.<br>2. Enter Amount: 500 (remaining limit would be 200).<br>3. Submit. |
| **Test data** | Already transferred today: 1800; Limit: 2000; New amount: 500. |
| **Expected result** | Transfer rejected; message e.g. "Daily limit exceeded" or "You can transfer up to $200 more today"; no debit. |

---

---

## Scenario 4: Order Management — Return Request

**Business flow:** Customer requests return for an order (or item); system validates eligibility (e.g. within 30 days, item in returnable state) and creates return request; refund processed per policy.

**Actors:** Customer, Support/System.

### Test cases

**TC_RET_01 — Eligible item: return request created and status visible**

| Field | Value |
|-------|--------|
| **ID** | TC_RET_01 |
| **Title** | Customer can submit return request for eligible order within return window |
| **Preconditions** | Order #ORD-1001 delivered 5 days ago; return policy 30 days; item not "non-returnable". User logged in. |
| **Steps** | 1. Go to My Orders.<br>2. Open order #ORD-1001.<br>3. Click "Return" (or "Request return") for the item.<br>4. Select reason: "Changed mind".<br>5. Submit return request. |
| **Test data** | Order: ORD-1001; Delivered: 5 days ago; Reason: Changed mind. |
| **Expected result** | Return request created; confirmation with return ID; order/return history shows "Return requested" or "Pending approval"; user can see return status. |

---

**TC_RET_02 — Return rejected when outside return window**

| Field | Value |
|-------|--------|
| **ID** | TC_RET_02 |
| **Title** | Return request rejected for order outside 30-day return window |
| **Preconditions** | Order #ORD-1002 delivered 35 days ago; return policy 30 days. |
| **Steps** | 1. Go to My Orders.<br>2. Open order #ORD-1002.<br>3. Look for "Return" or "Request return". |
| **Test data** | Order: ORD-1002; Delivered: 35 days ago. |
| **Expected result** | "Return" option not available or disabled; or if user tries, message "Return window expired" (e.g. after 30 days). No return request created. |

---

**TC_RET_03 — Partial return: one item returned, rest of order unchanged**

| Field | Value |
|-------|--------|
| **ID** | TC_RET_03 |
| **Title** | Customer returns one item from multi-item order; other items and order status correct |
| **Preconditions** | Order #ORD-1003 has 3 items (A, B, C); all eligible. User requests return for item B only. |
| **Steps** | 1. Open order #ORD-1003.<br>2. Request return for Item B only.<br>3. Submit and complete return (e.g. ship back, approval).<br>4. Check order details and refund. |
| **Test data** | Order: ORD-1003; Items: A, B, C; Return: B only. |
| **Expected result** | Return created only for B; items A and C still "Delivered" or unchanged; partial refund for B only; order shows "Partial return" or item-level status. |

---

---

## How to use these in real projects

1. **Copy and adapt** — Replace data (emails, IDs, amounts, limits) with your app’s rules and test data.
2. **Trace to requirements** — Map each TC to a requirement ID (e.g. BR-004 → TC_EC_01, TC_EC_02) for traceability.
3. **Add edge cases** — Same scenarios can be extended (e.g. checkout with multiple coupons, transfer to invalid account, return already refunded).
4. **Prioritize** — Mark P0/P1 for business-critical paths (e.g. login, payment, transfer) and run those first in regression.

Using real-life business scenarios like these keeps your test cases aligned with what users and the business actually do, and gives you ready-made examples for interviews or test design discussions.
