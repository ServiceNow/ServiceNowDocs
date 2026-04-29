---
title: Interaction form
description: The Interaction form displays information about a customer interaction.
locale: en-US
release: australia
product: Interaction Management
classification: interaction-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Interaction wrap up, Configuring Interaction Management, Interaction Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Interaction form

The Interaction form displays information about a customer interaction.

The interaction form includes the following fields.

<table id="table_aqy_gm2_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically assigned interaction number.

</td></tr><tr><td>

Type

</td><td>

The type of customer interaction, such as a chat or phone call.

</td></tr><tr><td>

Account

</td><td>

The name of the customer contact's company. This field is filled in automatically if the information is available in the contact record.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact.

</td></tr><tr><td>

Consumer

</td><td>

The name of the consumer.

</td></tr><tr><td>

State

</td><td>

The current state of the interaction. For more information, see [Interaction states](interaction-states.md#section_o4v_j4r_vdb).

</td></tr><tr><td>

Assigned to

</td><td>

The name of the assigned user.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the customer issue.

</td></tr><tr><td>

Work notes

</td><td>

Records information about the interaction and the work being done to resolve the customer issue.

</td></tr><tr><td>

Wrap up duration

</td><td>

If using the Interaction wrap up feature, the system administrator can configure the Interaction form and add the **Wrap up duration** field.

 This field records the length of time that the Interaction record spends in the Wrap Up state. This is a read-only field. If a duration is not calculated, this field is set to 0.

 Duration is calculated as the time an interaction is in the Wrap Up state before moving to either Closed Complete or Closed Abandoned.

**Note:** If an agent closes the tab and ends the interaction, the wrap up duration is recorded as 0 seconds.

</td></tr><tr><td>

System wrap up

</td><td>

If using the Interaction wrap up feature, the system administrator can configure the Interaction form and add the **System wrap up** field.

 The system determines if the interaction wrap up was performed manually by an agent \(by clicking **End Wrap Up**\) or automatically by the system and sets this field accordingly.

-   Set to **True** when automatic wrap up is enabled and the system moves an interaction from the Wrap Up state to either Closed Complete or Closed Abandoned at the end of the wrap up duration.
-   Set to **False** when an agent manually wraps up an interaction.

 The default value for this field is false.

</td></tr></tbody>
</table>**Parent Topic:**[Interaction wrap up](../concept/interaction-wrap-up-state.md)

