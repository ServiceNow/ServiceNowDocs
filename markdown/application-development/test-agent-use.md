---
title: Author, execute, and troubleshoot tests with Test Agent
description: Use Test Agent to significantly reduce the skills and resources needed to troubleshoot test failures on covered metadata.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-21"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Test Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Author, execute, and troubleshoot tests with Test Agent

Use Test Agent to significantly reduce the skills and resources needed to troubleshoot test failures on covered metadata.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

    **Note:** You can also navigate to ServiceNow Studio in place of ServiceNow IDE.

    The ServiceNow IDE or ServiceNow Studio interface shows up depending on your navigation selection.

2.  Select the + icon under the Now Assist window on the right to start a new chat.

3.  Enter a prompt in the Build Agent chat panel to create a test or an application, or to run a new or existing test.

    You can achieve the following:

    -   Write ATF tests in the global scope by authoring tests from simple prompts, such as validating that all mandatory fields are completed before submitting the Incident form.
    -   Execute existing ATF tests.

        **Note:** If you want to execute an existing ATF test using Test Agent, you're expected to create the ATF test before this process. See [Create new test](../../auto-test-framework/task/atf-tut-build-first.md#) for more information.

    -   Troubleshoot ATF test failures.
    -   Use Test Agent, an extension to building or editing apps with Build Agent, to generate ATF tests for newly built or edited functionality, run those tests, and troubleshoot failures directly within the IDE or ServiceNow Studio context.
    The Test Agent starts the process as mentioned in the prompt.

    As you enter a prompt, the interface page displays the associated code for an existing test or the code generated from the prompt.

4.  Review the information in the Test Agent console.

    **Note:** The content displayed in the Test Agent console depends on the tasks specified in the prompt.

    For example, if you're executing a test, the process first looks up the sys\_id, then builds and installs the latest code. After the build succeeds, it installs the latest changes on the instance and runs the test in the background.

    **Note:** If the test succeeds, the message saying that the test passed shows up on the console.

5.  If you're creating an application, generate tests based on the business rules and conditions defined in the prompt.

    The Test Agent starts the process as mentioned in the prompt. You can then review the information in the console as mentioned in the previous step. Once the tests are created, you can run them through another prompt.

    Each test displays a message indicating whether it passed or failed.

6.  Follow the automatic triaging process if the test execution fails.

    When a test fails, the Test Agent automatically starts the troubleshooting process. It identifies the step where the failure occurred and analyzes the root cause. The Test Agent then recommends possible fixes. After you select a recommended option, the Test Agent applies the fix, updates the test code, and reruns the test automatically. When the test passes, it provides a summary of the changes made to resolve the failure.


