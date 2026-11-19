---
title: Testing agentically developed apps
description: As part of the agentic development process on the ServiceNow AI Platform, Build Agent can generate, run, and troubleshoot Automated Test Framework \(ATF\) tests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/vc-and-atf.html
release: australia
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [vibe coding, AI-assisted development, automated testing, test generation, application development, quality assurance]
audience: developer
breadcrumb: [Develop, Agentic development, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Testing agentically developed apps

As part of the agentic development process on the ServiceNow AI Platform, Build Agent can generate, run, and troubleshoot Automated Test Framework \(ATF\) tests.

When you use agentic development, the ServiceNow AI Platform can:

-   Scaffold the data model, business logic, and user interface based on your prompts.
-   Generate ready-to-use ATF tests that validate the functionality of your new applications or flows.
-   Incorporate quality assurance and code resilience from the start, reducing the need to address them after initial development.

This means you can go from idea to a working, testable app much faster. After the initial generation, you can refine the app and its tests in ServiceNow Studio or the ServiceNow IDE, and run the ATF tests to verify that the app functions correctly.

**Note:** Build Agent can create, edit, and run ATF tests. For more information, see [Test what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent-testing.md).

Test Agent generates ATF tests for code that Build Agent creates, runs the tests, and performs a root cause analysis \(RCA\) on failures. If a test fails, Test Agent applies safe fixes or surfaces guidance in the chat panel.The tests can include ATF functional tests and UI tests. For details on configuring tests, see [Configure auto test prompting and UI tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ba-config-testing.md).You can also ask Build Agent to create or run a test suite to run multiple tests as a group.

Test execution requires the ATF Test Generator and Cloud Runner app to be installed and a cloud user set up. For more information, see [ATF Test Generator and Cloud Runner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/atf-tg-cr-intro.md).

If you start from an Autonomous Engineer plan, Test Agent reads the stories and acceptance criteria in the plan and generates tests as implementation begins, without a separate prompt. For more information, see [Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/autonomous-engineer.md).

ATF has a troubleshooting agent to debug test failures on specific metadata. For details, see [ATF troubleshooting agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/automated-test-framework-atf/atf-troubleshooting-agent-landing-page.md).

For full documentation on Automated Test Framework, see [Automated Test Framework \(ATF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/automated-test-framework-atf/atf-landing-page.md).

**Parent Topic:**[Agentic development on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/vibe-coding-using.md)

