---
title: Wait For Message action
description: Pause a flow until it receives a specific message from the flow API. Specify the string message that resumes running the flow, and optionally provide a time out value to resume the flow if no message is received after a specific amount of time.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Wait For Message action

Pause a flow until it receives a specific message from the flow API. Specify the string message that resumes running the flow, and optionally provide a time out value to resume the flow if no message is received after a specific amount of time.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Message**

    Data type: **String**

    The text string that the flow is waiting to receive from the sendMessage\(\) API. The action uses this message to resume running the flow. For more information about the sendMessage\(\) API, see [FlowAPI - sendMessage\(String contextSysID, String message, String payload\)](https://www.servicenow.com/docs/access?context=ScriptableFlowAPI&version=australia&pubname=australia-api-reference&section=FlowAPI-sendMessage_S_S_S&ft:locale=en-US).

-   **Enable timeout**

    Data type: **True/False**

    Option to limit the amount of time that the flow waits for the action to be completed before continuing.

    **Note:** Use the **Enable timeout** option to help prevent the flow from infinitely waiting. If the message isn't received, a timeout value specifies when the system can skip the Wait for Message action and go to the next item in the flow. You must set a Duration value to enable a timeout.

-   **Duration**

    Data type: **Duration**

    Amount of time that the flow waits before continuing when the **Enable timeout** option is selected. Enter the time to wait in hours, minutes, and seconds. If you leave this field empty, the flow doesn’t wait.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Payload**

    Data type: **String**

    A text string returned by the sendMessage\(\) API. The parent flow can use payload values as inputs for other actions or flow logic.

-   **State**

    Data type: **Choice**

    The completion status of the action as a numeric value.

    -   0 \(success\)
    -   1 \(error\)

## General Guidelines

Use these general guidelines when creating flows that wait for a message.

-   **Convert workflow event waiting activities using this action**

    Convert classic workflows that use the Wait for WF Event activity to flows that use the Wait For Message action. You can use the event name as the message text that resumes the flow.

-   **Use the sendMessage\(\) method to create messages**

    Create messages for waiting flows using the sendMessage\(\) method. If you want the flow to generate the message to resume running, create a custom action with a Script step to generate the message. Alternatively, create some script logic that runs outside the flow such as an event to generate the message. For more information about the sendMessage\(\) API, see [FlowAPI - sendMessage\(String contextSysID, String message, String payload\)](https://www.servicenow.com/docs/access?context=ScriptableFlowAPI&version=australia&pubname=australia-api-reference&section=FlowAPI-sendMessage_S_S_S&ft:locale=en-US).


## Wait for message to run Go back to flow logic

![Execution details of the Wait for Message action in the Waiting state. The other steps of the flow are in the Not Run state.](../images/example-wait-for-message-01.png)

In this example flow, the approval state determines whether to run the Wait for Message action. If the approval state is skipped or rejected, the flow waits for a message from the sendMessage\(\) API before continuing. You could use this logic to fix a rejected approval request and resubmit it for approval.

In this example, Fred Luddy rejected the approval and requested more information. To resume the flow, someone has to address Fred's comments, and then run the sendMessage\(\) API to send the proper message `Resume Flow`.

![Execution details of the Wait for Message action in the Completed state. The payload has a runtime value of Resubmitted for approval.](../images/example-wait-for-message-03.png)

After fixing the change request, someone ran the sendMessage\(\) API to send the message `Resume Flow` and also send the flow a Payload value of `Resubmitted for approval`. For more information about the sendMessage\(\) API, see [FlowAPI - sendMessage\(String contextSysID, String message, String payload\)](https://www.servicenow.com/docs/access?context=ScriptableFlowAPI&version=australia&pubname=australia-api-reference&section=FlowAPI-sendMessage_S_S_S&ft:locale=en-US).

Since the API message value matched the conditions of the Wait for Message action, the flow resumed running. In this case, the flow used a Go back to flow logic block to rerun the Ask for Approval action.

![Example activity stream of a change record with the text Resubmitted for approval.](../images/example-payload-wait-for-message.png)

Here is the activity log of the change request. The payload value `Resubmitted for approval` was added to the **Additional comments** field.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

