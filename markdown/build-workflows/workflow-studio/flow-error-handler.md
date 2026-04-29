---
title: Flow error handler
description: Enable flows to catch errors. Run a sequence of actions and subflows to identify and correct issues. For example, have flows log output values, send notifications, and run corrective subflows when they produce an error.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Flow error handler

Enable flows to catch errors. Run a sequence of actions and subflows to identify and correct issues. For example, have flows log output values, send notifications, and run corrective subflows when they produce an error.

## Benefits

Enable a flow error handler to gain these benefits.

-   Automate the identification of flow errors as they happen. Capture and push flow error information rather than manually search for issues caused by flow errors.
-   Automate the resolution of flow errors. Run actions and subflows to update records rather than manually updating records affected by flow errors.
-   Build your own action error handling logic. Specify when actions return an error rather than always return an error.

## Error Handler components

![Sample flow with Error Handler enabled. The Error Handler section has the Log and Send Email actions.](../images/flow-error-handler-ui.png "Error Handler user interface components")

Flow error handling consists of these components.

-   **1. Error Handler switch**

    Option to enable or disable flow error handling. When enabled, the flow displays the Error Handler section.

-   **2. Error Handler section**

    Section of flow that runs when the flow catches an error. Use this section to automate the identification and resolution of flow errors. You can add up to 10 items in this section.

    **Note:** The 10-item limit includes any combination of actions, flow logic, or subflows.

-   **3. Error Status**

    Object data pill containing details about the error caught by the flow.

-   **4. Error Status &gt; Code**

    Integer data pill indicating whether the flow produced an error. By default, a value of 1 indicates that the flow produced an error. A value of 0 indicates that the flow ran successfully. You can define your own error codes when you create a custom action.

-   **5. Error Status &gt; Message**

    String data pill containing the error message produced by the action, step, or system operation.


## Available error states

Enabling the Error Handler changes the states reported in the flow execution details. The Error Handler can produce these flow states.

-   **Completed \(error caught\)**

    State generated when the flow caught an error and successfully ran the items in the Event Handler section. The flow generates this state even when the Event Handler section is empty. This state is only available when you enable a flow Error Handler. This state is only visible from a flow execution details page. Flow context records instead display the state as **Complete**.

-   **Completed \(error skipped\)**

    State generated when a custom action continues running after a step failure. When an action generates this state, it passes it to the parent flow. This state is only available when you enable a flow Error Handler. This state is only visible from a flow execution details page. Flow context records instead display the state as **Complete**.

-   **Error**

    State generated when an error remains uncaught.

    -   An error occurs in the flow while the Error Handler is disabled
    -   An error occurs in the Error Handler section

## When an error occurs

When an error occurs in a flow with an active error handler, the flow stops running further actions and flow logic and instead runs the items in the error handler section. If the items in the error handler section run, the flow stops with the Completed \(error caught\) state. If the error handler itself generates an error, the flow stops with the Error state.

A flow cannot rerun items that generate an error or resume from the step that generated an error. You can use [Try flow logic](flow-logic-try.md) to continue running a flow that encounters an errors within the try block.

## Flow and action error handling resources

For more information about using error handling in actions and flows, see the ServiceNow® Community post [Flow and Action Error Handling Overview: Why and how to test for errors - Worfklow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-overview-why-and-how-to-test-for/ta-p/2877891).

-   [Flow and Action Error Handling Level 1: Retry and Action Error Evaluation - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-1-retry-and-action-error/ta-p/2877930)
-   [Flow and Action Error Handling Level 2: Flow Logic - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-2-flow-logic-workflow/ta-p/2877963)
-   [Flow and Action Error Handling Level 3: Flow Error Handling - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-3-flow-error-handling/ta-p/2877970)
-   [Flow and Action Error Handling Level 4: Good Practices and Summary - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-4-good-practices-and/ta-p/2877996)

## General guidelines

Follow these general guidelines to achieve the benefits offered by flow error handling.

-   **Avoid adding error handling items to the main section of the flow**

    A flow normally stops running when an action or subflow returns an error in the main section. A stopped flow cannot run any actions or subflows past the point where it returned an error. Adding error handling actions and subflows to the Error Handler section ensures they run them when there is an error.

-   **Capture Error Status information**

    The Error Status object contains information about the action that produced an error. You can use this information to identify the cause of the error as well as record data that may need correction.

-   **Suppress subflow error messages**

    You can enable the Error Handler for a subflow to prevent its errors from cascading to a parent flow. Leaving the subflow Error Handler section empty ensures that it always generates the **Completed \(error caught\)** state.

-   **Use subflows to avoid the 10-item limit**

    Rather than force your error-handling-process to fit within a 10-item limit, call subflows, which can contain many more items. You can also use the subflow outputs to trigger automation in other flows.

-   **Use subflows to take corrective actions**

    Rather than recreate the same sequence of actions in multiple flows, create reusable subflows to correct errors to your record data. When a flow error leaves your record data in an undesired state, use subflows to correct these records. You can use the error handler to identify such record data as a subflow output.


-   **[Add an error handler to a flow](../task/add-error-handler-flow.md)**  
Run a sequence of Workflow Studio actions and subflows to identify and correct issues that are caused by flow errors.
-   **[Create a custom action to throw an error](../task/create-custom-action-throw-error.md)**  
Create an action that intentionally throws an error to test flow error handling.

**Parent Topic:**[Building flows](flows.md)

**Related topics**  


[Action error evaluation](action-error-evaluation.md)

