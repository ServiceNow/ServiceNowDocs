---
title: Create field mapping from a source table to a work order
description: Create a table map to configure the fields that are copied from a source table to the work order fields. The source of a work order can be a case, change, incident, or others.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring data mapping, Configuring Template Management for Field Service, Configuring work orders, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Create field mapping from a source table to a work order

Create a table map to configure the fields that are copied from a source table to the work order fields. The source of a work order can be a case, change, incident, or others.

## Before you begin

You must activate the Template Management for Field Service plugin \(com.snc.fsm\_template\_management\).

Role required: admin

## About this task

Table mapping ensures that when a work order is created from its source, the information from the source table is copied to the appropriate target fields in the work order.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Template Management** &gt; **Table Mapping**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ahn_ybx_b5b"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping Name

</td><td>

The table map name.

</td></tr><tr><td>

API Name

</td><td>

The API for this table map.This field is automatically set.

</td></tr><tr><td>

Source Table

</td><td>

The source table for the map. For example,case, incident, change, or more.

</td></tr><tr><td>

Active

</td><td>

Option to enable the mapping from the source to the target tables.

</td></tr><tr><td>

Application

</td><td>

Read only. The application for this table map.This field is automatically set.

</td></tr><tr><td>

Advanced Field Mapping

</td><td>

Option to enable the advanced field mapping.

</td></tr><tr><td>

Target Table

</td><td>

The target table for the map. For example, wm\_order.

</td></tr><tr><td>

Use Advanced Condition

</td><td>

Option to enable the advanced condition mapping, which uses a script. If enabled, add a script in the Advanced Condition field.

</td></tr><tr><td>

Advanced Condition

</td><td>

The script to use if the **Use Advanced Condition** field is enabled.

</td></tr><tr><td>

Conditions

</td><td>

Use the condition builder to select the conditions that apply to the table map.

</td></tr><tr><td>

Order

</td><td>

Order of priority for processing multiple matching map definitions simultaneously to resolve dependencies. -   If there is only one matching table map, the system uses that map.
-   If there are multiple matching table maps with the same order, the system uses the map with the older created date.
-   If there are multiple matching table maps with different orders, the system uses the map with the highest order.


</td></tr><tr><td>

Advanced Field Mapping

</td><td>

Option to map fields using advanced scripts.**Note:**

-   If the same source or target field is configured in both the basic and advanced field mappings, the advanced field mapping overrides the basic field mapping.
-   If the fields configured in the basic and advanced field mapping are different, the field configurations in the advanced field mapping are appended to the field configurations in the basic field mapping.
 This field is available only when the method of mapping is advanced and **Advanced Field Mapping** option is selected.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The table map is created by mapping the selected source table to the work order table.

5.  Create field mapping to copy information from the source field to an appropriate field in the work order.

    1.  In the Basic Field Mapping related list, select **New**.

    2.  On the form, fill in the fields.

<table id="table_s3v_ngg_c5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table Map

</td><td>

The table map name that is used for mapping fields.This field is automatically set.

</td></tr><tr><td>

Source Table

</td><td>

The source table for the map.This field is available only when the method of mapping is basic and the **Advanced** option is not selected.

</td></tr><tr><td>

Source Field

</td><td>

Column on the source table for field mapping.This field is available only when the method of mapping is basic and the **Advanced** option is not selected.

</td></tr><tr><td>

Application

</td><td>

The application for this field map.This field is automatically set.

</td></tr><tr><td>

Target Table

</td><td>

The target table for the map. For example, wm\_order.This field is automatically set.

</td></tr><tr><td>

Target Field

</td><td>

Columns on the work order table that you want to populate with the mapped source field value.

</td></tr><tr><td>

Order

</td><td>

Order of priority for processing mapped fields.

</td></tr><tr><td>

Active

</td><td>

Option to enable the mapping of information from the source field to the work order field.

</td></tr><tr><td>

Advanced

</td><td>

Option to map fields using advanced scripts.**Note:**

-   If the same source or target field is configured in both the basic and advanced field mappings, the advanced field mapping overrides the basic field mapping.
-   If the fields configured in the basic and advanced field mapping are different, the field configurations in the advanced field mapping are appended to the field configurations in the basic field mapping.


</td></tr></tbody>
</table>    3.  Click **Submit**.

6.  To map more field, repeat step 5.


## Result

The source and target tables are mapped and ready to copy information from the source field to an appropriate field in the work order.

