---
title: Test a subflow
description: You can test a subflow alone, or when added to a flow. When testing a subflow alone, you must define the inputs that the subflow uses in its actions. Because a subflow does not have a trigger, testing a subflow runs the actions using the defined input values. Unless updated, subsequent tests use the same inputs defined in the initial test run.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Building subflows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Test a subflow

You can test a subflow alone, or when added to a flow. When testing a subflow alone, you must define the inputs that the subflow uses in its actions. Because a subflow does not have a trigger, testing a subflow runs the actions using the defined input values. Unless updated, subsequent tests use the same inputs defined in the initial test run.

## Before you begin

[Create a subflow in Workflow Studio](create-subflow.md) that contains at least one action and save it. Workflow Studio only tests saved subflows that contain at least one action.

Role required: flow\_designer or admin

## About this task

Because testing a subflow creates or changes records on the instance, flow designers should always test subflows on a non-production instance containing relevant demonstration data.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click the subflows tab and open a saved subflow.

3.  Click **Test**.

    The Test Subflow dialog opens.

4.  Define input values for the subflow to use in its actions.

    The values defined are remembered on future test runs.

5.  Click **Run Test**.

    **Note:** Select the **Run test in background** option to test a subflow asynchronously in the background.

    If you select the **Run test in background** option, the execution details are displayed only after the execution is completed asynchronously in the background. Also, the execution details are associated with the subflow only after execution is completed.

6.  After the flow executes, click **Subflow has been executed. To view the subflow, click here**.

    The Execution Details open.


## What to do next

Review the [Flow execution details](../concept/flow-execution-details.md).

Once the subflow behaves as desired, you can [publish the subflow](publish-subflow.md) and add it to a flow.

**Parent Topic:**[Building subflows](../concept/subflows.md)

