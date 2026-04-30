---
title: Create a Change model
description: Depending on your requirements, you can create a Change model and configure the states and transitions for a specific use case.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Create a Change model

Depending on your requirements, you can create a Change model and configure the states and transitions for a specific use case.

## Before you begin

Role required: change\_manager

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ijj_ytc_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the Change model.

</td></tr><tr><td>

Default Change Model

</td><td>

Option for enabling the Change model as a default model on the Change request form.

</td></tr><tr><td>

Active

</td><td>

Option for enabling that this model is available for selection when creating a Change request.

</td></tr><tr><td>

Color

</td><td>

Color that appears on the left side of the Change model bar on the **Models** tab in the Change landing page.

</td></tr><tr><td>

Available in 'Create New'

</td><td>

Option for enabling that this model is available for selection on the **Models** tab on the Change landing page. Also, the model will be available to select in the **Model** field on the Change request form.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the Change model.

</td></tr><tr><td>

Implementation states

</td><td>

Implementation state for the Change model. For more information on states, see [State model and transitions](../concept/c_ChangeStateModel.md).If you are using Mass CI Update with Change Models ensure the Implementation states field in the model is set to the state in which you want the changes to take effect.

</td></tr><tr><td>

Record Preset

</td><td>

Preset values for all changes using this model.

</td></tr><tr><td>

Advanced Security

</td><td>

Option to enable role-based access controls and user criteria to tailor the Change creation landing page views. When you enable Advanced Security, **Available For**, **Not Available For**, and **Can write** tabs appear next to **Model States** tab.

</td></tr><tr><td>

Read Roles

</td><td>

Option to define the roles to view the Change model.

</td></tr><tr><td>

Write Roles

</td><td>

Option to define the roles to edit the Change model.

</td></tr></tbody>
</table>4.  Click the form context menu icon \(![Form context menu icon.](../image/form-context-menu.png)\) and select **Save**.

    The Model States context menu appears. You can select the states for your Change model.

5.  Click **New**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |State|State that you want to include in your model.|
    |Initial State|Option to enable this state as the initial state for your model. This field is automatically selected when you add the first state to your model.|

7.  To save the state and return to the Change Model form, click **Submit**.

8.  To add a transition between the states, click the display/hide hierarchical lists icon \(![Display/hide hierarchical lists icon.](../image/display-hide-hierarchial-lists.png)\) for the model state that you want to apply the transition to.

    The Model State Transitions context menu appears.

9.  Click **New**.

10. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |From|State that the Change request is moving from.|
    |To|State that the Change request is moving to.|
    |Automatic Transition|Option for enabling automatic transition to the Change request when the defined conditions are met. Selecting this option also prevents you from manually selecting the **State** field on the Change request form.|

11. Click the form context menu icon \(![Form context menu icon.](../image/form-context-menu.png)\) and click **Save**.

    The Model State Transition Condition context menu appears.

12. Click **New**.

13. On the form, fill in the fields.

<table id="table_ybk_z2v_znb"><thead><tr><th>

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

State that you're applying the transition condition to. This field is automatically set with the state that you're applying the condition to.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the condition.

</td></tr><tr><td>

Requires

</td><td>

Condition for your transition. You can select a pre-defined condition, such as **Mandatory Fields** to require that specified fields are populated before the model state transitions, or select **Transition Condition** to define a more granular condition.

To create pre-defined conditions, see [Create predefined conditions](create-predefined-transition-condition-type.md).

</td></tr><tr><td>

Condition \(condition builder\)

</td><td>

Condition on the Change request that must be fulfilled to enable the transition.

</td></tr><tr><td>

Condition \(script\)

</td><td>

Script that must be fulfilled to enable the transition. The script returns a value of **True** when passed.

</td></tr><tr><td>

Active

</td><td>

Option to make the condition active.

</td></tr></tbody>
</table>14. Click **Submit**.

15. Select **Available For** tab.

16. Select **New** to add the list of users who can access the Change model

17. On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the user criteria record.|
    |Active|Option to make the condition active.|
    |Users|Option to select the users who can access the Change model.|
    |Groups|Option to select the groups who can access the Change model.|
    |Roles|Option to select the role who can access the Change model.|
    |Companies|Option to select the companies who can access the Change model.|
    |Locations|Option to select the location of the company who can access the Change model.|
    |Departments|Option to select the departments who can access the Change model.|
    |Match All|Option to use the Change model if it meets all conditions in the user criteria.|
    |Advanced|Option to create a script to meet the condition for user criteria.|

18. Select **Submit**.

19. Manage the users to access the change model by providing the user access in **Not Available For**, **Available For**, and **Can Write** tabs:

    -   **Available For** – Provides the access for the change model
    -   **Not Available For** – Doesn’t provide the access for the change model
    -   **Can Write** – Provides the editable access to the change model
    For more information on user access, refer [Create a user criteria record for Change Management](create-user-criteria.md).

20. Select **Submit**.


-   **[Create predefined transition condition types](create-predefined-transition-condition-type.md)**  
Create predefined transition conditions to reuse the conditions for your Change models.
-   **[Attach a process for Change model states](../concept/attach-process-change-model.md)**  
You can attach a process with defined conditions to the Change model states to enable state transitions.

**Parent Topic:**[Configuring Change Management](../concept/configure-change-management.md)

