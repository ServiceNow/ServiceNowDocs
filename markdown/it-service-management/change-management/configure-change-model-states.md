---
title: Configure change model states
description: Configure states for change models and define transition between multiple states.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# Configure change model states

Configure states for change models and define transition between multiple states.

## Before you begin

Role required: change\_manager

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models**.

2.  Select the change model for which you want to define states.

3.  Navigate to **Model States**.

4.  Select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |State|State that you want to include in your model.|
    |Initial State|Option to enable this state as the initial state for your model. This field is automatically selected when you add the first state to your model.|

6.  Save the state and return to the Change Model form by selecting **Submit**.

7.  Add a transition between the available states by selecting the display/hide hierarchical lists icon \(![](../image/display-hide-hierarchial-lists.png)\) for the model state that you want to apply the transition to.

    1.  Select **New**.

        The Model State Transitions page is displayed.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |From|State that the change request is moving from.|
        |To|State that the change request is moving to.|
        |Automatic Transition|Option for enabling automatic transition to the change request when the defined conditions are met. Selecting this option also helps prevent you from manually selecting the **State** field on the change request form.|

    3.  Select the form context menu icon \(![](../image/form-context-menu.png)\) and select **Save**.

    4.  Select **New** to add conditions for transition between states.

    5.  On the form, fill in the fields.

<table id="table_jdx_tpy_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the condition.

</td></tr><tr><td>

State Transition

</td><td>

This field is automatically set to the state that you're applying the condition to.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the condition.

</td></tr><tr><td>

Requires

</td><td>

Condition for your transition.The available options are:

-   **Mandatory Fields**:Requires specified fields to be populated before the model state transitions.
-   **Transition Condition**: Enables you to define a more granular condition.

For more information, see [Create predefined conditions](create-predefined-transition-condition-type.md).

</td></tr><tr><td>

Condition \(condition builder\)

</td><td>

Condition that must be fulfilled to enable the state transition.This field is available only when **Transition Condition** is selected from **Requires** field.

</td></tr><tr><td>

Condition \(script\)

</td><td>

Script that must be fulfilled to enable the transition. The script returns a value of **True** when passed.

</td></tr><tr><td>

Active

</td><td>

Option to make the condition active.

</td></tr></tbody>
</table>    6.  Select **Save**.


**Parent Topic:**[Create a Change model](create-a-change-model.md)

