---
title: Create Record action
description: Creates a record on any table. You can dynamically add and configure fields for the record.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Create Record action

Creates a record on any table. You can dynamically add and configure fields for the record.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Table in which to create record.

-   **Fields**

    Data type: **Template Values**

    Field values to set for the record. For example, to set the short description to a certain value, select **Short description** and set the desired value.

    To learn about creating template value input, see [Create a template value input](../task/template-value.md).

    **Important:** The system does not support updating multiple journal fields such as the additional comments or work notes of a task record.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Table**

    Data type: **Table Name**

    Table where record was created.

-   **Record**

    Data type: **Record**

    Reference to record created.


## Create a problem record from an incident record

![Create Problem Record where the Parent is set to the incident Sys ID, the Category is Network, and the Problem Statement is set.](../images/example-create-record-action.png)

In this example, the flow runs when a priority 1 network incident changes to the resolved state. The Create Record action creates a problem record where the Parent is set to the trigger incident's Sys ID, the Category is set to Network, and Problem statement is set to Determine the cause of the trigger incident's number.

![Execution details for PRB00400002, which was created from INC0000002](../images/example-create-record-action-execution-details.png)

In this example, the action creates problem record PRB00400002, which was created from INC0000002. You can use the Record runtime value to open the new record.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

