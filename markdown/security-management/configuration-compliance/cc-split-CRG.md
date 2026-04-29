---
title: Split a remediation task
description: From an existing remediation task in the Configuration Compliance application, identify a subset of test results that you want to move to a new Remediation Task.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Split a remediation task

From an existing remediation task in the Configuration Compliance application, identify a subset of test results that you want to move to a new Remediation Task.

**Important:** As an admin and a remediation owner, you can split a remediation task from the [Vulnerability Manager Workspace](../../vulnerability-response/concept/vr-ws-exceptions-split-VMGR-ws.md) and [IT Remediation Workspace](../../vulnerability-response/task/vr-ws-split-task.md) respectively.

## Before you begin

Role required: a user with the itil role

## About this task

As an IT or remediation specialist, you can split existing remediation tasks in the **Open**, **Under Investigation**, or **Awaiting Implementation** states with more than one test result. By creating a new Remediation Task with test results that match specific criteria, you can work with a specific group of test results without impacting the original remediation task.

When you specify the conditions for the test results that you want to move to a new remediation task with the condition builder, only the active test results that match your criteria are moved to the new task. You are not required to create change requests \(CHGs\) when you split a remediation task. You have the option to split a remediation task at the same time you create a change request, or, you can split a remediation task without creating a change request.

The following image illustrates the basic flow for splitting a remediation task. The detailed steps for this flow follow the image.

![States for splitting a Remediation Task and move test results to another remediation task](../image/CC-Split-CRG-01.png "Flow for splitting a remediation task")

Use cases for splitting test results from existing Remediation Tasks into new tasks might include the following examples:

-   When you want to create a change request or change requests for a split task.
-   When you reassign a split task to another user in your assignment group.
-   When you request a deferral or exception for a split task because you know that some test results on specific configuration items \(CI\) cannot be remediated in a given time frame.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Tests** &gt; **Remediation Tasks** &gt; **My Open Tasks**.

    The list of Remediation Tasks assigned to your groups is displayed.

2.  In the Number column, click the remediation task that you want to split.

    The Remediation Task record is displayed.

3.  To create a subset of test results for a new task that matches specific criteria, follow these steps.

    On the upper right of the record, click **Split Task**.

    You might prefer this method of creating a new remediation task if you are working from a large group with multiple test results.

    The Split remediation task form is displayed.

4.  With the condition builder displayed, specify the conditions for the test results that you want to move to a new remediation task.

    For example, you may prefer to filter out only test results that match the following conditions:

    -   In the **Open** state.
    -   Risk scores greater than 75.
    -   Result is **Failed**.
    If test results match your filter after you enter the conditions, a message is displayed with the number of test results that match.

    If a message is displayed that no test results match your filter, or, that all your test results match your criteria, adjust the conditions so at least one test result matches your filter criteria.

5.  Click **Preview items** to view the matched test results.

    A new window, Remediation Tasks, displays the items.

6.  To preview details about the test results that match your filter criteria, follow these steps before you click **Split Task** to create the new group.

    These details include the assignment group and who the test result is assigned to. Viewing this information on the preview may help ensure that the new task is properly assigned.

    1.  With the Remediations list displayed in the preview, click an item in the Result column.

        The Test Result record is displayed.

    2.  Verify the **Assignment group** and **Assigned to** fields are correct.

    3.  Click **Update**.

7.  When you are ready to create the new remediation task, click **Split Task**.

    A message indicates the number of test results that are moved to the new remediation task, and the new remediation task is displayed. To help you identify the new task, you might prefer to edit the text in the **Short description** field and edit the Assignment group or Assigned to fields again, if required.

    **Note:** For under 200 test results, the split operation is done synchronously, and the test results are displayed in the new task.

    For over 200 test results, the split operation is done asynchronously in the background, and it may take a few seconds for the test results to appear in the new task. The following message is also displayed: `n test results will be moved from TRGxxxxxxx to new remediation task GRCxxxxx shortly.`

8.  Alternatively, you can create a new remediation task by selecting test results directly from the Test Results related list on a remediation task.

    You might prefer this method if you have only a few test results in a remediation task, or you know exactly which tests you want to move to a new remediation task.

    1.  With the remediation task record displayed, scroll to the Test Results related list.

    2.  In the far left column, select check boxes for the test results you want to create a new remediation task for.

    3.  From the Actions on selected rows list in the lower left of the record, click **Split Task**.

    4.  In the Split remediation task form that is displayed, to help you identify the new group, you might prefer to edit the text in the **Short description** field.

    5.  Click **Split Task**.

        A message indicates the number of test results that have moved to the new task, and the new remediation task is displayed.

        After the change request for this remediation task is resolved, if there are no other open change requests associated with this remediation task, the remediation task is also moved to the **Resolved** state.

        **Note:** You can still manually move change requests and remediation tasks through the states of their life cycles on their respective records with state synchronization enabled, but when the system registers that a change request has changed its state, or you add a change request or remove it from a remediation task, state synchronization potentially can override your manual intervention. However, change requests states do not automatically move the remediation task from the `Closed` or `Deferred` states.

        For more information, see [State synchronization between change requests and remediation tasks](cc-cr-state-synch.md).


## What to do next

You can create or associate change requests for your new remediation tasks. For more information, see [Associate a remediation task to an existing change request](cc-CR-v12-assoc.md) and [Create a change request in Configuration Compliance](cc-CR-v12-create.md).

