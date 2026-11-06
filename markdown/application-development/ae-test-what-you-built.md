---
title: Test what you built with Autonomous Engineer
description: Test Agent generates test coverage for each work item that Autonomous Engineer builds, executes the tests, and performs root cause analysis \(RCA\) on failures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/ae-test-what-you-built.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 3
keywords: [Autonomous Engineer, Test Agent, ATF, automated testing, work items, root cause analysis]
breadcrumb: [Use, Autonomous Engineer, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Test what you built with Autonomous Engineer

Test Agent generates test coverage for each work item that Autonomous Engineer builds, executes the tests, and performs root cause analysis \(RCA\) on failures.

Autonomous Engineer runs Test Agent on each work item as part of plan execution. Build Agent provides the underlying execution layer for this testing. Tests are generated and run for each work item, and the results appear directly under the work item in the plan dashboard.

To enable testing in Autonomous Engineer, see [Configure auto test prompting and UI tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ba-config-testing.md).

For complete documentation on Test Agent, see [Test Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/test-agent-landing-page.md).

\[Omitted image "ae-tests-run.png"\] Alt text: Work item showing description, acceptance criteria, and ATF tests section with 3 of 3 tests passed. For details, refer to the surrounding text.

If a test fails, Test Agent performs an RCA. It then either applies safe fixes autonomously or surfaces actionable guidance in the chat panel so you can resolve the issue without leaving ServiceNow Studio.

## Test Agent capabilities in Autonomous Engineer

When used with Autonomous Engineer, Test Agent does the following:

-   Generates tests within the same plan execution, without a separate prompt.
-   Runs the tests and shows the results under each work item.
-   Performs root cause analysis on failures and either applies safe fixes or proposes fixes in the chat panel.
-   Generated ATF tests are stored in the sys\_atf\_tests \[sys\_atf\_tests\] table under the app scope for which they were created. You can schedule regression test runs using the generated tests.

## Test generation

If automatic test generation is enabled in Build Agent settings, Autonomous Engineer generates tests for the acceptance criteria of each work item.

Automatic prompting for tests reduces the chance of skipping test coverage during execution by keeping test generation part of the standard work item loop.

To manually prompt for tests, ask Autonomous Engineer to `Generate ATF tests for all the feature permutations on the app we built`. Then tell Autonomous Engineer to `Execute all ATF tests.`

## Test Agent workflow

The end-to-end workflow is:

1.  Autonomous Engineer builds a work item in the execution phase.
2.  Test Agent uses the work item context to generate contextually relevant functional, UI, and ATF tests.
3.  Autonomous Engineer asks whether you want to run the tests.
4.  Failures are automatically triaged. Test Agent produces an RCA and either applies safe fixes autonomously or proposes them through the chat panel.
5.  Autonomous Engineer ingests the RCA and re-executes tests until a passing status is achieved, completing the auto-heal loop. Stale tests are automatically updated to reflect the newest functionality.
6.  View tests in the **Work item** dashboard.
7.  Optionally, ask Autonomous Engineer to create or run a test suite to execute multiple tests as a group and review consolidated results in the chat panel.

## Scope and availability

Test Agent is available for Autonomous Engineer in the following environments and scopes:

|Dimension|Supported values|
|---------|----------------|
|Authoring environment|ServiceNow Studio|
|Application scope|Global, custom, store|
|Test types|ATF functional tests, UI tests, and test suites|
|Execution target|Cloud Runner lanes|

**Note:** Test execution requires the ATF Test Generator and Cloud Runner app to be installed and a cloud user set up. For more information, see [ATF Test Generator and Cloud Runner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/atf-tg-cr-intro.md).

**Parent Topic:**[Using Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-using-autonomous-engineer.md)

