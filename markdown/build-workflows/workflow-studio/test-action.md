---
title: Test an action
description: Test an action before publishing it for other users.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an action in Workflow Studio, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Test an action

Test an action before publishing it for other users.

## Before you begin

-   [Create an action](create-action.md) and save it.
-   Role required: flow\_designer, flow\_operator, action\_designer, or admin.

## About this task

A user with the flow\_designer role should always test actions on non-production instances containing relevant demonstration data because testing an action creates or changes records on the instance.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click the **Actions** tab and select the action that you want to test.

3.  Click **Test**.

    The system displays the Test Action dialog box.

4.  Fill in the fields for the action.

    **Note:** Complete all mandatory fields in the Test Action dialog box.

5.  Click **Run Test**.

    **Note:** Select the **Run test in background** option to test an action asynchronously in the background.

    If you select the **Run test in background** option, the execution details are displayed only after the execution is completed asynchronously in the background.


## What to do next

Click `Action has been executed. To view the action, click here` to view the action execution details. See [Flow execution details](../concept/flow-execution-details.md) for information about the executions.

**Note:** Users must have the flow\_operator or admin role to view the executions.

**Parent Topic:**[Create an action in Workflow Studio](create-action.md)

