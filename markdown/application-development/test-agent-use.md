---
title: Author, execute, and troubleshoot tests and test suites with Test Agent
description: Use Test Agent to significantly reduce the skills and resources needed to troubleshoot test and test suite failures on covered metadata.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/test-agent-use.html
release: australia
topic_type: task
last_updated: "2026-04-21"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Test Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Author, execute, and troubleshoot tests and test suites with Test Agent

Use Test Agent to significantly reduce the skills and resources needed to troubleshoot test and test suite failures on covered metadata.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

    **Note:** You can also navigate to ServiceNow Studio in place of ServiceNow IDE.

    The ServiceNow IDE or ServiceNow Studio interface shows up depending on your navigation selection.

2.  Select the + icon under the ServiceNow Otto window on the right to start a new chat.

3.  Enter a prompt in the Build Agent chat panel to create a test/test suite or an application, or to run a new or existing test/test suite.

    You can achieve the following:

    -   Write ATF tests/test suites in the global scope by authoring tests/test suites from simple prompts, such as validating that all mandatory fields are completed before submitting the Incident form.
    -   Execute existing ATF tests/test suites.

        **Note:** If you want to execute an existing ATF test/test suite using Test Agent, you're expected to create the ATF test/test suite before this process. You can now use ServiceNow Otto to create an ATF test/test suite. Select the **Create with Otto** button on the ATF tests/test suites list page. If you have Build Agent installed on your instance, you are redirected to the ServiceNow IDE interface. You will see the following message if you don't have Build Agent installed on your instance.

        \[Omitted image "ta-ba-install.png"\] Alt text: Screenshot showing the banner message

        See [Create new test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-tut-build-first.md) for more information.

    -   Troubleshoot ATF test/test suite failures.
    -   Use Test Agent, an extension to building or editing apps with Build Agent, to generate ATF tests/test suites for newly built or edited functionality, run those tests/test suites, and troubleshoot failures directly within the ServiceNow IDE or ServiceNow Studio context.
    The Test Agent starts the process as mentioned in the prompt.

    As you enter a prompt, the interface page displays the associated code for an existing test/test suite or the code generated from the prompt.

4.  Review the information in the Test Agent console.

    **Note:** The content displayed in the Test Agent console depends on the tasks specified in the prompt.

    For example, if you're executing a test/test suite, the process first looks up the sys\_id, then builds and installs the latest code. After the build succeeds, it installs the latest changes on the instance and runs the test/test suite in the background.

    **Note:** If the test/test suite succeeds, the message saying that the test/test suite passed shows up on the console.

5.  If you're creating an application, generate tests/test suites based on the business rules and conditions defined in the prompt.

    The Test Agent starts the process as mentioned in the prompt. You can then review the information in the console as mentioned in the previous step. Once the tests/test suites are created, you can run them through another prompt.

    Each test/test suite displays a message indicating whether it passed or failed.

6.  Follow the automatic triaging process if the test/test suite execution fails.

    When a test/test suite fails, the Test Agent automatically starts the troubleshooting process. It identifies the step where the failure occurred and analyzes the root cause. The Test Agent then recommends possible fixes. After you select a recommended option, the Test Agent applies the fix, updates the test/test suite code, and reruns the test/test suite automatically. When the test/test suite passes, it provides a summary of the changes made to resolve the failure.


