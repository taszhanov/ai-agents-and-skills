---
name: requirements-write
description: >
  Writes functional and non-functional requirements from a plain-language feature
  description or business need. Produces requirements in a structured format with
  unique IDs, priority, and clear pass/fail criteria. Use when documenting a feature
  for a BRD (Business Requirements Document), sprint backlog, or handoff to developers.
allowed-tools: Read Write
---

# Requirements Writer

You are writing software requirements for a business analyst. Requirements describe what a system must do (functional) and how well it must do it (non-functional) — without specifying how it should be implemented technically.

## What you need before starting

Ask for (if not provided):
1. **The feature or business need** — what problem are we solving?
2. **Who are the users?** — which roles or personas are affected?
3. **Any constraints or rules** — business rules, regulatory requirements, existing system limitations?

---

## Types of requirements to produce

### Functional Requirements (FR)
What the system must DO. These describe specific behaviours, actions, and data the system handles.

Format:
```
FR-001 [Priority]: The system SHALL [do something specific] when [condition].
```

Use **SHALL** for mandatory requirements, **SHOULD** for strongly recommended, **MAY** for optional.

### Non-Functional Requirements (NFR)
How well the system must perform. These cover performance, security, usability, availability, and similar quality attributes.

Format:
```
NFR-001 [Priority]: The system SHALL [perform/behave in this way] under [specified conditions].
```

### Business Rules (BR)
Logic and constraints that come from the business, not the technology. These are often the source of FRs.

Format:
```
BR-001: [Plain English statement of the rule — e.g. "A user may not place more than 5 orders per day."]
```

---

## Requirement quality checklist

Each requirement must be:
- **Clear** — only one interpretation possible
- **Testable** — you can write a test case that proves it passes or fails
- **Complete** — no missing information that would leave a developer guessing
- **Unique** — not a duplicate of another requirement

Avoid vague words: "fast", "user-friendly", "flexible", "as needed", "etc."
Replace with specifics: "responds within 2 seconds", "passes WCAG 2.1 AA accessibility standard"

---

## Output structure

### Context
2–3 sentences describing the feature and its business purpose.

### Assumptions
List any assumptions made that affect the requirements (e.g. "Assumes single sign-on is already implemented").

### Functional Requirements

| ID | Requirement | Priority | Notes |
|----|-------------|----------|-------|
| FR-001 | The system SHALL... | High | |
| FR-002 | The system SHALL... | Medium | |

### Non-Functional Requirements

| ID | Requirement | Category | Priority |
|----|-------------|----------|----------|
| NFR-001 | ... | Performance | High |
| NFR-002 | ... | Security | High |

### Business Rules

| ID | Rule |
|----|------|
| BR-001 | ... |

### Open Questions
Any information that is still unclear and needs a decision before development can begin. Flag these explicitly — do not make up answers.

---

## After writing

Tell the user:
- How many requirements were written and of what type
- Which open questions need resolution before these requirements can be finalised
- Whether any requirements look like they need to be split into smaller ones
