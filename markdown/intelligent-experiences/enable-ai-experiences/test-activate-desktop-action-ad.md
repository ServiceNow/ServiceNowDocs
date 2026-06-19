---
title: Test and activate a desktop action in AI Desktop Actions
description: Test the desktop action and then activate it so that it’s available as a tool in the AI Agent Studio. You can add this tool to the AI agents that execute desktop actions in your desktop environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/test-activate-desktop-action-ad.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-05-22"
reading_time_minutes: 5
breadcrumb: [Design defined-path desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Test and activate a desktop action in AI Desktop Actions

Test the desktop action and then activate it so that it’s available as a tool in the AI Agent Studio. You can add this tool to the AI agents that execute desktop actions in your desktop environment.

## Before you begin

-   Capture your automation steps. For more information, see [Automate repetitive tasks by recording steps with AI in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/record-with-ai-ad.md), [Automate repetitive tasks by auto-capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/auto-create-desktop-action-ad.md), or [Extend a desktop action by manually capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/manual-create-desktop-action-ad.md).
-   Configure the properties for screens, anchors, and steps. For more information, see [Screen, anchor, and step properties in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/screen-anchor-and-action-properties-ad.md).
-   Add desktop action details, such as name, description, and associated applications, and review inputs and outputs. For more information, see [Add details to desktop actions in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/add-details-desktop-action-ad.md).

Role required: sn\_aia.admin

## About this task

You can test the desktop action before you activate it. You can also test individual screens to quickly identify and troubleshoot issues.

Execution workspace is launched to run and test the selected screen orthe desktop action.

\[Omitted image "execution-workspace-ad.png"\] Alt text: AI Desktop Actions showing the Shipping Management app with fields on a Windows 10 background.

After you run the test by entering the required inputs manually, test results are shown either for a screen orfor entire desktop action in the Execution workspace. While running tests, if you do not see the Execution workspace coming forth, switch to the Execution workspace manually.

While working on a desktop action, the test values you enter are retained across test runs until you close the desktop action or reset the test values.

## Procedure

1.  From the desktop action header, select **Test**.

2.  Option 1: Run the screen-level test.

    1.  In the Test modal, enter required inputs for the screen that you want to test.

    2.  Select **Test screen**.

        The Execution workspace is launched.

    3.  Enter the Windows Security credentials.

        Observe the test run in the Execution workspace.

        **Note:** If any pop up is blocking the automation from running, step in to clear the pop up so that you can see the test run in the Execution workspace.

    4.  After the test run is complete, check the status in the Test modal.

        -   If test is successful, proceed with testing the next screen.

            \[Omitted image "ad-sucess-test-desktop-action-scrn.png"\] Alt text: Test completed window displaying status as Success.

        -   If test isn’t successful, fix the issue highlighted in the error message and run the screen-level test again.

            \[Omitted image "ad-fail-test-desktop-action-scrn.png"\] Alt text: Test completed window displaying status as Failed.

    5.  Reset test data by selecting **Reset**.

    6.  Cancel running test by selecting **Cancel**.

3.  Option 2: Run the Desktop action-level test.

    1.  In the Test modal, enter the required input values in the desktop action.

        -   **Show inputs** - Shows all the required input fields.
        -   **Show all** - Shows all fields.
    2.  Select **Run test**.

        The Execution workspace is launched.

    3.  Enter the Windows Security credentials.

        Observe the test run in the Execution workspace.

        **Note:** If any pop up is blocking the automation from running, step in to clear the pop up so that you can see the test run in the Execution workspace.

    4.  After the test run is complete, check the status in the Test modal.

        -   If test is successful, proceed with activating the desktop action.

            \[Omitted image "ad-sucess-test-desktop-action.png"\] Alt text: Test completed window displaying status as Success.

        -   If test isn’t successful, select **Back to Test** to check the configuration and run the test again.

            \[Omitted image "ad-fail-test-desktop-action.png"\] Alt text: Test completed window displaying status as Failed.

4.  Cancel running test by selecting **Cancel**.

5.  After a successful completion of the desktop action test and when you're satisfied with the result, select **Activate** to publish the desktop action in AI Agent Studio.

    **Important:** If you recorded the desktop action using [Record with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/record-with-ai-ad.md), an alert appears if any screens have failed anchors. Resolve the issues before activating to verify reliable automation at runtime.

    The **Activate** button sets the desktop action as active or inactive. Only the activated on-screen desktop actions can be selected from the drop-down in AI Agent Studio.

    **Note:** After activation, save the desktop action to make it available as a tool in AI Agent Studio.


If you get en error that the file size is beyond 10 MB, you can increase the file size in a payload by creating system properties in the ServiceNow instance. For more information, see [Increase payload limit through system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/increase-payload-limit-ad.md).

## What to do next

Create an AI agent. For more information, see [Creating AI agents for AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/create-ai-agents-ad.md).

Enable AI agents to perform desktop actions by adding desktop actions as tools. For more information, see [Add a defined desktop action tool to an AI agent for desktop and web-based task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/add-desktop-action-ai-agent.md).

