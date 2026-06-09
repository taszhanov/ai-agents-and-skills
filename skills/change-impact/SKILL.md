---
name: change-impact
description: >
  Produces a change impact assessment for a proposed feature, process change, or
  system update. Identifies which users, teams, systems, and processes are affected,
  how they are affected, and what actions are needed to manage the transition.
  Use before a major release, process change, or when assessing the risk of a change.
allowed-tools: Read Write
---

# Change Impact Assessment

You are producing a change impact assessment for a business analyst. A change impact assessment answers: **"If we make this change, what else does it affect and what do we need to do about it?"**

It prevents surprises by identifying downstream effects on people, processes, and systems before a change goes live.

## What you need before starting

Ask for (if not provided):
1. **The change** — what is being changed? (a feature, a process, a system, a policy)
2. **The reason** — why is this change being made?
3. **Go-live date** — when is this expected to happen?
4. **Known affected areas** — which teams, systems, or users are already known to be affected?

---

## Output structure

---

### Change Summary

| Field | Value |
|-------|-------|
| **Change name** | |
| **Type** | Feature / Process / Policy / System / Data |
| **Proposed go-live** | |
| **Change owner** | |
| **Impact level** | High / Medium / Low |

**Description:** 2–3 sentences explaining what is changing and why, in plain English.

---

### Impact Assessment

#### People Impact

| Group | How affected | Severity | Action required |
|-------|-------------|----------|-----------------|
| [e.g. Customer Support team] | [They will need to handle new request type] | High | Training required before go-live |
| [e.g. End users] | [New login flow — they will need to re-authenticate] | Medium | Communication email required |

**Severity guide:**
- **High** — significant change to daily work or customer experience
- **Medium** — noticeable change but manageable with minimal support
- **Low** — minor or invisible to the affected group

---

#### Process Impact

| Process | How it changes | Owner | Action required |
|---------|---------------|-------|-----------------|
| [Process name] | [What changes in the steps or flow] | [Role] | [Update SOP / retrain / communicate] |

---

#### System / Technical Impact

| System | How affected | Action required | Owner |
|--------|-------------|-----------------|-------|
| [System name] | [e.g. New API endpoint needed, database schema change] | [What needs to be done] | [Team] |

---

#### Data Impact

| Data entity | What changes | Risk | Action required |
|-------------|-------------|------|-----------------|
| [e.g. Customer records] | [e.g. New field added, existing field format changes] | [e.g. Migration risk for existing data] | [Migration plan, data validation] |

---

### Risk Register

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| [e.g. Users are not trained in time] | Medium | High | Schedule training 2 weeks before go-live |
| [e.g. Legacy system incompatibility] | Low | High | Test integration in staging before release |

---

### Communication Plan

| Audience | Message | Channel | When | Owner |
|----------|---------|---------|------|-------|
| [e.g. All end users] | [What they need to know] | [Email / Slack / Town hall] | [Date] | [Role] |

---

### Readiness Checklist

Before go-live, the following must be complete:
- [ ] All affected teams have been informed
- [ ] Training completed for impacted roles
- [ ] SOPs and documentation updated
- [ ] Systems tested in staging
- [ ] Rollback plan defined (what happens if the change needs to be reversed)
- [ ] Communication sent to end users

---

### Open Questions

List anything that needs a decision or more information before the impact assessment can be finalised.

---

## After writing

Tell the user:
- The overall impact level (High / Medium / Low) and the key reason
- The most critical action to complete before go-live
- Any open questions that need urgent resolution
