---
title: Test a flow
description: Before activating a flow so other users can access it, test to make certain it works the way you expect.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Test a flow

Before activating a flow so other users can access it, test to make certain it works the way you expect.

## Before you begin

Role required: flow\_designer or admin

## About this task

Testing a flow bypasses the flow trigger conditions to run it with the test data you provide. For example, testing a flow with a record **Created** trigger causes the system to act as if the selected record was created. For a list of data pills available by trigger type, see [Workflow Studio flow trigger types](../reference/flow-triggers.md).

**Note:** Because testing a flow creates or changes records on the instance, flow designers should always test flows on a non-production instance containing relevant demonstration data.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**, then double-click the row for the flow you want to test.

2.  Save the flow.

3.  Select **Test**.

    The system displays the Test flow dialog. The contents of the Test flow dialog depend on the type of trigger.

4.  If the flow has a record trigger, create or select a record to use for the test.

    To create a record, select the **Create new record** button ![Create new record button](../images/add-record-button.png).

5.  If the flow has a record **Updated** or **Created or Updated** trigger, specify which fields and values changed in the update.

    To specify a field value change, select the **Create new changed field** button ![Create new changed field button](../images/add-changed-field-button.png) for each field whose value you want to change. Complete the changed field details for each changed field.

    |Field|Description|
    |-----|-----------|
    |Field Name|The field updated by the test.|
    |Previous Value|The field value prior to the update.|
    |Current Value|The field value after the update.|
    |Previous Display Value|The field display value prior to the update.|
    |Current Display Value|The field display value after the update.|

6.  Select **Run Test**.

    **Note:** Select the **Run test in background** option to test a flow asynchronously in the background.

    The system tests the flow.

7.  Select **Your test has finished running. View the flow execution details**.

    **Note:** This link is created irrespective of your choice for the **Run test in background** option. If you have selected the **Run test in background** option, the execution details are displayed only after the execution is completed asynchronously in the background. Also, the execution details are associated with the flow only after execution is completed.

    The system displays the flow execution details for the test.


## What to do next

Review the [Flow execution details](../concept/flow-execution-details.md).

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

