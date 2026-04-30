---
title: Configure list control settings for the list editor
description: You can configure the list control settings that affect the list editor.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [List editor administration, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure list control settings for the list editor

You can configure the list control settings that affect the list editor.

## Before you begin

Role required: personalize\_control

## About this task

[List control settings](t_ConfigureListControls.md#) customize the behavior of list functions for a table.

## Procedure

1.  Navigate to a list view for the desired table.

2.  Right-click any column heading and select **Configure** &gt; **List Control**.

3.  On the List Control form, select the desired settings.

<table id="table_zjz_rll_v4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List edit type

</td><td>

Ability for the user to edit values directly in individual cells in a list. The options are: -   **Save immediately \(cell edit mode\):** enables cell editing. The entire row is saved when the user enters a new value.
-   **Save data by rows:** enables cell editing. The row is saved only when the user navigates away from the row or selects the **Save** icon \(![Save icon](../image/IconSave.png)\). This mode allows the user to modify multiple values before saving a record.
-   **Disable list editing:** prevents users from editing cells in the list.
 This field is available for standard lists only.

</td></tr><tr><td>

List edit insert row

</td><td>

Ability for a user to create records in list view. When it is enabled, an empty row appears at the bottom of the list.![Insert a new row](../image/InsertANewRow.png)

 This field is available for standard lists only.

</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[List editor administration](../reference/r_AdministeringTheListEditor.md)

