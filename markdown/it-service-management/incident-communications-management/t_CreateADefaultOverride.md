---
title: Create a default override
description: Create a default override to specify user or group for a contact definition of an incident communication plan. It helps you to set multiple conditions based on which a user or a group is considered as a contact.
locale: en-US
release: zurich
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Incident Communications Management and Contacts, Manage, Incident Communications Management, IT Service Management]
---

# Create a default override

Create a default override to specify user or group for a contact definition of an incident communication plan. It helps you to set multiple conditions based on which a user or a group is considered as a contact.

## Before you begin

Role required: ia\_admin or admin

## About this task

The Default overrides related list is available only if you select **Default override** as the value of the **Source** field in the Contact definition form.

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Contact Administration** &gt; **Contact Definitions**.

2.  Open the contact definition record.

3.  In the Default override section, click **New**.

    ![Default override form](../image/NewDefaultOverride.png)

4.  On the form, fill the fields.

<table id="table_wf5_bzg_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order

</td><td>

The order in which the condition in default override should be evaluated.

</td></tr><tr><td>

User value

</td><td>

User specified in the **User value** field is assigned as the contact if the condition in the default override matches. **Note:** The **User value** field appears if the value of the **Type** field in the Contact definition form is **User**.

</td></tr><tr><td>

Group value

</td><td>

Group specified in the **Group value** field is assigned as the contact if the condition in the default override matches. **Note:** The **Group value** field appears if the value of the **Type** field in the Contact definition form is **Group**.

</td></tr><tr><td>

Condition

</td><td>

The conditions defining whether the default override values are to be applied. If multiple conditions are defined, each condition is evaluated as per the listed order. If no conditions match, the default override is not applied.

</td></tr></tbody>
</table>5.  Click **Submit**.

    Default override and its conditions are defined for a contact definition.


**Parent Topic:**[Incident Communications Management and Contacts](../concept/c_IncidentAlertContact.md)

**Related topics**  


[Responsibilities for Incident Communication Plan](../reference/r_ResponsibilitiesForIncidentAlerts.md)

[Define contact responsibilities](t_CreateAContactResponsibility.md)

[Create a contact definition](t_CreateAContactDefinition.md)

[Add a user as a contact](t_AddAContactManually.md)

