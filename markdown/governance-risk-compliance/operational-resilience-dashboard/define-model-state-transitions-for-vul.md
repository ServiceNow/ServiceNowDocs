---
title: Define the state transitions model
description: Define the model state transitions and conditions to control how a vulnerability traverses through the different workflow states.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up the State model and Action task model, Setting up the Operational vulnerability module, Completing general administrative tasks, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Define the state transitions model

Define the model state transitions and conditions to control how a vulnerability traverses through the different workflow states.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

The workflow states set up within the state model are shown on the stepper component overview page. Refer to the following setup to configure the stepper component:

1.  Display type: Specify whether the state should appear as **As Node** or **As sub-level**.
2.  Stepper label: This label is displayed on the stepper component for each state.
3.  Parent node: If the display type for the state is set to **As sub-level**, then define the state that will act as the parent node for this sub-level.

## Procedure

1.  Navigate to **All** &gt; **Operational Vulnerability** &gt; **State Models**.

2.  To add a new workflow state, select **New** in the State label column.

3.  On the form, fill in the fields.

<table id="table_ok4_tfv_kvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

Name of the workflow state. Choices is: **New**

</td></tr><tr><td>

Model

</td><td>

State model that uses this workflow state. This field is automatically set to the state model name.

</td></tr><tr><td>

Display type

</td><td>

Display type of the workflow state. Choices are the following:-   **As node**: Display as a parent state.
-   **As sub-level**: Display as a sub-state of the parent state.


</td></tr><tr><td>

Stepper label

</td><td>

Label to be displayed on the stepper component for the state. This field is automatically set to the state.

</td></tr><tr><td>

Is optional

</td><td>

Option to select the state as optional. This field appears only when **As node** is selected from the **Display type** field.

</td></tr></tbody>
</table>4.  Select **Update**.

    The example shows the Assessment state. The Model State Transitions and State Model Attributes related lists are displayed.

5.  To update the model state transition from the Model State Transitions related list, select it from the display name column in the GRC workflow states list.

    ![State model.](../image/vul-state-model.png)

6.  To add the model state transition, select **New** on the Model State Transitions context menu.

    The Model State Transitions context menu is shown in the example.

    ![Model State Transitions.](../image/op-vul-workflow-states.png)

    The Model State Transition New record is displayed.

    ![Model State Transition record.](../image/model-state-transition-record.png)

7.  On the Model State Transition record form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |From|Name of the state. This field is automatically set to **State \[state\]**.|
    |To|State that you want to move to from the selected state|
    |Automatic transition|Option to enable the automatic transition of the workflow state.|

8.  Select **Submit**.

    The newly added Model State Transition is displayed in Model State Transitions related list.


