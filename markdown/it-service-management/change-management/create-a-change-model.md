---
title: Create a Change model
description: Create change models to configure the states and transitions to match your organization's change processes.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Create a Change model

Create change models to configure the states and transitions to match your organization's change processes.

## Before you begin

Role required: change\_manager

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ijj_ytc_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name the change model based on the process associated with the change model. For example, the following change models can be created for the traditional types of ITIL changes:-   Normal
-   Standard
-   Emergency


</td></tr><tr><td>

Default Change Model

</td><td>

Option for enabling the change model as a default model on the change request form.

</td></tr><tr><td>

Active

</td><td>

Option for making the model available for selection when creating a change request.

</td></tr><tr><td>

Color

</td><td>

Color that appears on the side of the change model bar on the **Models** tab in the change landing page.

</td></tr><tr><td>

Available in 'Create New'

</td><td>

Option for enabling that this model for selection on the **Models** tab on the change landing page and in the **Model** field on the change request form.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the change model.

</td></tr><tr><td>

Implementation states

</td><td>

Implementation state for the change model. For more information on states, see [Legacy: State model and transitions](../concept/c_ChangeStateModel.md).If you are using Mass CI Update with change models, verify that the **Implementation states** field in the model is set to the state in which you want the changes to take effect.

</td></tr></tbody>
</table>4.  In the **Security** tab, fill in the fields.

<table id="table_dyx_l11_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Advanced Security

</td><td>

Option to enable role-based access controls and user criteria to tailor the Change creation landing page views. When you enable Advanced Security, the **Not Available For**, **Available For**, and **Can Write** tabs appear next to the **Model States** tab in the related lists.For more information on managing user access to the change model, see [Create a user criteria record for Change Management](create-user-criteria.md).

</td></tr><tr><td>

Available For

</td><td>

Users with access to the change model.

</td></tr><tr><td>

Not Available For

</td><td>

Users with no the access to the change model

</td></tr><tr><td>

Can Write

</td><td>

Users with editable access to the change model

</td></tr><tr><td>

Read Roles

</td><td>

Roles that can view the change model.

</td></tr><tr><td>

Write Roles

</td><td>

Roles to edit the change model.

</td></tr></tbody>
</table>5.  Provide standard information for specific fields to be available for a new change request created using the model.

    If you set a preset for the model, the value becomes read-only for change records created using the model.

    1.  In the **Preset Management** tab, select the **Apply record preset** check box.

    2.  Select the record preset from the list, and then select the relevant option for the chosen preset.

    3.  Select the fields from the list, and then select the relevant value for the chosen field.

    4.  Select **Submit**.

6.  In the **Template Management** tab, provide information regarding the change templates associated with the change model.

<table id="table_wr2_xb1_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Who can propose Templates

</td><td>

Users allowed to propose templates using this change model. The available options are:-   Anyone who can modify this model
-   Anyone who can read this model


</td></tr><tr><td>

Template approval users

</td><td>

Users who can approve templates proposed using this change model.

</td></tr><tr><td>

Template approval groups

</td><td>

User groups that can approve templates created using this change model.

</td></tr></tbody>
</table>7.  Select **Submit** to save the change model with the details provided.


## What to do next

[Configure change model states](configure-change-model-states.md).

[Create and propose a change template](create-change-template.md).

[Configure template categories](configure-template-categories.md).

-   **[Configure change model states](configure-change-model-states.md)**  
Configure states for change models and define transition between multiple states.
-   **[Create predefined transition condition types](create-predefined-transition-condition-type.md)**  
Create predefined transition conditions to reuse the conditions for your change models.
-   **[Attach a process for Change model states](../concept/attach-process-change-model.md)**  
You can attach a process with defined conditions to the Change model states to enable state transitions.
-   **[Create and propose a change template](create-change-template.md)**  
Create, customize, and then propose for publication a change template aligned to a change model to make change creation faster, and promote data quality and consistency.

**Parent Topic:**[Configuring Change Management](../concept/configure-change-management.md)

