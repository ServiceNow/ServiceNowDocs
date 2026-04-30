---
title: Create or edit planning attributes
description: Create or edit planning attributes to plan and forecast your resources and financials for a project.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the Planning attributes, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create or edit planning attributes

Create or edit planning attributes to plan and forecast your resources and financials for a project.

## Before you begin

Role required: pps\_admin, sn\_align\_core.apw\_admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Planning attributes**.

2.  Use the following options to create or edit a planning attribute.

<table id="choicetable_bwd_pjg_cxb"><thead><tr><th align="left" id="d39520e76">

Option

</th><th align="left" id="d39520e79">

Description

</th></tr></thead><tbody><tr><td id="d39520e85">

**To create an attribute**

</td><td>

1.  Select **New**.
2.  On the Planning attribute form, fill the fields.

For a description of the field values, see [Planning attribute form](planning-attributes-form.md).

3.  Select **Submit**.

The attribute is created and the planning attributes screen is displayed.

4.  Open the newly created attribute.
5.  Enter field names for the lookup table values in the Planning attribute column configurations table.
6.  Set the planning attribute to active using the **Active** option to enable it for resource or financial planning.


</td></tr><tr><td id="d39520e136">

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


**Related topics**  


[Using the Planning attributes](../concept/planning-attributes.md)

