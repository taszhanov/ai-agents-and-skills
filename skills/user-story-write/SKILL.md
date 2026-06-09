---
name: user-story-write
description: >
  Writes user stories in standard "As a / I want / So that" format, with detailed
  acceptance criteria in Given/When/Then or checklist format. Use when translating
  a business need or feature idea into a story card ready for a sprint backlog.
allowed-tools: Read Write
---

# User Story Writer

You are writing user stories for a business analyst. A user story is a short description of a feature from the perspective of the person who will use it — it captures the who, what, and why without going into technical implementation details.

## What you need before starting

Ask for (if not provided):
1. **The feature or need** — what should the system do?
2. **Who is the user?** — which type of user or role benefits from this?
3. **The business value** — why does this matter? What problem does it solve?

---

## User story format

```
As a [type of user],
I want to [do something / have something available],
So that [I get this benefit / this business outcome is achieved].
```

**Rules:**
- The "As a" part should name a real role, not a system ("As the system" is wrong — the system does not have goals)
- The "I want" part describes the capability from the user's point of view — not the technical solution
- The "So that" part must state a real business benefit — if you cannot explain the benefit, the story is not ready

---

## What to produce

### 1. The user story card

Write the story in the format above. Keep it to 2–3 lines.

### 2. Acceptance criteria

Write 4–8 acceptance criteria. Use one of these formats depending on what fits better:

**Checklist format** (for simpler stories):
- [ ] The user can do X
- [ ] The system displays Y when Z happens
- [ ] Error message is shown if the input is invalid

**Given/When/Then format** (for stories with clear flows):
- Given [precondition], When [action], Then [expected outcome]

### 3. Definition of Done

A short list of what "done" means for this story — not just functionality but also quality:
- [ ] Feature works as described in all acceptance criteria
- [ ] Edge cases and error states are handled
- [ ] Tested on [relevant environments/browsers/devices if applicable]
- [ ] Reviewed and signed off by [role]

### 4. Story size hint (optional)

Give a rough effort estimate using T-shirt sizing: XS, S, M, L, XL — and a one-sentence reason.

---

## Example output

**User Story:**
```
As a registered customer,
I want to reset my password using my email address,
So that I can regain access to my account if I forget my password.
```

**Acceptance Criteria:**
- Given the user is on the login page, When they click "Forgot Password", Then they are taken to a password reset form
- Given a valid email address is entered, When the form is submitted, Then a reset link is sent to that email within 2 minutes
- Given an email address not in the system is entered, When submitted, Then the message "If this email exists, a reset link has been sent" is shown (do not confirm whether the email exists — security requirement)
- Given the reset link is clicked, When the new password is set, Then the old password no longer works and the user is logged in automatically

**Definition of Done:**
- [ ] All acceptance criteria pass in QA
- [ ] Tested with valid email, invalid email, and expired link
- [ ] Signed off by Product Owner

**Size:** M — standard auth flow, no third-party integrations involved
