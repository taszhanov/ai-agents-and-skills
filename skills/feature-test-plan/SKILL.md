---
name: feature-test-plan
description: >
  Creates a structured test plan for a specific feature or release. Covers scope,
  test types, test cases summary, entry/exit criteria, and sign-off checklist.
  Use before starting testing on a new feature to align QA, developers, and
  stakeholders on what will and will not be tested.
allowed-tools: Read Write
---

# Feature Test Plan Writer

You are writing a test plan for a business analyst. A test plan is a document that answers: **"What will we test, how will we test it, and how will we know when testing is complete?"**

It keeps developers, testers, and stakeholders aligned before testing begins — so there are no surprises about scope or what "done" means.

## What you need before starting

Ask for (if not provided):
1. **Feature name and description** — what is being tested?
2. **User stories or requirements** — what does the feature need to do?
3. **Out of scope** — what will NOT be tested in this cycle?
4. **Test environment** — where will testing happen? (dev, staging, UAT)
5. **Who is testing** — QA engineer, BA, developer, or end-user UAT?

---

## Test plan output structure

---

### 1. Overview

| Field | Value |
|-------|-------|
| **Feature** | [Feature name] |
| **Version / Sprint** | [e.g. v2.1 / Sprint 14] |
| **Test Lead** | [Name or role] |
| **Target Test Date** | [Date range] |
| **Environment** | [Dev / Staging / UAT / Production] |

**Feature summary:** 2–3 sentences describing what the feature does and why it matters to the user.

---

### 2. Scope

**In scope — will be tested:**
- [List of functionality, flows, and scenarios covered]

**Out of scope — will NOT be tested in this cycle:**
- [List of explicitly excluded areas and why — e.g. "Performance testing is out of scope for this sprint"]

---

### 3. Test Types

Check which test types apply and briefly describe the approach for each:

| Test Type | Included? | Approach |
|-----------|-----------|----------|
| Functional testing | Yes/No | Verify each requirement manually |
| Negative / error path testing | Yes/No | Test with invalid inputs and edge cases |
| Regression testing | Yes/No | Re-run existing tests for affected areas |
| UI / visual testing | Yes/No | Check layout, labels, and responsive behaviour |
| Integration testing | Yes/No | Verify interaction with [system/API/database] |
| UAT (User Acceptance Testing) | Yes/No | Business stakeholder sign-off |

---

### 4. Test Case Summary

List the key scenarios to be tested (not full test cases — just titles and priority):

| ID | Scenario | Type | Priority |
|----|----------|------|----------|
| TC-001 | [Scenario title] | Positive | High |
| TC-002 | [Scenario title] | Negative | High |
| TC-003 | [Scenario title] | Edge case | Medium |

> Full test cases should be written separately using `/test-case-write`.

---

### 5. Entry Criteria
Testing will NOT begin until all of these are true:
- [ ] Feature is deployed to the test environment
- [ ] Test data is available and prepared
- [ ] Requirements / user stories are finalised and signed off
- [ ] Previous critical bugs are resolved

---

### 6. Exit Criteria
Testing is considered complete when:
- [ ] All High-priority test cases have passed
- [ ] No open Critical or Major bugs remain
- [ ] All Medium test cases have been executed (pass or documented exception)
- [ ] Stakeholder sign-off received (for UAT)

---

### 7. Risks

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| [e.g. Test data not ready] | Medium | High | Prepare test data set in advance |

---

### 8. Sign-Off

| Role | Name | Sign-Off Date |
|------|------|---------------|
| QA Lead | | |
| Product Owner | | |
| Developer | | |

---

## After writing

Tell the user:
- How many test scenarios are covered
- Any obvious gaps in test coverage based on the requirements
- Recommended next step (e.g. "Write full test cases using /test-case-write")
