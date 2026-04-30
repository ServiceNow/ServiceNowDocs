---
title: Define access hour preferences for a work order task
description: Set default access hours for a work order task based on the customer preference at various levels, such as account, location, asset, and so on.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring the auto-population of access hours in a work order task, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Define access hour preferences for a work order task

Set default access hours for a work order task based on the customer preference at various levels, such as account, location, asset, and so on.

## Before you begin

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Access Hours Configuration** &gt; **Access Hour Levels**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ptm_2z3_dsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Access hour level

</td><td>

Name for the level.

</td></tr><tr><td>

Match Criteria

</td><td>

Criteria that must match to auto-populate the access hours.You can select multiple criteria.

</td></tr><tr><td>

Order

</td><td>

Order in which the access hour level should be evaluated to auto-populate the access hours.An ordering rule sorts the levels in descending order.

</td></tr><tr><td>

Active

</td><td>

Option to make this level configuration active.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The access hour level is created.

5.  From the Access Hour Configuration module, select **Access Hour Preferences**.

6.  Select **New**.

7.  On the form, fill in the fields.

<table id="table_qtx_l2p_dsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Access hour level

</td><td>

Name of the access hour level for which you’re defining preferences.The matching criteria specified for the access hour level appear as fields in the access hour preference form. For example, if the selected access hour level is Account and its specified matching criteria are Consumer and Location, the Location and Consumer fields appear in the Access Hour Preferences form.

</td></tr><tr><td>

Type

</td><td>

The type of output data to display access hours, either Value and Script.Use Value to define static access hours or Script to define the access hours dynamically.

</td></tr><tr><td>

Active

</td><td>

Option to make this preference active.

</td></tr><tr><td>

Access Hour

</td><td>

The static value used by the work order task to determine access hours, such as 8-5 weekdays.This field appears only when Value is selected in the Type field.

</td></tr><tr><td>

Script

</td><td>

The script used by the work order task to determine access hours. Use a script to determine access hours dynamically by making use of work order task attributes such as priority, work type, and so on. In the script, identify the attribute using the structure `workOrderTask.<attributeName> or workOrder.<attributeName>`. For example, you could determine the access hours of a task based on its priority. If the priority is 1, the script would return access hours 24x7 and if the priority is greater than 1, the script would return access hours 8-5 weekdays.

 This field appears only when Script is selected in the Type field.

</td></tr></tbody>
</table>8.  Select **Submit**.


## Result

The access hours are set to auto-populate in the work order task based on the customer preference at various levels.

