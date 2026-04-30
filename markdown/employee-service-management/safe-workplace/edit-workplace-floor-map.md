---
title: Update a workplace floor plan
description: Update a workplace floor plan by uploading a new plan.
locale: en-US
release: yokohama
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Providing your workplace data, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Update a workplace floor plan

Update a workplace floor plan by uploading a new plan.

## Before you begin

Role required: sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration** &gt; **Floors**.

2.  Select the floor you want to update.

3.  Select the **Update floor plan** related link.

4.  Select **Manage Attachments**, delete the current floor plan file, and attach the new floor plan file.

    You can have only one .dxf file uploaded at a time.

5.  Select **Next**.

6.  In the Select layers column, select the layers that you want to appear on the floor plan.

    For example, you might not want electrical rooms, kitchens, storage closets, or other elements to appear on the floor plan when it renders.

7.  Select **Render**.

    The floor plan appears under the **Preview plan** tab. Use your mouse to zoom in and out.

8.  Select **Next**.

9.  On the form, fill in the fields.

<table id="table_ty3_xqq_zlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AutoCAD tag

</td><td>

Tags from the uploaded `.dxf` file identify spaces on the floor plan.The tags that appear are those that you selected in the **Select layers** column.

 **Note:** If you do not see any AutoCAD tags, you can use AutoCAD software to change text or text objects into block references.

</td></tr><tr><td>

Space Field

</td><td>

The field in the Space \[sn\_wsd\_core\_space\] table with which you want to associate the tag. For example, you could associate an attribute named ROOM\_NAME with the **Name** field and give it a higher order so it becomes the second part of the name.

</td></tr><tr><td>

Order

</td><td>

Determines the order of processing for your AutoCAD tag to Space Field mapping.**Note:** Lower numbers process first.

</td></tr></tbody>
</table>10. Select **Preview Changes** and in the **Preview changes** tab, review the changes you are going to make before you commit them.

11. Select **Submit**.


## Result

The following changes occur:

-   Map values are filled in.
-   Existing spaces that no longer match are deleted.
-   If old spaces have been renamed, the new names replace the old ones.
-   Any reservations are deleted.

A original floor record is updated with the floor plan attached to it. The Spaces related list is also updated. To view your changes, go to **Floor Plan Update Logs**.

-   **[View your workplace floor plan update logs](view-workplace-floor-map-logs.md)**  
After updating your workplace floor plan, you can view all changes made.

**Parent Topic:**[Providing your workplace data](../concept/providing-your-workplace-data.md)

