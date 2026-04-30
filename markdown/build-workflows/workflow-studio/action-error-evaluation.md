---
title: Action error evaluation
description: Enable actions to catch step failures and continue running. Identify when specific error conditions occur and return your own action status code, status message, and error state.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create an action in Workflow Studio, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Action error evaluation

Enable actions to catch step failures and continue running. Identify when specific error conditions occur and return your own action status code, status message, and error state.

## Benefits

Enable action error evaluation to gain these benefits.

-   Catch step failures and allow an action to continue running. Specify the failure behavior of each step you add to an action.
-   Create your own error conditions. Specify when an action returns an error state as well as the status codes and messages they return.
-   Provide more error handling information and options to flow designers. Use your own action status codes and messages to identify issues and provide details for corrective actions.

## Action error evaluation step components

Each step offers these error evaluation components.

![Sample step configured to Don't stop the action and go to the next step if this step fails.](../images/action-error-evaluation-ui-01.png "Error evaluation step components")

-   **1. If this step fails option**

    Option to continue running the next step or go to error evaluation. This option has no effect on the Step Status.

-   **2. Step Status**

    Object data pill containing runtime details about the step. Each step in an action returns a Step Status.

-   **3. Step Status &gt; Code**

    Integer data pill indicating whether the step produced an error. A step returns a value of 1 when it produces an error for any reason. For example, a step can produce an error if it is missing mandatory input data or returns output in the wrong data type. A step returns a value of 0 when it runs successfully. You cannot customize these codes.

-   **4. Step Status &gt; Message**

    String data pill containing the error message produced by the step or system operation. You cannot customize the step status message.


## Action error evaluation configuration components

Action error evaluation consists of these configuration components.

![Sample Error Evaluation section with an error condition. The sample error condition returns an Action Status Code of 100 and an Action Status Message of No Incident Task Created.](../images/action-error-evaluation-ui-02.png "Error evaluation configuration components")

-   **5. Error Evaluation section**

    Section containing possible error conditions. When an action runs, it evaluates the available error conditions from top to bottom looking for a possible match. An action returns the Action Status specified by the first matching error condition. If there is no matching error condition, the Action status is set to the Step Status of the last step run.

    **Note:** Data stream actions do not have an error evaluation section.

-   **6. Add error condition option**

    Option to add an error condition. Each error condition is equivalent to an else if flow logic block. Only one error condition can be true at a time.

-   **7. Error condition configuration**

    Options available to configure an error condition.

    -   Label you want to use to identify this error condition
    -   Conditions that must be met to match this error condition
    -   Error state you want the action to return to flow
    -   Action Status Code you want the action to return to flow
    -   Action Status Message you want the action to return to flow
-   **8. Action Status**

    Object data pill containing runtime details about the action. An action always returns an Action Status.

-   **9. Action Status &gt; Code**

    Integer data pill containing the code returned by the first matching error condition or the last step run. You can return your own code when you create a custom error condition.

-   **10. Action Status &gt; Message**

    String data pill containing the message produced by a matching error condition or the last step run. You can return your own message when you create a custom error condition.


## Flow and action error handling resources

For more information about using error handling in actions and flows, see the ServiceNow® Community post [Flow and Action Error Handling Overview: Why and how to test for errors - Worfklow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-overview-why-and-how-to-test-for/ta-p/2877891).

-   [Flow and Action Error Handling Level 1: Retry and Action Error Evaluation - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-1-retry-and-action-error/ta-p/2877930)
-   [Flow and Action Error Handling Level 2: Flow Logic - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-2-flow-logic-workflow/ta-p/2877963)
-   [Flow and Action Error Handling Level 3: Flow Error Handling - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-3-flow-error-handling/ta-p/2877970)
-   [Flow and Action Error Handling Level 4: Good Practices and Summary - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-4-good-practices-and/ta-p/2877996)

## General guidelines

Follow these general guidelines to achieve the benefits offered by action error evaluation.

-   **Allow only independent steps to continue running**

    Allow a step to continue running if it does not return data required by a later step. If a step provides data necessary for later steps, then you know that the later steps cannot run successfully.

-   **Avoid more than 10 error conditions**

    While there is no limit to the number of error conditions you can create, each error condition requires evaluation. The more error conditions your action has to evaluate, the potentially slower your action can run.

-   **Identify specific step failures**

    You can use the Step Status to identify when a specific step fails. Identifying a specific step can be useful when your action contains multiple instances of the same type of step. You may also want to identify a specific step so that a flow error handler can take specific corrective actions for the failure.

-   **Put specific error conditions before general error conditions**

    Error evaluation stops when the action finds a matching error condition. Putting general error conditions first may prevent the action from ever matching specific error conditions.

-   **Use descriptive error condition labels**

    Identify an error condition without having to edit it. By default, you can only see error conditions when you edit them.


-   **[Add error condition](../task/add-error-condition.md)**  
Enable an action to return custom status information when specific conditions are met. Specify whether a flow considers your custom action status as an error or a successful run.

**Parent Topic:**[Create an action in Workflow Studio](../task/create-action.md)

