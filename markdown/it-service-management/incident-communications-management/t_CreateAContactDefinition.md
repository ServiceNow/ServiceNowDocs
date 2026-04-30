---
title: Create a contact definition
description: Define the recipients of a particular incident communication plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle.
locale: en-US
release: xanadu
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Incident Communications Management and Contacts, Manage, Incident Communications Management, IT Service Management]
---

# Create a contact definition

Define the recipients of a particular incident communication plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle.

## Before you begin

Role required: ia\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Contact Administration** &gt; **Contact Definitions**.

2.  Click **New**.

    ![Contact definition form](../image/CreateContactDefinition.png "Contact definition form")

3.  On the form, fill in the fields.

<table id="table_hjx_zwg_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the contact definition.

</td></tr><tr><td>

Type

</td><td>

Type of contact such as user or group that you want to involve in the plan.

</td></tr><tr><td>

Responsibility

</td><td>

Responsibility that the user or group is expected to handle.

</td></tr><tr><td>

Source

</td><td>

Method to determine the user or group to associate with this definition.The source can be:

-   **None**: Use no association. You should associate users or groups [manually](t_AddAContactManually.md) within the Incident Communication Plan form.
-   **Default Override**: Use [default override](t_CreateADefaultOverride.md) to associate users or groups based on conditions.
-   **Form Field**: Use information from the incident communication plan form based on the value specified in the **Source field**.


</td></tr><tr><td>

Quantity

</td><td>

The maximum number of contacts that can be associated with the selected responsibility for each incident communication plan record. **Note:** The **Quantity** field appears only when you select **None** as the value for the **Source** field.

</td></tr><tr><td>

Source field

</td><td>

The field on the Incident Communication Plan form whose value is considered to be the contact associated with the selected contact responsibility.-   For contact type as **User**, the values are **Assigned to**, **Closed by**, **Opened by**, or **Resolved by**.
-   For contact type as **Group**, the value is **Assignment group**.
 **Note:** The **Source field** appears only when you select **Form field** as the value for the **Source** field.

</td></tr><tr><td>

Active

</td><td>

Check box to indicate whether the definition is active or not.

</td></tr><tr><td>

Condition

</td><td>

The conditions that must be met to associate this contact definition to a particular user or group. If multiple conditions are defined, each condition is evaluated in the order listed.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Incident Communications Management and Contacts](../concept/c_IncidentAlertContact.md)

**Related topics**  


[Responsibilities for Incident Communication Plan](../reference/r_ResponsibilitiesForIncidentAlerts.md)

[Define contact responsibilities](t_CreateAContactResponsibility.md)

[Create a default override](t_CreateADefaultOverride.md)

[Add a user as a contact](t_AddAContactManually.md)

