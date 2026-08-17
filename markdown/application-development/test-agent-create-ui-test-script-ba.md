---
title: Create a UI Test Script in Build Agent
description: Create test scripts for custom user interfaces using conversational interaction with Build Agent. UI Test Scripts expose elements of Testing Library and run as part of the Automated Test Framework \(ATF\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/test-agent-create-ui-test-script-ba.html
release: australia
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 2
breadcrumb: [UI Test Script in Automated Test Framework \(ATF\), Use, Test Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Create a UI Test Script in Build Agent

Create test scripts for custom user interfaces using conversational interaction with Build Agent. UI Test Scripts expose elements of Testing Library and run as part of the Automated Test Framework \(ATF\).

## Before you begin

-   Build Agent is available in your ServiceNow Studio instance or IDE
-   You have access to ATF and Testing Library capabilities

Role required: admin

## About this task

UI Test Script enables agentic authoring through conversational interaction. Instead of manually writing test code, you describe your testing needs to Build Agent and it generates Testing Library code for you.

## Procedure

1.  In ServiceNow Studio or the IDE, open Build Agent.

    Build Agent is the agentic authoring interface for creating tests and test scripts.

2.  Navigate to the UI Test Script authoring section.

3.  Describe your test requirements conversationally to Build Agent.

    Provide a natural language description of what you want to test. For example:

    -   Create a test that fills out a user profile form with name and email, then selects the **Submit** button
    -   Test that the error message appears when a required field is left empty
    -   Verify that the dashboard loads and displays the correct widgets
4.  Review the generated test script code.

    Build Agent generates test code using the UI Test Script API supporting a subset of Testing Library syntax. The code appears in an editor or panel where you can review it for accuracy.

    -   Correct element selectors targeting your UI components
    -   Appropriate Testing Library methods for user interactions
    -   Meaningful assertions that validate expected behavior
5.  Refine the test script through conversational feedback.

    If the generated script needs changes, provide conversational feedback to Build Agent. For example:

    -   Add an assertion for the success message after submit
    -   Change the email field selector to use the aria-label attribute
    -   Add a wait before checking the result
    Build Agent updates the test code based on your feedback.

6.  Package the UI Test Script as an ATF step.

    Choose how to integrate the test:

    -   **Single step:** Package the entire UI Test Script as one ATF step
    -   **With other steps:** Include the UI Test Script alongside other ATF test steps in the same test case
7.  Save the test script.

8.  Run the test to verify it works correctly.

    Execute the test through ATF. The test runs in the client test runner and produces:

    -   Overall pass/fail result at the ATF step level
    -   Line-level success/failure indicators for each assertion in the test code

## Result

After you complete these steps, you have created a UI Test Script that:

-   Uses Testing Library syntax to interact with and validate your custom UI
-   Runs as an ATF step alongside other tests
-   Produces pass/fail results with line-level detail showing which assertions succeeded or failed
-   Can be refined further through conversational feedback with Build Agent

If the test fails, review the UI Test Script logs and screenshots to understand what went wrong, then use conversational feedback to update the test script.

