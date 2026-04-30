---
title: Fire Event action
description: Create a system event record in the Event \[sysevent\] table to be processed by a scheduled event handler. Pass event parameters using flow data.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Fire Event action

Create a system event record in the Event \[sysevent\] table to be processed by a scheduled event handler. Pass event parameters using flow data.

## Roles and availability

Available as a ServiceNow Core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Event \[Event Registration\]**

    Data type: **Reference.Event Registration\[sysevent\_register\]**

    Event Registration record that defines the type of system event that you want to create.

-   **Record**

    Data type: **Record**

    Sys ID of the record that triggered the event.

-   **Table**

    Data type: **Table Name**

    Table containing the record that triggered the event.

-   **Parameter 1**

    Data type: **String**

    Text input to specify the first event parameter.

-   **Parameter 2**

    Data type: **String**

    Text input to specify the second event parameter.


## Outputs

This action has no outputs.

## Fire an incident escalated event

![Field values used to fire the incident.escalated event.](../images/example-fire-event-action.png)

This example creates an incident.escalated event when an incident record is updated to change the value of the Escalation field. The incident.escalated event expects the value of parameter 1 to be the current value of the Escalation field and parameter 2 to be the previous value of the Escalation field.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

