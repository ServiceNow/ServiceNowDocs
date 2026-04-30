---
title: Configure the Financial Services Operations Integration with Guidewire
description: Use this procedure to select and configure the Financial Services Operations Integration with Guidewire application.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Configure the Financial Services Operations Integration with Guidewire

Use this procedure to select and configure the Financial Services Operations Integration with Guidewire application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  To customize the connection configuration, navigate to **Flow Designer** &gt; **Connections**.

    There are three connections for Guidewire:

    -   Guidewire ClaimCenter
    -   Guidewire PolicyCenter
    -   Guidewire ContactManager
    Select one of these connections and follow the instructions described in [Set up Guidewire spoke](https://www.servicenow.com/docs/access?context=set-up-guidewire-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) to update the connection configuration.

3.  Select the **Subflows** tab.

4.  If you have installed:

    -   Personal Lines Claims, search for **Get Personal Auto Claim** in the Name field.
    -   Commercial Lines Claims, search for **Get Commercial Auto Claim** in the Name field.
5.  Locate the flow from the list and open it.

    For information about subflows, see [Financial Services Operations Integration with Guidewire subflows](../reference/fso-guidewire-integration-subflows.md).

6.  Select **Test**.

    The Test Subflow dialog opens.

    Define the input values for the subflow to use in its actions. The values that you define are automatically filled in on future test runs.

7.  Select **Run Test**.

    **Note:** Select the **Run test in background** option to test a subflow asynchronously in the background. If you select the option, the execution details are displayed only after the execution completes asynchronously in the background. Also, the execution details are associated with the subflow only after execution completes.

8.  After the flow executes, select **Your test has finished running. View the subflow execution details.**.

    The Execution Details open.


**Parent Topic:**[Financial Services Operations Integration with Guidewire](../concept/fso-integration-with-guidewire-landing-page.md)

