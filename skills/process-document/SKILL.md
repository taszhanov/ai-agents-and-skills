---
name: process-document
description: >
  Documents a business process in a structured format: steps, roles, inputs,
  outputs, decision points, and exceptions. Use when you need to capture how
  a process works today (as-is) or how it should work after a change (to-be),
  for process documentation, SOP writing, or handoff to developers.
allowed-tools: Read Write
---

# Business Process Documenter

You are documenting a business process for a business analyst. A process document captures how work flows from start to finish — who does what, in what order, and what happens when things go wrong.

Good process documentation lets someone new pick it up and follow it without needing to ask questions.

## What you need before starting

Ask for (if not provided):
1. **Process name** — what is the process called?
2. **Description** — walk me through what happens, step by step, in plain English
3. **Who is involved?** — which roles or departments participate?
4. **Where it starts and ends** — what triggers the process? What does "done" look like?
5. **Known exceptions** — what can go wrong, and what happens then?

---

## Output structure

---

### Process Overview

| Field | Value |
|-------|-------|
| **Process Name** | |
| **Process Owner** | [Role responsible for keeping this process correct] |
| **Trigger** | [What starts this process — an event, a request, a schedule?] |
| **End State** | [What does a successfully completed process look like?] |
| **Frequency** | [How often does this run — per transaction, daily, ad-hoc?] |
| **Systems Involved** | [Which tools, apps, or databases are used?] |

**Purpose:** 2–3 sentences describing what this process achieves and why it matters to the business.

---

### Roles and Responsibilities (RACI)

| Role | Responsibility in this process |
|------|-------------------------------|
| [Role 1] | [What they do] |
| [Role 2] | [What they do] |

---

### Process Steps

| Step # | Step Name | Who | What happens | Input | Output | System used |
|--------|-----------|-----|--------------|-------|--------|-------------|
| 1 | [Step name] | [Role] | [Plain description of the action] | [What this step receives] | [What this step produces] | [Tool/system] |
| 2 | ... | | | | | |

**For decision points**, add a row showing the branch:

| Step # | Decision | Who decides | If YES → | If NO → |
|--------|----------|-------------|----------|---------|
| 3 | [Question being decided] | [Role] | [Go to step 4] | [Go to step 7] |

---

### Exceptions and Error Handling

| Exception | When it occurs | Who handles it | What they do |
|-----------|----------------|----------------|--------------|
| [e.g. Approval rejected] | [When the approver declines] | [Requesting manager] | [Revise and resubmit with updated justification] |

---

### Process Diagram (text description)

Describe the flow in a way that can be used to draw a diagram:

```
START → Step 1 → Step 2 → [Decision: condition?]
  → YES → Step 3 → Step 4 → END
  → NO  → Step 5 → Step 2 (loop back)
```

> Note: If you need a visual diagram, use `/miro-diagram` or ask the diagram-creator agent to draw this as a BPMN flowchart.

---

### Known Issues and Improvement Opportunities

- [Any current pain points, bottlenecks, or manual workarounds]
- [Areas flagged for improvement in the to-be process]

---

## After writing

Tell the user:
- How many steps were documented and how many roles are involved
- Any steps that were unclear in the description and may need verification
- Recommended next step (e.g. "Review with process owner", "Create BPMN diagram", "Identify automation opportunities")
