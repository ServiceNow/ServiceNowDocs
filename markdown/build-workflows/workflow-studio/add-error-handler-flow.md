---
title: Add an error handler to a flow
description: Run a sequence of Workflow Studio actions and subflows to identify and correct issues that are caused by flow errors.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Flow error handler, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Add an error handler to a flow

Run a sequence of Workflow Studio actions and subflows to identify and correct issues that are caused by flow errors.

## Before you begin

Role required: flow\_designer or admin

## About this task

A flow error handler allows your flow to catch an error and run a set of actions, flow logic options, and subflows.

**Important:** A flow error handler cannot resume or restart a flow that produces an error.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Create a flow or open an existing flow.

    For more information about creating a flow, see [Create a flow in Workflow Studio](create-flow.md).

3.  Enable the ERROR HANDLER switch.

    Workflow Studio adds an error handler section to the flow and the Data pane.

4.  Add actions, flow logic options, or subflows to the Error Handler section.

    You can add up to 10 actions, flow logic options, or subflows to this section. Consider using a subflow to capture the error information or to correct issues with the record data.

    You can add flow logic options to the error handler. These options are described in the following table.

    |Flow logic option|Description|
    |-----------------|-----------|
    |If|Selectively apply one or more actions only when a list of conditions is met. For more information, see [If](../concept/flow-logic-if.md).|
    |Wait for a duration of time|Use this flow logic option to pause the flow for a specified time period and resume the flow execution after the time period elapses. For more information, see [Wait for a duration of time](../concept/flow-logic-wait-for-a-duration.md).|
    |End Flow|Use this flow logic option to stop a flow within Workflow Studio. For more information, see [End Flow](../concept/flow-logic-end-action.md).|
    |Dynamic Flow|Identify and run a flow or subflow dynamically by using runtime data. Build templates to provide expected inputs for dynamically called flows or subflows. For more information, see [Dynamic Flow](../concept/flow-logic-dynamic-flow.md).|
    |Set Flow Variables|Assign a value to one or more flow variables. Change or update a variable's value during a flow. For more information, see [Set Flow Variables](../concept/flow-logic-set-flow-variables.md).|

    The Error Status object contains the information about the flow error. You can also use the Action Status object that is returned by each action to build the conditional logic. Both of these objects are available from the Data pane.

5.  Add stages in the Error Handler.

    For more information on how to add stages, see [Configure stages and add them to a flow](add-stages.md).

6.  Add a custom action to the main body of the flow that throws an error.

    To learn how to create a custom action, see [Create a custom action to throw an error](create-custom-action-throw-error.md).

7.  Test your flow to ensure that the error handler works as expected.

    For more information about testing a flow, see [Test your flow](flow-test.md).

8.  When your flow error handling is working as expected, select the delete icon next to your custom action that throws an error to remove it from your flow.


## Result

Your flow runs the actions, flow logic options, and subflows that you specify when the flow produces an error. The flow execution details display the Completed \(error caught\) state for both the flow and the action that returned an error.

**Parent Topic:**[Flow error handler](../concept/flow-error-handler.md)

