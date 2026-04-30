---
title: Get Latest Response Text From Email step
description: Provide the most recent reply or forward message in an e-mail chain to other steps in your action.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Get Latest Response Text From Email step

Provide the most recent reply or forward message in an e-mail chain to other steps in your action.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Inputs

Provide a value for each input that your step needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

|Input|Data type|Description|
|-----|---------|-----------|
|Email Record|Record|Email record whose most recent reply or forward message you want to provide to other steps in your action. Select an Email \[sys\_email\] record from the list, or add an Email \[sys\_email\] record data pill from the Data panel.|

## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your action.

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

Body text for the most recent reply or forward message in the Email \[sys\_email\] record that you selected for the step's input.**Note:** If you select an Email \[sys\_email\] record with a Type of New for this step's input, the Latest Response Text output will be the entire body text of the e-mail.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

