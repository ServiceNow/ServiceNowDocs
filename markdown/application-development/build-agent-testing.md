---
title: Testing what you built
description: Test Agent generates test coverage for code created by Build Agent, executes tests, and performs root cause analysis on failures. Prompt Test Agent to complete build-to-test workflows in a single development session without manual test authoring or failure investigation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Testing what you built

Test Agent generates test coverage for code created by Build Agent, executes tests, and performs root cause analysis on failures. Prompt Test Agent to complete build-to-test workflows in a single development session without manual test authoring or failure investigation.

Test Agent extends Build Agent by making every build safe before release. After Build Agent produces code changes in a development instance, Test Agent consumes the same prompt and code context to author functional Automated Test Framework \(ATF\) tests, execute those tests, and triage any failures automatically.

For complete documentation on using Test Agent, see [Test Agent](../../../administer/test-agent/reference/test-agent-landing-page.md).

When a test fails, Test Agent performs a root cause analysis \(RCA\) and either auto-applies safe fixes or surfaces actionable guidance in the chat panel so you can resolve the issue without leaving ServiceNow Studio or the ServiceNow IDE.

## Customer outcomes

Test Agent delivers the following measurable outcomes:

-   Build and test in one session: You no longer need to context-switch between authoring code and writing tests. Both happen sequentially within the same Build Agent session.
-   Faster failure triage: Automated RCA and proposed fixes reduce the time you spend looking through logs after a test run.
-   More release confidence: Measurable quality gates enforced by automated test execution give you verifiable evidence of code health before promotion to production instances.
-   Generated ATF tests are stored in the sys\_atf\_tests table under the app scope for which they were created. You can schedule regression test runs using the generated tests.

## Example prompts

An example prompt to get Build Agent to create and run ATF tests would be `Generate ATF tests for all the feature permutations on the app we built`.

Then, you can tell Build Agent to `Execute all ATF tests.`

## Test Agent workflow

The end-to-end workflow is:

1.  Create or edit an app in a development instance using Build Agent in ServiceNow Studio or the ServiceNow IDE, driven by your prompt.
2.  Test Agent consumes the prompt and the resulting code changes to generate contextually relevant functional ATF tests.
3.  Prompt Build Agent to run the tests.
4.  Failures are automatically triaged. Test Agent produces an RCA and either applies safe fixes autonomously or proposes them to you through the Build Agent chat panel.
5.  Build Agent ingests the RCA from Test Agent and re-executes tests until a passing status is achieved, completing the auto-heal loop.

## Key developer experiences

-   **Autonomous test authoring**

    When you use Build Agent to implement a new story, you can prompt it to create functional tests automatically.

-   **Assisted troubleshooting**

    Test Agent automatically troubleshoots failed tests, generates RCAs, and proposes targeted fixes, eliminating manual log investigation.

-   **Auto-healing**

    Build Agent consumes the RCA produced by Test Agent and applies fixes to code or tests, then re-executes the test suite until all tests reach a passing status. This removes the need for developers to manually patch and maintain tests during a session.


## Scope and availability

Test Agent is available in the following environments and scopes:

|Dimension|Supported values|
|---------|----------------|
|Authoring environment|ServiceNow Studio, the ServiceNow IDE|
|Application scope|Global, custom, store|
|Test types|ATF functional tests|
|Execution target|Cloud Runner lanes|

**Note:** Test execution requires the ATF Test Generator and Cloud Runner app to be installed and a cloud user set up. See here for more details: https://www.servicenow.com/docs/r/zurich/servicenow-platform/atf-test-generator-and-cloud-runner/atf-tg-cr-intro.html

**Parent Topic:**[Use Build Agent](../tasks/use-build-agent.md)

