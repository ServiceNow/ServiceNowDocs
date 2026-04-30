---
title: Special handling notes with HR Service Delivery Agent Workspace
description: Get an agent's attention by adding special handling notes to a case.Configure an HR table to use special handling notes. You must do this before you can create special handling notes.Create special handling notes that an agent can see for a specific HR case or an HR case with a set of conditions.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Setting up HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Special handling notes with HR Service Delivery Agent Workspace

Get an agent's attention by adding special handling notes to a case.

You can set up special handling notes to appear as a pop-up modal or as a related list on the form.

Special handling notes have a status, an assigned priority, and an expiration date.

To configure special handling notes for HR Service Delivery Agent Workspace, do the following:

1.  Edit the special handling notes properties.

    For more information, see [Configure special handling notes properties](https://www.servicenow.com/docs/access?context=t_EnableOnScreenAlertProperties&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

2.  Create special handling notes for an HR table.

    For more information, see [Configure special handling notes](https://www.servicenow.com/docs/access?context=configure-special-handling-notes&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

3.  Create a special handling note.

    For more information, see [Configure special handling notes](https://www.servicenow.com/docs/access?context=configure-special-handling-notes&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).


For more information, see Highlighted values in the form header and [Special handling notes](https://www.servicenow.com/docs/access?context=c_OnScreenAlerts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

## Configure special handling notes in HR Service Delivery Agent Workspace

Configure an HR table to use special handling notes. You must do this before you can create special handling notes.

### Before you begin

Role required: sn\_hr\_core.admin

### Procedure

1.  Navigate to **All** &gt; **Special Handling Notes** &gt; **Configuration**.

2.  Click **New** or select an existing record.

3.  In the **Table name** list, select an HR table.

    Selecting the HR case \[sn\_hr\_core\_case\] does not automatically include any child tables.

4.  Move a related field to the Selected list.

5.  Click **Submit**.

    The Special Handling Notes Configuration list appears.


## Add a special handling note in HR Service Delivery Agent Workspace

Create special handling notes that an agent can see for a specific HR case or an HR case with a set of conditions.

### Before you begin

Role required: sn\_hr\_core.admin

### Procedure

1.  Navigate to **All** &gt; **Special Handling Notes** &gt; **Special Handling Notes**.

2.  Click **New** or select an existing record.

3.  On the form, fill in the fields.

<table id="table_l31_1hg_yjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Short description that describes the special handling note.

</td></tr><tr><td>

Message

</td><td>

Message that appears in the special handling notes. Rich text formatting is available.

</td></tr><tr><td>

Type

</td><td>

Type of special handling note that you can select:-   Standard: Select this option to display a special handling note for a specific record. When you select the ![Lookup documents using list icon](../image/magnifying-glass.png) Lookup documents using list icon, you can select a table and associated record.

![Special Handling Notes - Related record](../reference/images/hr-special-handling-notes-standard.png)

-   Conditional: Select this option to use filter conditions to specify when a special handling note appears.


</td></tr><tr><td>

Display as a pop-up alert

</td><td>

Special handling note that appears as a pop-up alert. **Note:** Currently, a pop-up alert is the only way to show special handling notes. Select this option to show special handling notes. If you leave this option clear, special handling notes appear on the HR case form as an embedded list on the platform version of HR. For more information, see [Work an HR case](../task/t_CreateAnHRCase.md).

</td></tr><tr><td>

Priority

</td><td>

Priority that you assign to the special handling note. The choices are:-   1 - Critical \(red\)
-   2 - High \(orange\)
-   3 - Moderate \(light green\)
-   4 - Low \(light blue\)
The priority and color appear in the special handling note.

</td></tr><tr><td>

Status

</td><td>

Status of the special handling note: The status based on the **Expires on date**. -   Active: The special handling note is active.
    -   Active notes appear in the pop-up window.
    -   Active notes remain until dismissed or set to Inactive or Expired.
-   Inactive: The special handling note is no longer active and does not appear in a pop-up window. Inactive special handling notes still appear when you navigate to **Special Handling Notes** &gt; **Special Handling Notes**.
-   Expired: The special handling note is no longer active. The expiration date has passed or manually expired.


</td></tr><tr><td>

Effective immediately

</td><td>

Option to activate the special handling note immediately.If you leave this option unselected, you can specify a date and time that the special handling note appears.

</td></tr><tr><td>

Effective on

</td><td>

Field that is available when you leave the **Effective immediately** option unselected.Select the ![Select date and time icon](../reference/images/calendar-icon.png) Select date and time icon to select the date and time when the special handling note appears.

</td></tr><tr><td>

Expires on

</td><td>

Field where you can set a date and time to automatically inactivate a special handling note. Click the ![Select date and time icon](../reference/images/calendar-icon.png) Select date and time icon to access the calendar where you can choose the date and time to activate the special handling note.

</td></tr><tr><td>

Table name

</td><td>

List that is available when you select **Conditional** from the **Type** field.Select the HR table where you want the special handling note to appear in for a specific HR case or when you satisfy filter conditions.

**Note:** Special handling notes do not support child tables. For example, if you select the HR case \[sn\_hr\_core\_case\], the special handling note only appears for cases that are specific to the table. To create a special handling note for child tables, you must create a special handling note for each table.

</td></tr><tr><td>

Related record

</td><td>

Field that is available when you select **Standard** from the **Type** field.When you select this option, a pop-up window appears where you can select the table name and a case from the **Document** field. For example, you can select HR case from the **Table name** field and the HR case where you want the special handling note to appear.

</td></tr><tr><td>

Conditions

</td><td>

Field that is available when you select **Conditional** from the **Type** field.Select the conditions when met that would show the special handling note. For example, let's say that you want to add a special handling note for a General Inquiry case for an employee named Aileen Mottern, you would select: **\[HR profile\] \[is\] \[Aileen Mottern\]**.

**Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


