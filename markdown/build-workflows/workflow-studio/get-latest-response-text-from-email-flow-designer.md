---
title: Get Latest Response Text From Email action
description: Provide the most recent reply or forward message in an e-mail chain to other actions in your flow.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Get Latest Response Text From Email action

Provide the most recent reply or forward message in an e-mail chain to other actions in your flow.

## Roles and availability

-   Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

|Input|Data type|Description|
|-----|---------|-----------|
|Email Record|Record|Email record whose most recent reply or forward message you want to provide to other actions in your flow. Select an Email \[sys\_email\] record from the list, or add an Email \[sys\_email\] record data pill from the Data panel.|

## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

<table id="table_g5q_jxh_knb"><thead><tr><th>

Output

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Latest Response Text

</td><td>

String

</td><td>

Body text for the most recent reply or forward message in the Email \[sys\_email\] record that you selected for the action's input.**Note:** If you select an Email \[sys\_email\] record with a Type of New for this action's input, the Latest Response Text output will be the entire body text of the e-mail.

</td></tr></tbody>
</table>**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

