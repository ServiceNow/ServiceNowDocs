---
title: Add special handling notes for an HR Service Delivery case
description: Create special handling notes that appear for a specific HR case or set of conditions.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use HR Case Management, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add special handling notes for an HR Service Delivery case

Create special handling notes that appear for a specific HR case or set of conditions.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **Special Handling Notes** &gt; **Special Handling Notes**.

2.  Select **New** or an existing record.

3.  Fill in the fields.

<table id="table_af5_kxt_hkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Enter a short description that describes the special handling note.

</td></tr><tr><td>

Message

</td><td>

Enter a message that appears in the special handling notes. Rich text formatting is available.

</td></tr><tr><td>

Type

</td><td>

Select the type of special handling note:-   Standard: Select to display a special handling note for a specific table and related record. For example, if you select HR case, you can select from list of HR cases. A special handling note appears for a specific HR case already created.
-   Conditional: Select to use filter conditions. Use filter conditions to specify when a special handling note appears.


</td></tr><tr><td>

Display as a pop-up alert

</td><td>

Leave this field blank. **Note:** Currently, a pop-up window is only for HR Service Delivery Agent Workspace.

</td></tr><tr><td>

Priority

</td><td>

Assign a priority to the special handling note. The choices are:-   1 - Critical \(red\)
-   2 - High \(orange\)
-   3 - Moderate \(light green\)
-   4 - Low \(light blue\)
The priority and color appear in the special handling note.

</td></tr><tr><td>

Status

</td><td>

The status of the special handling note.-   Active: The special handling note is active.
    -   Active notes appear in the pop-up window.
    -   Active notes remain until dismissed or set to Inactive or Expired.
-   Inactive: The special handling note is no longer active and does not appear in a pop-up window. Inactive special handling notes still appear when you navigate to **Special Handling Notes** &gt; **Special Handling Notes**.
-   Expired: The special handling note is no longer active. The expiration date has passed or manually expired.


</td></tr><tr><td>

Effective immediately

</td><td>

Check to activate the special handling note immediately.If you leave this field unchecked, you can specify a date and time the special handling note appears.

</td></tr><tr><td>

Effective on

</td><td>

Appears when you leave the Effective immediately field unchecked.Select a date and time when the special handling note appears.

</td></tr><tr><td>

Expires on

</td><td>

If you want to automatically inactivate a special handling note, select a date and time.

</td></tr><tr><td>

Table name

</td><td>

Appears when you select Conditional from the Type field.Select the HR table the special handling note appears for when a specific HR case appears or when you satisfy filter conditions.

**Note:** Special handling notes do not support child tables. For example, if you select the HR case \[sn\_hr\_core\_case\], the special handling note only appears for cases specific to the table. To create a special handling note for child tables, you must create a special handling note for each table.

</td></tr><tr><td>

Related record

</td><td>

Appears when you select Standard from the **Type** field.Select and a pop-up menu appears.

 Select the table name and a corresponding case from the Document field. For example, select HR case from the Table name field and the HR case you want the special handling note to appear.

</td></tr><tr><td>

Conditions

</td><td>

Appears when you select Conditional from the **Type** field.Select conditions when met, show the special handling note. For example, select:

-   HR profile
-   is
-   Aileen Mottern
This condition shows the special handling note for a General Inquiry case for Aileen Mottern.

**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Select **Submit** or **Update**.


**Parent Topic:**[Use HR Case Management](../concept/c_HRCaseManagement.md)

