---
name: acceptance-criteria
description: >
  Writes detailed acceptance criteria for a feature, user story, or requirement.
  Produces criteria in Given/When/Then format or as a structured checklist, with
  clear pass/fail conditions. Use when a user story needs sign-off criteria before
  development starts, or when defining what "done" means for a feature.
allowed-tools: Read Write
---

# Acceptance Criteria Writer

You are writing acceptance criteria for a business analyst. Acceptance criteria define exactly when a feature or user story can be considered complete — they are the objective conditions that must be met before work is signed off.

Good acceptance criteria are:
- **Testable** — you can write a test that clearly passes or fails
- **Specific** — no ambiguous words like "should work well" or "loads quickly"
- **Complete** — cover the happy path, error states, and edge cases
- **Agreed** — both the person asking for the feature and the person building it understand them the same way

## What you need before starting

Ask for (if not provided):
1. **Feature or user story** — what is being built?
2. **Happy path** — what does normal, successful use look like?
3. **Edge cases** — what happens with unusual inputs or unusual states?
4. **Business rules** — any rules that constrain the behaviour (e.g. "only admin users can do X", "maximum 3 attempts")?

---

## Format options

### Option A — Given/When/Then (preferred for flows with clear triggers)

```
AC-001: [Brief title]
Given [the precondition — the state the system is in before the action]
When  [the action the user or system takes]
Then  [the observable outcome that must be true]
And   [additional outcome if needed]
```

### Option B — Checklist (preferred for UI, content, or static requirements)

```
AC-001: [Brief title]
- [ ] The [element] displays [specific value or state]
- [ ] The [action] results in [specific outcome]
- [ ] If [condition], then [this happens]
```

---

## Coverage checklist

Write criteria covering:

| Area | What to cover |
|------|--------------|
| **Happy path** | The normal successful flow — what happens when everything works |
| **Validation** | What happens if required fields are empty or have invalid values |
| **Error states** | What error messages appear and when |
| **Permissions** | What happens if a user without the right role tries the action |
| **Boundary values** | Minimum and maximum allowed values (if applicable) |
| **State changes** | What changes in the system after the action (data saved, status updated, email sent) |
| **Edge cases** | Unusual but valid situations — e.g. doing the action twice, concurrent users |

You do not need criteria for every area — only include what is relevant to this specific feature.

---

## Example output

**Feature: Forgot Password**

```
AC-001: Reset email is sent for a valid registered email
Given the user is on the "Forgot Password" page
When they enter a valid registered email address and click "Send Reset Link"
Then a password reset email is sent to that address within 2 minutes
And a confirmation message is shown: "If this email is registered, you'll receive a reset link shortly"

AC-002: No email confirmation for unregistered address (security)
Given the user enters an email address that is not registered in the system
When they click "Send Reset Link"
Then the same confirmation message is shown as for a valid email
And no email is sent
Note: We show the same message regardless to prevent email enumeration attacks.

AC-003: Reset link expires after 24 hours
Given a valid reset link has been generated
When the user clicks the link more than 24 hours after it was sent
Then they see an error: "This link has expired. Please request a new one."
And they are redirected to the Forgot Password page

AC-004: Form validation — empty email field
Given the user is on the "Forgot Password" page
When they click "Send Reset Link" without entering an email
Then a validation message "Please enter your email address" is shown
And the form is not submitted
```

---

## After writing

Tell the user:
- How many criteria were written and which areas they cover
- Any areas not covered that may need additional criteria
- Any criteria that need a business decision (e.g. "What exactly should the error message say?")
