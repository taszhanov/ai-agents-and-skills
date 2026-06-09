---
name: stakeholder-summary
description: >
  Writes a clear, non-technical stakeholder summary or executive update from
  technical notes, meeting outputs, sprint results, or a feature description.
  Translates complex or jargon-heavy content into plain business language.
  Use when presenting progress, decisions, or findings to leadership or clients.
allowed-tools: Read Write
---

# Stakeholder Summary Writer

You are writing a stakeholder-facing summary for a business analyst. Stakeholders — executives, clients, product owners — need to understand what is happening, what decisions were made, and what they need to do, without wading through technical details.

The golden rule: **if a non-technical manager could not understand it in 60 seconds, it needs to be simpler.**

## What you need before starting

Ask for (if not provided):
1. **What to summarise** — paste the notes, sprint report, meeting output, or description to be translated
2. **Audience** — who is reading this? (executive, client, internal stakeholder, board)
3. **Purpose** — is this a status update, a decision request, a go/no-go, or a findings report?
4. **Any decisions or actions needed from the reader?** — does the stakeholder need to do something after reading?

---

## Output formats

Choose the format that fits the purpose:

---

### Format A — Status Update

Use for: regular sprint updates, weekly progress reports, feature status

```
## [Feature / Project Name] — Status Update
[Date]

**Status:** 🟢 On Track / 🟡 At Risk / 🔴 Blocked

### What was completed
- [Plain-English summary of what was built or done]
- [Keep to 2–4 bullet points — no technical jargon]

### What is in progress
- [What is currently being worked on]

### Blockers or risks
- [Anything that could delay delivery — stated as a business impact, not a technical issue]
  e.g. "The integration with the payment provider is delayed, which may push the go-live date back by one week."

### Next steps
- [What happens next and by when]

### Decisions needed (if any)
- [Specific question requiring a yes/no or choice from the stakeholder]
```

---

### Format B — Decision Paper

Use for: asking a stakeholder or executive to choose between options

```
## Decision Required: [Topic]
[Date] | Requested by: [Name/Role]

### Background (2–3 sentences)
[Why this decision is needed now. What problem are we solving?]

### Options

**Option 1 — [Name]**
[What it involves in plain English]
- Pros: ...
- Cons: ...
- Cost/Effort: ...

**Option 2 — [Name]**
[What it involves]
- Pros: ...
- Cons: ...
- Cost/Effort: ...

### Recommendation
[Which option is recommended and the one key reason why]

### Decision needed by: [Date]
```

---

### Format C — Findings Summary

Use for: presenting research, analysis, or test results

```
## [Topic] — Findings Summary
[Date]

### What we looked at
[1–2 sentences on scope and method]

### Key findings
1. [Most important finding — stated as a business fact, not a technical observation]
2. [Second finding]
3. [Third finding]

### What this means for us
[1–2 sentences on the business implication]

### Recommended next steps
1. [Action] — [Owner] — [By when]
2. ...
```

---

## Writing rules

- **No acronyms without explanation** — write "API (the connector between two systems)" not just "API"
- **No passive voice** — "the team completed the feature" not "the feature was completed"
- **Numbers over adjectives** — "3 days late" not "slightly delayed"; "saves 2 hours per week" not "significant time saving"
- **One idea per sentence** — if a sentence has more than one clause, split it
- **Lead with the most important thing** — the first sentence should answer "so what?"

---

## After writing

Ask the user:
- "Does the tone match your audience — is this too formal / not formal enough?"
- "Are there any numbers or metrics I should include that you have available?"
