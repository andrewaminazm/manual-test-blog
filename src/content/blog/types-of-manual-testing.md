---
title: Types of Manual Testing Explained
description: Functional, regression, smoke, UAT, exploratory, and more — when to use each type and what they mean for testers.
pubDate: 2025-02-15
tags: [basics, types, functional, regression, smoke]
---

Manual testing is not one single activity. Depending on **when** you test and **what** you focus on, you’ll use different **types** of testing. Here’s a clear overview.

## Functional testing

**What:** Check that features work as specified (requirements / specs).

**When:** After a feature is built or changed.

**Example:** Login accepts valid credentials and rejects invalid ones; "Add to cart" updates the cart total.

You design test cases from requirements and execute them to verify correct behavior.

## Regression testing

**What:** Re-run existing tests to ensure new or changed code didn’t break existing functionality.

**When:** After every release, hotfix, or major change.

**Example:** After fixing a payment bug, you re-test login, search, checkout, and profile to make sure nothing else broke.

Regression can be manual (run a set of test cases) or automated (run a suite of scripts).

## Smoke testing

**What:** Quick, high-level check that the build is stable enough to test in depth.

**When:** Right after a new build or deployment.

**Example:** Can you open the app? Log in? Reach main screens? If these fail, you don’t proceed to detailed testing.

Smoke is a subset of tests; it’s not full coverage.

## Sanity testing

**What:** Narrow check on one or a few areas after a small change.

**When:** After a bug fix or a very small feature change.

**Example:** You fixed the "Forgot password" flow — sanity is testing only that flow, not the whole app.

Sanity is even narrower than smoke.

## User acceptance testing (UAT)

**What:** Testing by end users (or their representatives) to confirm the system meets business needs and is acceptable for release.

**When:** Near the end of the project, before go-live.

**Example:** Real customers or business analysts run real-life scenarios (e.g. place order, process return) in a UAT environment.

As a tester, you may prepare scenarios and support UAT; execution is often done by business users.

## Exploratory testing

**What:** Simultaneous learning, test design, and execution without pre-written scripts. You explore the product and decide what to try next.

**When:** Anytime — often alongside scripted tests, or when specs are unclear or time is limited.

**Example:** You click around a new feature, try odd inputs, and follow hunches to find issues a script might miss.

Useful for finding edge cases and usability problems.

## Compatibility testing

**What:** Check that the application works across different environments: browsers, devices, OS versions, screen sizes.

**When:** When the product is expected to support multiple platforms.

**Example:** Test the same flow on Chrome, Firefox, Safari, and on mobile vs desktop.

## Usability testing

**What:** Focus on how easy and pleasant the product is to use — navigation, clarity, accessibility, flow.

**When:** During or after feature development; often with real users.

**Example:** Can users find the checkout? Is the error message clear? Is the form too long?

## Summary

| Type            | Goal                                      | When / who                          |
|-----------------|-------------------------------------------|-------------------------------------|
| Functional      | Verify features match requirements        | After feature development           |
| Regression      | Ensure changes didn’t break existing      | After each release / change          |
| Smoke           | Confirm build is testable                 | After each build                     |
| Sanity          | Quick check after small change            | After fix or tiny feature            |
| UAT             | Confirm fit for business / go-live        | Near release; often business users   |
| Exploratory     | Find unexpected issues; learn product     | Anytime; no script                   |
| Compatibility   | Works on target browsers/devices         | When multi-platform support needed   |
| Usability       | Easy and clear to use                     | During/after design and development  |

As a manual tester, you’ll often combine these: e.g. smoke after build, functional for new features, regression before release, and exploratory when you have time to dig deeper.
