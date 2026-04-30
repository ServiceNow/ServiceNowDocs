---
title: Create a custom list based on a system table
description: Create a custom list on Workplace Central based on a system table.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2025-04-11"
reading_time_minutes: 1
breadcrumb: [Creating custom lists on Workplace Central, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Create a custom list based on a system table

Create a custom list on Workplace Central based on a system table.

## Before you begin

**Note:** You might require additional roles based on the system table that you want to access for the custom list.

Role required: sn\_wsd\_central.workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

2.  Select the **Lists** icon \(![Lists icon.](../images/wsd-central-lists-icon.png)\).

3.  Select the **My Lists** tab, then select **Add new list**.

    The New List pop-up appears with the **Start from existing** tab selected by default.

4.  Select the **Create your own** tab.

5.  On the form, fill in the fields.

<table id="table_fwb_q2s_z2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List Name

</td><td>

Display name for the custom list.

</td></tr><tr><td>

Select Source

</td><td>

System table that you want to use for your custom list.The system only displays tables that your role has access to. After you select a list, additional fields are displayed on the pop-up.

</td></tr><tr><td>

Select columns

</td><td>

Columns that are picked from the selected system table and displayed on the custom list.This field is displayed after you select a system table in the **Select Source** field. Some columns might already be selected based on the selected list.

</td></tr></tbody>
</table>6.  In the Add filters section, use the following options to filter and sort the records in your custom list.

<table id="choicetable_gj5_lfs_z2c"><thead><tr><th align="left" id="d298226e196">

Option

</th><th align="left" id="d298226e199">

Description

</th></tr></thead><tbody><tr><td id="d298226e205">

**Use existing filter**

</td><td>

Use an existing filter that is available with the selected Workplace Central list.

</td></tr><tr><td id="d298226e217">

**Save filter**

</td><td>

Save the current filter criteria.You can use saved filters for other custom lists. You can also grant permissions to other users to use the filter for their custom lists.

</td></tr><tr><td id="d298226e228">

**Refresh \(Update count\)**

</td><td>

Update the number of records based on the current filter criteria.

</td></tr><tr><td id="d298226e237">

**Editor**

</td><td>

Create condition sets for the filter criteria.

</td></tr><tr><td id="d298226e247">

**Sort by**

</td><td>

Select fields that are to sort the results in the custom lists in ascending or descending order.

</td></tr></tbody>
</table>7.  Select **Create**.


**Parent Topic:**[Creating custom lists on Workplace Central](../concept/creating-custom-lists-wsd.md)

