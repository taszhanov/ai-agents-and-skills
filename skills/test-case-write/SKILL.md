---
name: test-case-write
description: >
  Writes structured test cases from a feature description, user story, or requirements.
  Produces test cases in a standard table format with ID, title, preconditions, steps,
  expected result, and priority. Use when preparing a test plan for QA or for sign-off
  documentation.
allowed-tools: Read Write
---

# Test Case Writer

You are writing structured test cases for a business analyst. A test case is a documented procedure that verifies a specific piece of functionality works as expected.

## What you need before starting

Ask for (if not provided):
1. **Feature or requirement** — what needs to be tested?
2. **Scope** — which part of the system? (e.g. login page, checkout flow, API endpoint)
3. **Test type** — functional (does it work?), negative (does it fail correctly?), boundary (edge values?), or all three?

---

## Test case format

Produce each test case using this structure:

---

**TC-001 — [Short descriptive title]**

| Field | Value |
|-------|-------|
| **Priority** | High / Medium / Low |
| **Type** | Positive / Negative / Boundary / Edge Case |
| **Preconditions** | What must be true before the test starts |
| **Test Data** | Specific values to use during the test |

**Steps:**
1. Step one — what to do
2. Step two — what to do next
3. ...

**Expected Result:**
> What should happen if the feature is working correctly. Be specific — name exact messages, states, redirects, or data changes.

**Actual Result:** _(leave blank — filled in during test execution)_

**Status:** Not Run / Pass / Fail

---

## Coverage to aim for

For any feature, produce test cases covering:
- **Happy path** — the normal successful flow (1–2 cases)
- **Negative / invalid input** — wrong data, missing required fields, invalid formats (2–3 cases)
- **Boundary values** — minimum and maximum allowed values if relevant (1–2 cases)
- **Permission / access control** — what happens if the wrong user type tries the action (1 case)
- **State-based cases** — e.g. what if the action is taken twice, or on an already-processed item (1 case)

## Priority rules

- **High** — core business flow; if this fails, the feature is unusable
- **Medium** — important but not a blocker; impacts some users or scenarios
- **Low** — edge case, cosmetic, or rarely encountered

---

## After writing the test cases

Add a short summary:
- Total number of test cases written
- Coverage breakdown (how many positive, negative, boundary)
- Any scenarios that could not be written due to missing information — flag these clearly
