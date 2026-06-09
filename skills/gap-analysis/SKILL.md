---
name: gap-analysis
description: >
  Produces a structured gap analysis comparing the current state ("as-is") to the
  desired future state ("to-be"). Identifies what is missing, what needs to change,
  and what can stay the same. Use when evaluating a process, system, or capability
  against a target or new requirement.
allowed-tools: Read Write
---

# Gap Analysis

You are producing a gap analysis for a business analyst. A gap analysis answers the question: **"Where are we now, where do we need to be, and what is the gap between them?"**

It is used to identify what needs to change before a new feature, process, or system can go live.

## What you need before starting

Ask for (if not provided):
1. **Current state (As-Is)** — how does the process, system, or capability work today?
2. **Target state (To-Be)** — what should it look like after the change?
3. **Scope** — are we analysing a process, a system, a team's capabilities, or something else?
4. **Driver** — why is this change needed? (new regulation, customer request, strategic goal, etc.)

---

## Output structure

### Executive Summary
3–4 sentences: What was analysed, what is the main finding, and what is the recommended next step?

---

### Current State (As-Is)
Describe how things work today. Be factual — no judgement yet.
- What process/system/capability exists?
- Who is involved?
- What are its known strengths?
- What are its known weaknesses or pain points?

---

### Target State (To-Be)
Describe what the future looks like after the change is made.
- What should the process/system/capability do?
- What standards, requirements, or expectations must it meet?
- What does success look like?

---

### Gap Analysis Table

| # | Area | Current State | Target State | Gap | Priority | Recommended Action |
|---|------|---------------|--------------|-----|----------|--------------------|
| 1 | [e.g. User Authentication] | [what exists now] | [what is needed] | [what is missing] | High/Medium/Low | [what to do] |
| 2 | ... | ... | ... | ... | ... | ... |

**Gap types:**
- **Missing** — does not exist at all, needs to be built
- **Partial** — exists but does not fully meet the requirement
- **Compliant** — already meets the target state (no gap)
- **Excess** — exists but is no longer needed (consider removing)

---

### Prioritised Action Plan

Numbered list of recommended actions, ordered from highest to lowest priority:

1. **[Action]** — [Why this is first / what it unblocks]
2. ...

---

### Risks and Dependencies

- What could prevent closing these gaps?
- Are there dependencies between gaps (e.g. Gap 3 cannot be closed until Gap 1 is resolved)?
- Are there external factors (regulations, third-party systems, team capacity)?

---

### Open Questions

List anything that could not be determined from the information provided and needs a decision or further investigation before action can be taken.

---

## After writing

Tell the user:
- How many gaps were found and at what priority level
- Which gaps are blockers (must be resolved before anything else can move forward)
- What the single most important next step is
