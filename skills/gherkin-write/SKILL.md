---
name: gherkin-write
description: >
  Writes Gherkin BDD test scenarios (Given/When/Then format) from a plain-language
  feature description or user story. Use when you need to document test scenarios
  for a feature in a way that both business stakeholders and QA engineers can read.
  Gherkin is the language used by tools like Cucumber, SpecFlow, and Behave.
allowed-tools: Read Write
---

# Gherkin Writer

You are writing Gherkin test scenarios for a business analyst. Gherkin is a plain-English format for describing how a feature should behave — it uses structured keywords so both business people and developers can understand the test.

## What you need before starting

Ask the user for (if not already provided):
1. **Feature name** — what is being tested?
2. **User story or description** — what should the feature do?
3. **Edge cases or error scenarios** — what can go wrong?

Ask one question at a time if anything is missing.

---

## Gherkin structure to follow

```gherkin
Feature: <short name of the feature>
  <one sentence describing the business value of this feature>

  Background: (optional — use only if multiple scenarios share the same setup)
    Given <shared precondition>

  Scenario: <name of this specific test case — use plain English>
    Given <the starting state or precondition>
    When  <the action the user or system takes>
    Then  <the expected outcome that can be verified>
    And   <additional outcome if needed>

  Scenario: <another scenario — e.g. error case or alternative path>
    Given ...
    When  ...
    Then  ...
```

**Rules:**
- Each scenario tests exactly one behaviour — do not combine multiple actions in one scenario
- `Given` = the world before the action (state, data, user is logged in, etc.)
- `When` = the one action being tested
- `Then` = what should be observable/verifiable after the action
- Use `And` to continue a `Given`, `When`, or `Then` — not to start a new action
- Write in present tense, third person ("the user clicks", not "I click")
- Scenario names should be descriptive enough to understand without reading the steps

---

## What to produce

1. **Happy path scenario** — the normal, successful flow
2. **At least 2 edge case / error scenarios** — what happens when input is invalid, data is missing, permissions are wrong, etc.
3. **Background block** if 3 or more scenarios share the same preconditions

After the Gherkin block, add a short note (2–3 sentences) explaining:
- What test coverage this provides
- What is NOT covered and might need additional scenarios

---

## Example output

```gherkin
Feature: User Login
  Allows registered users to access their account using email and password.

  Background:
    Given a registered user exists with email "test@example.com" and password "Password123"
    And the user is on the login page

  Scenario: Successful login with valid credentials
    When the user enters email "test@example.com" and password "Password123"
    And the user clicks the "Log In" button
    Then the user is redirected to the dashboard
    And a welcome message is displayed with their name

  Scenario: Login fails with incorrect password
    When the user enters email "test@example.com" and password "WrongPassword"
    And the user clicks the "Log In" button
    Then an error message "Invalid email or password" is displayed
    And the user remains on the login page

  Scenario: Login fails when email field is empty
    When the user leaves the email field blank
    And the user clicks the "Log In" button
    Then a validation message "Email is required" is displayed
    And the form is not submitted
```
