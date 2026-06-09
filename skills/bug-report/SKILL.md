---
name: bug-report
description: >
  Writes a detailed, structured bug report from a plain-language description of
  what went wrong. Produces a report with steps to reproduce, expected vs actual
  behaviour, severity, and environment details. Use when you need to log a defect
  in a bug tracker (Jira, GitHub Issues, etc.) or share a defect with developers.
allowed-tools: Read Write
---

# Bug Reporter

You are writing a bug report for a business analyst. A good bug report gives a developer everything they need to find, reproduce, and fix the issue — without back-and-forth questions.

## What you need before starting

Ask for (if not provided):
1. **What went wrong** — describe the unexpected behaviour in plain English
2. **Steps to reproduce** — what did you do before the bug appeared?
3. **What you expected to happen** — what should have happened?
4. **Environment** — browser, device, OS, app version, test environment (dev/staging/prod)?
5. **Screenshots or error messages** — paste any error text if available

---

## Bug report format

---

### Bug Title
`[Short, specific description — e.g. "Login button unresponsive when email field is empty"]`

> A good title follows this pattern: **[What broke] + [where] + [under what condition]**
> Bad: "Login doesn't work"
> Good: "Login button does nothing when email field is empty on the login page"

---

### Summary
One paragraph (2–4 sentences) describing the bug in plain English. Who is affected? What is the impact on the user? Is this blocking or intermittent?

---

### Severity & Priority

| Field | Value |
|-------|-------|
| **Severity** | Critical / Major / Minor / Cosmetic |
| **Priority** | High / Medium / Low |
| **Frequency** | Always / Sometimes / Rarely / Once |

**Severity guide:**
- **Critical** — system crash, data loss, security issue, or core feature completely broken
- **Major** — important feature is broken but a workaround exists
- **Minor** — feature partially works or is confusing but does not block the user
- **Cosmetic** — visual or text issue only, no functional impact

---

### Environment

| Field | Value |
|-------|-------|
| **Environment** | Dev / Staging / Production |
| **Browser / Device** | e.g. Chrome 124, Windows 11 |
| **App / Build Version** | e.g. v2.3.1 |
| **User Role** | e.g. Admin, Regular User, Guest |

---

### Steps to Reproduce

1. Go to [specific page or feature]
2. Do [specific action]
3. Do [next action]
4. Observe [what happens]

> Steps must be specific enough that anyone can follow them and see the same bug. Avoid vague steps like "click around the page".

---

### Expected Behaviour
> What should have happened according to the requirements or common sense?

---

### Actual Behaviour
> What actually happened? Include exact error messages, wrong values, or unexpected states.

---

### Attachments
- Screenshot: [describe what the screenshot shows, or paste error text]
- Log output: [paste relevant console errors or server logs if available]

---

### Additional Notes
Any context that might help: recent deployments, related features, only affects certain users/data, etc.

---

## After writing the report

Ask the user:
- "Do you have a screenshot or error message text to add?"
- "Which bug tracker are you using? I can format this for Jira, GitHub Issues, or another system if needed."
