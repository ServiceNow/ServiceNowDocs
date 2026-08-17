---
title: UI Test Script in Automated Test Framework \(ATF\)
description: UI Test Script enables you to create test code for custom user interfaces exposing elements of Testing Library within the Automated Test Framework \(ATF\). Generate test scripts through conversational interaction with Build Agent and run them alongside other ATF tests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/test-agent-ui-test-script-atf.html
release: australia
topic_type: concept
last_updated: "2026-07-27"
reading_time_minutes: 1
breadcrumb: [Use, Test Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# UI Test Script in Automated Test Framework \(ATF\)

UI Test Script enables you to create test code for custom user interfaces exposing elements of Testing Library within the Automated Test Framework \(ATF\). Generate test scripts through conversational interaction with Build Agent and run them alongside other ATF tests.

## Key benefits

UI Test Script provides these benefits:

-   Agentic authoring through conversational interaction reduces manual test code writing effort
-   Test API exposes elements of Testing Library, a widely-used UI testing library with consistent patterns
-   Test scripts integrate seamlessly with ATF framework and run in the client test runner
-   Line-level success/failure indicators help you quickly identify and fix failing assertions
-   Conversational editing allows you to refine test scripts through natural language interaction with Build Agent

## How it works

UI Test Script operates in two phases: authoring and execution.

**Authoring Phase:**

-   You interact conversationally with Build Agent to describe the UI test you want to create
-   The UI Test Script Skill generates test code using Testing Library syntax
-   Generated test scripts can be packaged as a single "UI Test Script" step in ATF, or included alongside existing steps
-   You can refine tests by providing conversational feedback through the Build Agent panel

**Execution Phase:**

-   UI Test Scripts run as part of the ATF framework in the client test runner
-   The overall test passes or fails at the ATF step level
-   Line-level indicators within the test code show which specific assertions succeeded or failed

## Test results and feedback

When UI Test Scripts run, you receive results at two levels:

-   Step level: The overall "UI Test Script" step passes or fails in ATF based on the cumulative result of all assertions
-   Line level: Inside the test code, individual assertions show success or failure indicators, helping you pinpoint which checks passed and which failed

## Troubleshooting

The troubleshooting process in UI Test Scripts is manual:

-   Review UI Test Script logs to see execution details
-   Check test run screenshots to visually verify what the test was attempting
-   Modify the test script conversationally through Build Agent if changes are needed

## Availability

UI Test Script is available in the following environments:

-   ServiceNow Studio \(SNS\)
-   IDE \(Integrated Development Environment\)
-   Standard ATF forms and lists \(for non-conversational creation\)

