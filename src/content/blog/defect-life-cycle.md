---
title: Defect Life Cycle (Bug Life Cycle)
description: From New to Closed — the states a bug goes through and what each status means for testers and developers.
pubDate: 2025-02-05
tags: [bugs, process, defect]
---

When you log a bug, it goes through several **states** until it’s fixed and verified. That flow is the **defect (or bug) life cycle**. Understanding it helps you use your bug-tracking tool correctly and communicate with the team.

## Common defect states

**New** — The bug is reported (by you or someone else) and not yet reviewed.

**Assigned** — A developer (or owner) is assigned to fix it.

**Open / In progress** — The developer is working on the fix.

**Fixed / Resolved** — The developer has implemented a fix and marks it resolved. The bug is ready for **retest**.

**Retest** — You (the tester) verify the fix. You run the same steps and check if the issue is gone.

**Reopened** — The bug still occurs after the fix (or a new issue appeared). You reopen it and assign back to dev. It goes through Open → Fixed → Retest again.

**Closed** — The bug is verified as fixed (or decided as duplicate, won’t fix, etc.) and no further action is needed.

**Deferred / Postponed** — The team decides to fix it in a later release. It’s not fixed now but is acknowledged.

**Won’t fix / Not a bug** — After review, the team decides it’s not a defect (e.g. by design) or not worth fixing. Often then closed.

**Duplicate** — The same issue was already reported. The duplicate is closed and linked to the original bug.

## Simple flow (typical path)

```
New → Assigned → Open → Fixed → [Tester: Retest]
                                    ↓
                    Pass → Closed   OR   Fail → Reopened → Open → ...
```

## What you do as a tester

1. **Report** — Log the bug with clear steps and set status to **New** (or as per your tool).
2. **Retest** — When status is **Fixed**, run the same steps in the same environment. If the issue is gone and no new problem appears, set to **Closed**. If it still fails (or something else broke), set to **Reopened** and add a comment.
3. **Avoid reopening without retest** — Only reopen when you’ve actually retested and the bug still exists (or a regression appeared). Add the build/environment and result of retest in the comment.

Different companies may use slightly different status names (e.g. "In progress" vs "Open", "Verified" vs "Closed"). The idea is the same: New → Assigned → Work → Fixed → Retest → Closed or Reopened. Knowing the defect life cycle keeps your bug list accurate and helps the team track progress.
