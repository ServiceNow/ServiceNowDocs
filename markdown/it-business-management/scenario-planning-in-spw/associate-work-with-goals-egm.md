---
title: Associate a planning item with goals or targets
description: Create a goal or target relationship with a planning item or any other item to identify and associate your current or future work and achieve your goals and targets.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage goals, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Associate a planning item with goals or targets

Create a goal or target relationship with a planning item or any other item to identify and associate your current or future work and achieve your goals and targets.

## Before you begin

Role required: sn\_apw\_advanced.spw\_goal\_user and sn\_align\_core.apw\_user

## About this task

You can associate a goal or target with the planning items - Project, Demand, and Epic.

From the Align work window, you can associate a goal or target with multiple planning items at a time. From the Planning items tab of the goal or target, you can associate a goal or target with only one planning item at a time.

You can create goal or target relationships with a custom planning item from the Align work window only if the planning item table is added to the **planning\_item\_types\_allow\_list** property. For more information, see [Enable custom item types in Strategic Planning](../../alignment-planner-workspace/task/enable-custom-item-types-strategic-planning-workspace.md).

**Note:** When a goal or target relationship is created with a planning item \(Project, Demand, or Epic\), the record appears on the Planning items tab on the goal record. When a goal or target relationship is created with any other item, the record appears on the Other items tab on the respective goal or target record.

## Procedure

1.  Open the Goal/Target Relationship form using one of the following options.

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d133532e80">

Option

</th><th align="left" id="d133532e83">

Steps

</th></tr></thead><tbody><tr><td id="d133532e89">

**From the Align work window**

</td><td>

**Note:** From the Align work window, you can create a goal or target relationship with planning items only. To create a goal or target relationship with any item other than planning item, navigate to the full details page of the item using the second option in this table.

 1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.
2.  From the list of portfolio plans, select the required portfolio plan that the goal belongs to.
3.  In the Goals view, select the **Goals and targets** tab.
4.  Next to the required goal or target that you want to associate a work item for, select the row context menu icon \(![Row context menu icon.](../../alignment-planner-workspace/images/action-menu-icon.png)\) and select **Align work**.

Alternatively, you can select **View aligned work** from the row context menu icon \(![Row context menu icon.](../../alignment-planner-workspace/images/action-menu-icon.png)\) to open the side panel. Select the Align work icon \(![Align work item icon.](../images/icon-align-work-item.png)\) from the Aligned work tab of the side panel.

5.  On the Align work window, select the planning items you want to associate with the goal or target and then select **Confirm**.

![Align work to goals.](../images/goals-align-work-to-goal.gif)

You can search for the required planning items by applying filter on the Name column.

For a description of the field values, see [Goal/Target Relationship form](../reference/goal-relationship-form-egm.md).

</td></tr><tr><td id="d133532e184">

**From the Planning items or Other items tab**

</td><td>

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.
2.  From the list of portfolio plans, select the required portfolio plan that the goal belongs to.
3.  In the Goals view, select the **Goals and targets** tab.
4.  Select the required goal or target that you want to associate a planning or strategic item for.

The Goal side panel opens with the **Details** tab.

5.  In the side panel, select **Full Details** to open the goal form.
6.  \(To create a goal or target relationship with a planning item\) On the **Planning items** tab, select **Add**.
7.  \(To create a goal or target relationship with an item other than planning item\) On the **Other items** tab, select **Add**.
8.  On the Goal/Target Relationships form, for a planning item \(Project, Demand, or Epic\), fill in the **Planning item type** and **Planning item** fields on the Goal/Target Relationship form.

For any item other than planning item, on the Goal/Target Relationship form, fill in the **Table** and **Document ID** fields.

For a description of the field values, see [Goal/Target Relationship form](../reference/goal-relationship-form-egm.md).

</td></tr></tbody>
</table>2.  Select either **Done** or **Save**.


