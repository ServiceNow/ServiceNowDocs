---
title: Add Worknote Link to Context action
description: Add a journal field entry containing a link to the current flow context record. Use the link to view the flow execution details of the current flow. You can add a flow context link to any record that has a journal field.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Add Worknote Link to Context action

Add a journal field entry containing a link to the current flow context record. Use the link to view the flow execution details of the current flow. You can add a flow context link to any record that has a journal field.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Table name containing the record you want to update with a link.

-   **Record**

    Data type: **Record**

    Record where you want to add a link to the flow execution details. You can use the [Look Up Record action](lookup-record-flow-designer.md) to find an appropriate record.

-   **Journal Field**

    Data type: **Field Name**

    Journal field to insert the link to the flow execution details. For example, the work notes field of a task record.


## Outputs

This action has no outputs. Instead it updates the selected record to add a direct link to the flow execution details for the flow that ran this action.

## Add a link to an incident record

![Configuration of the Add Worknote Link to Context](../images/example-add-worknote-link-to-context-action.png)

In this example, a flow runs when an priority 1 incident is created in the Network category. The Update Record action assigns the incident to the Network assignment group. The Add Worknote Link to Context action updates the trigger incident record. The action adds the link to Work notes journal field.

![Execution details of the Add Worknote Link to Context](../images/example-add-worknote-link-to-context-execution-details.png)

The execution details show that the trigger incident record INC008112 was updated to add a link to the work notes field.

![Incident record with a link to the flow execution details for the Demo Add Worknote Link to Context flow](../images/example-add-worknote-link-to-context-record-link.png)

The incident record work notes field contains a text message and a link to the flow execution details for the flow.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

