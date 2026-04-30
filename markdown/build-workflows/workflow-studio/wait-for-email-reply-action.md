---
title: Wait For Email Reply action
description: Pause a flow until an email reply is received to an outbound email record
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Actions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Wait For Email Reply action

Pause a flow until an email reply is received to an outbound email record

## Roles and availability

This action is a ServiceNow Core action.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Record \[Email\]**

    Data type: **Reference**

    The Email \[sys\_email\] record that you want the action to wait for a reply to.

    **Note:** The email record has to meet the following requirements to be valid:

    -   The target record field of the email has to be populated.
    -   The email record that you select must be an outbound email type such as "sent" or "send-ready." You can change the types of outbound email through the**com.glide.hub.flow\_engine.wait\_for\_email\_reply\_input\_state** system property. For more information, see [Workflow Studio flow system properties](flow-designer-system-properties.md)
-   **Enable Timeout**

    Data type: **True/False**

    Option to limit the amount of time that the flow waits for the action to be completed before continuing.

-   **Duration**

    Data type: **Duration**

    Amount of time that the flow waits before continuing when the **Enable timeout** option is selected. Enter the time to wait in hours, minutes, and seconds. If you leave this field empty, the flow doesn’t wait.

-   **Schedule**

    Data type: **Record**

    Schedule record used to compute the timeout duration when the **Enable timeout** option is selected. For example, waiting for 10 hours as part of an 8-5 weekdays schedule causes the flow to wait for one or more business days. If you leave this field empty, the timeout runs without a schedule.


## Outputs

The following outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Email Reply**

    Data type: **Record**

    The Email \[sys\_email\] record that was sent in reply to the input email record.

-   **State**

    Data type: **Choice**

    The completion status of the action as a numeric value.

    -   0 \(Success: There was an email reply\)
    -   1 \(Error: There was no email reply\)

## General Guidelines

Use these general guidelines when creating flows that wait for an email reply.

-   **Add a timeout duration for the Wait for Email Reply action**

    Add a timeout value to prevent your flow from pausing indefinitely if no reply is ever received. Use a timeout duration greater than a few hours and preferably in days. The timeout value needs to provide sufficient time for the instance to process outbound email in the "send-ready" state and also time for the instance to process inbound email replies. You can use a timeout value along with the Status output to handle cases when an email message never receives a reply. For example, you can use an If flow logic block to check for a status value of 1 and then have your flow continue based on there being no reply.

-   **Use the Email Reply output as input data for other flow actions**

    You can use the content of the Email Reply as data for another flow action. For example, you could update an Incident record with the contents of a reply or use the lack of a reply to set the state of an incident to closed.

-   **Use the Send Email action as an input**

    You can use the output of the Send Email action as the input of the Wait for Email Reply action.

-   **Emails with existing replies don’t pause the flow**

    If the email input already has an existing reply, the flow doesn’t pause on the action. In that case, the outputs are populated with a reference to the existing email reply and the flow progresses normally.


## Wait for an email reply about a resolved incident

![Example flow that waits for a reply to an incident resolved message](../images/example-wait-for-email-reply.png)

In this example flow, the flow sends an email when an incident update is resolved. The Wait For Email Reply action waits for three business days for a reply. If there’s a reply, the incident record state is updated to Work in Progress for an agent to review. If there’s no reply, the incident record is updated to the Closed state.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

