---
title: Create or edit planning attributes
description: Create or edit planning attributes to plan and forecast your resources and financials for a project.Use the Planning attribute form fields to modify a planning attribute.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Planning attributes, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create or edit planning attributes

Create or edit planning attributes to plan and forecast your resources and financials for a project.

## Before you begin

Role required: pps\_admin, sn\_align\_core.apw\_admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Planning attributes**.

2.  Use the following options to create or edit a planning attribute.

<table id="choicetable_bwd_pjg_cxb"><thead><tr><th align="left" id="d38151e76">

Option

</th><th align="left" id="d38151e79">

Description

</th></tr></thead><tbody><tr><td id="d38151e85">

**To create an attribute**

</td><td>

1.  Select **New**.
2.  On the Planning attribute form, fill the fields.

For a description of the field values, see [Planning attribute form](configure-planning-attributes.md#).

3.  Select **Submit**.

The attribute is created and the planning attributes screen is displayed.

4.  Open the newly created attribute.
5.  Enter field names for the lookup table values in the Planning attribute column configurations table.
6.  Set the planning attribute to active using the **Active** option to enable it for resource or financial planning.


</td></tr><tr><td id="d38151e136">

**To update an attribute**

</td><td>

1.  Select the required attribute name.
2.  On the Planning attribute form, fill in the fields.


</td></tr></tbody>
</table>3.  Enter field names for the lookup table values in **Planning attribute column configurations** table.

4.  To add new configurations to the default column configuration list for any tables containing the financials or resource management attributes:

    1.  Select **New**.

    2.  Select a lookup table from the list.

    3.  Select a field name from the list and select **Submit**.

        For example: If you want to create an attribute for the Location field, add the location-related columns to the selected lookup table.

        The selected item is added to the column configuration list with an auto-generated field description.

5.  Select **Update**.

    **Important:** If you're creating an attribute for resource management, make sure that you add the Attribute field to the **resource\_allocation**, **resource\_plan**, and **sn\_plng\_att\_core\_resource\_assignment** lookup tables. Similarly, if you're creating an attribute for financials, add the Attribute field to the **cost\_plan** lookup table along with the resource management lookup tables.


## Planning attribute form

Use the Planning attribute form fields to modify a planning attribute.

<table id="table_z14_vbg_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attribute type

</td><td>

Attribute type list.-   Resource: To use the attribute for resources or financials for your project.
-   Task: To use the attribute to generate labor costs only.

</td></tr><tr><td>

Attribute name

</td><td>

Name of the attribute.

</td></tr><tr><td>

Enable for resource management

</td><td>

Option to enable the attribute for resource planning.This option is selected by default.

</td></tr><tr><td>

Enable for financials

</td><td>

Option to enable/disable the attribute for financial planning.**Note:**

-   To enable an attribute for financials, it should be enabled for resource management.
-   To disable an attribute for financials for an ongoing project: Delete all the existing labor cost plans, disable the attribute for financials, and regenerate labor cost plans.

</td></tr><tr><td>

Attribute table

</td><td>

The default attribute table is the Employee Profile from which the attribute sources the information.

</td></tr><tr><td>

Attribute field

</td><td>

Element name from the Employee Profile table to define the attribute.Relevant lookup tables for the selected field value are displayed in the Planning attribute column configurations table after saving the form.

Enter the respective field names of the columns to activate the attribute.

</td></tr><tr><td>

Active

</td><td>

Option to activate and use the attribute for planning.

</td></tr><tr><td>

Task attribute table and field

</td><td>

Table name and field value for a task attribute.This field is visible only while creating a Task type attribute.

</td></tr></tbody>
</table>