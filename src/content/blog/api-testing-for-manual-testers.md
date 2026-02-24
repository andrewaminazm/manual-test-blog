---
title: API Testing for Manual Testers (With Postman)
description: How to test REST APIs manually using Postman — requests, status codes, response validation, and practical examples.
pubDate: 2025-01-02
tags: [API testing, Postman, basics]
---

**API testing** means checking that an application's **API** (Application Programming Interface) works as expected — correct responses, right status codes, proper error handling. As a manual tester you don't need to know programming to start; **Postman** makes it straightforward.

## What is an API?

An API is a way for two systems to communicate. In web apps, the **UI** calls a **backend API** that returns data. When you fill in a form and click "Submit," the browser sends an **API request**; the server sends an **API response**.

Manual API testing means sending those requests yourself (without the UI) and verifying the responses.

## Why test APIs?

- **Faster than UI testing** — No waiting for pages to load; you get a direct response.
- **Find backend bugs early** — Some bugs only show in the API, not the UI.
- **Validate data** — Check values returned by the API match what the UI shows.
- **Test edge cases** — Send invalid data directly without the UI preventing it.

## HTTP basics you need to know

**Methods (verbs):**

| Method | Meaning | Example |
|--------|---------|---------|
| GET    | Read data | Get a list of users |
| POST   | Create data | Register a new user |
| PUT    | Update (replace) | Update a user profile |
| PATCH  | Update (partial) | Change only the email |
| DELETE | Delete data | Delete a user |

**Status codes:**

| Code | Meaning |
|------|---------|
| 200 OK | Success |
| 201 Created | Resource created |
| 400 Bad Request | Invalid input |
| 401 Unauthorized | Not logged in |
| 403 Forbidden | Logged in but no permission |
| 404 Not Found | Resource doesn't exist |
| 500 Internal Server Error | Server-side bug |

**Request parts:** URL (endpoint), method, headers (e.g. `Authorization`, `Content-Type`), and body (for POST/PUT/PATCH).

## Getting started with Postman

1. Download and install [Postman](https://www.postman.com/downloads/) (free).
2. Open Postman → click **New → HTTP Request**.
3. Choose method (GET), enter URL, click **Send**.
4. See the response body, status code, and headers.

## Practical example: testing a login API

**Endpoint:** `POST https://api.example.com/auth/login`

**Request body (JSON):**
```json
{
  "email": "user@example.com",
  "password": "Test@123"
}
```

**Headers:**
```
Content-Type: application/json
```

**Expected response (200 OK):**
```json
{
  "token": "eyJhbGciOi...",
  "user": { "id": 1, "email": "user@example.com" }
}
```

**What to verify:**
- Status code is **200**.
- Response contains `token` field.
- `user.email` matches the email you sent.
- No sensitive data (e.g. password) in the response.

## Negative test cases for APIs

Good API testing includes negative cases:

| Test | Input | Expected response |
|------|-------|--------------------|
| Wrong password | Correct email, wrong password | 401 Unauthorized |
| Missing field | No password in body | 400 Bad Request |
| Invalid email format | `notanemail` | 400 Bad Request |
| Non-existent user | Unknown email | 401 or 404 |

## Performance testing in Postman

Postman now includes a **performance testing** feature where you can run a collection of requests under load and see metrics like response time, throughput, and error rate. This is useful for basic load testing without extra tools.

You can find it in Postman under **Collections → Run → Performance** (see [official docs](https://learning.postman.com/docs/collections/performance-testing/performance-test-configuration)).

## What to check in every API test

- **Status code** — Is it correct for the scenario (200, 201, 400, 401, etc.)?
- **Response body** — Does it contain the expected fields and values?
- **Data types** — Is `id` a number, `email` a string, etc.?
- **Error messages** — Are error responses clear and helpful?
- **No sensitive data** — Passwords or tokens should not appear where they shouldn't.
- **Response time** — Is it reasonable (e.g. under 500ms for simple reads)?

API testing is a powerful skill for manual testers. It lets you test faster, deeper, and catch backend issues that UI tests often miss.
