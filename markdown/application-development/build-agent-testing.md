---
title: Test what you built with Build Agent
description: Test Agent generates test coverage for code created by Build Agent, executes tests, and performs root cause analysis \(RCA\) on failures. Prompt Test Agent to complete build-to-test workflows in a single development session without manual test authoring or failure investigation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/build-agent-testing.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Test what you built with Build Agent

Test Agent generates test coverage for code created by Build Agent, executes tests, and performs root cause analysis \(RCA\) on failures. Prompt Test Agent to complete build-to-test workflows in a single development session without manual test authoring or failure investigation.

Test Agent extends Build Agent by making every build safe before release. After Build Agent produces code changes in a development instance, Test Agent consumes the same prompt and code context. It uses those to author functional Automated Test Framework \(ATF\) tests, execute those tests, and triage any failures automatically.

-   For details on configuring tests in Build Agent, see [Configure auto test prompting and UI tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-config-testing.md).
-   For more information ATF test generation, see [ATF test generation in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/test-agent-atf-test-gen-ba.md).
-   For complete documentation on using Test Agent, see [Test Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/test-agent-landing-page.md).

If a test fails, Test Agent performs an RCA. Then it either auto-applies safe fixes or surfaces actionable guidance in the chat panel so you can resolve the issue without leaving ServiceNow Studio or the ServiceNow IDE.

## Customer outcomes

Test Agent delivers the following measurable outcomes:

-   Build and test in one session: You no longer need to context-switch between authoring code and writing tests. Both happen sequentially within the same session.
-   Faster failure triage: Automated RCA and proposed fixes reduce the time you spend looking through logs after a test run.
-   More release confidence: Measurable quality gates enforced by automated test execution give you verifiable evidence of code health before promotion to production instances.
-   Generated ATF tests are stored in the sys\_atf\_tests \[sys\_atf\_tests\] table under the app scope for which they were created. You can schedule regression test runs using the generated tests.

## Test generation prompting

After each development action in Build Agent, Test Agent asks whether to generate ATF tests for what you just built. You can accept or decline the prompt at each step. When you accept the prompt, Test Agent generates tests before returning control to you in the chat panel.

\[Omitted image "ba-tests-prompt-for.png"\] Alt text: Prompt asking whether to write tests to cover the app, with Yes, proceed selected and a Submit button.

Automatic prompting for tests reduces the chance of skipping test coverage during rapid development by keeping test generation as part of the standard development loop.

To manually prompt for tests, ask Build Agent to `Generate ATF tests for all the feature permutations on the app we built`. Then, you can tell Build Agent to `Execute all ATF tests.`

## Test Agent workflow

The end-to-end workflow is:

1.  Create or edit an app in a development instance using Build Agent in ServiceNow Studio or the ServiceNow IDE, driven by your prompt.
2.  Alternatively, start from an Autonomous Engineer application plan. Test Agent reads the stories and acceptance criteria in the plan and generates tests automatically as implementation begins, without a separate prompt. For more information on running tests in Autonomous Engineer, see [Autonomous Engineer in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-autonomous-engineer.md).
3.  Test Agent consumes the prompt and the resulting code changes to generate contextually relevant functional and UI ATF tests.
4.  Respond to Build Agent asking whether you want to run the tests.
5.  Failures are automatically triaged. Test Agent produces an RCA and either applies safe fixes autonomously or proposes them to you through the chat panel.
6.  Build Agent ingests the RCA from Test Agent and re-executes tests until a passing status is achieved, completing the auto-heal loop. Stale tests are automatically updated to reflect the newest functionality.
7.  Alternatively, ask Build Agent to create or run a test suite to execute multiple tests as a group and review consolidated results in the chat panel.

## Key developer experiences for Test Agent in Build Agent

-   **Autonomous test authoring**

    When you use Build Agent to implement a story, you can prompt it to create functional and UI tests automatically.

-   **Test generation from Autonomous Engineer plans**

    When you use Autonomous Engineer to produce an application plan, Build Agent hands off that plan to Test Agent as implementation begins. Test Agent reads each story and its acceptance criteria in the plan and automatically generates Automated Test Framework tests to validate the expected behavior. Generated tests are executed immediately, and any failures are triaged by Test Agent before control returns to you in the chat panel. This closes the loop from planning to tested implementation within a single Build Agent session, without a separate prompt to create or run tests.

-   **UI testing**

    Generate comprehensive UI tests for applications you build with Build Agent. UI testing extends the existing functional test capability to cover browser-level interactions, such as multi-step page navigation flows. Request a UI test by prompting Build Agent to generate a UI test for the application or flow you want to validate. For more information, see [UI Test Script in Automated Test Framework \(ATF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/test-agent-ui-test-script-atf.md).

-   **List and related list step generation**

    Test Agent can generate ATF tests that use list and related list test steps, including validate related list visibility and apply filter to list tests. List step support extends test coverage beyond form-based interactions to include list view interactions on the ServiceNow AI Platform. For more information on list and related list test steps, see [List and Related List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/test-steps-list-related-list.md).

-   **Test suite authoring and execution**

    Create ATF test suites and edit existing ones from Build Agent. Group individual tests under a suite and execute the suite from the chat panel to run regression testing without selecting individual tests. Execution status and any errors are reported in the chat panel. For more information on test suites, see [Building and running automated test suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-suites-overview.md).

-   **Automatically updated tests**

    Test Agent automatically identifies outdated ATF tests as your application changes, and updates or removes them to keep your test suite aligned with your current code. Tests that no longer map to application artifacts are removed. Tests that partially match updated artifacts are revised to reflect the current implementation. Automatic test maintenance reduces the overhead of keeping ATF tests synchronized with ongoing development and removes the need to manually audit and update tests after each code change.

-   **Auto-healing**

    Build Agent consumes the RCA produced by Test Agent and applies fixes to code or tests, then re-executes the test suite until all tests reach a passing status. This removes the need for developers to manually patch and maintain tests during a session.

-   **Assisted troubleshooting**

    Test Agent automatically troubleshoots failed tests, generates RCAs, and proposes targeted fixes, eliminating manual log investigation.


## Scope and availability

Test Agent is available in the following environments and scopes:

|Dimension|Supported values|
|---------|----------------|
|Authoring environment|ServiceNow Studio, the ServiceNow IDE, and the ServiceNow SDK \(execution tool only\)|
|Application scope|Global, custom, store|
|Test types|ATF functional tests, UI tests, and test suitesATF functional and UI tests|
|Execution target|Cloud Runner lanes|

**Note:** Test execution requires the ATF Test Generator and Cloud Runner app to be installed and a cloud user set up. For more information, see [ATF Test Generator and Cloud Runner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/atf-tg-cr-intro.md).

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-build-agent.md)

