---
title: Associate or update primary goal or target
description: Associate a primary goal or target for the planning items where the items contribute to achieving the goal or target.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage enterprise goals, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Associate or update primary goal or target

Associate a primary goal or target for the planning items where the items contribute to achieving the goal or target.

## Before you begin

Role required: sn\_apw\_advanced.spw\_goal\_user

## About this task

You can associate a goal or target as primary with a planning item by populating the **Primary goal** and **Primary target** fields on the Planning item form respectively. When you populate the **Primary target** field, the **Primary goal** is automatically populated with the goal of the populated target. For more information, see [Planning item form](../../alignment-planner-workspace/reference/planning-item-form.md).

After you associate planning items with goals or targets, you can check these relationships directly on the Planning items tab of the goal's form or on the Goal/Target Relationships tab of the planning item's form.

**Note:**

-   By default, the goal or target becomes the primary when you associate a goal or target with a planning item for the first time. Then after, association of any goal or target with the planning item becomes a secondary association unless the **Primary** field is selected while associating the goal or target.
-   When a planning item already has a primary goal association and you want to make another goal as primary, the existing primary goal association becomes secondary and the fresh association becomes primary for the planning item.
-   Associating the primary goal or target isn’t supported for strategic items such as initiatives and strategic programs.
-   To associate the primary goal or target with a custom planning item, ensure that the custom planning item is added to the **planning\_item\_types\_allow\_list** property.

## Procedure

1.  Open the required planning item form using one of the following options.

<table id="choicetable_ncp_ty2_fqb"><thead><tr><th align="left" id="d46444e112">

Option

</th><th align="left" id="d46444e115">

Navigation

</th></tr></thead><tbody><tr><td id="d46444e121">

**From the Portfolio Plans tab**

</td><td>

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.
2.  From the list of portfolio plans, select the required portfolio plan that the planning item belongs to.
3.  Select **Planning**.
4.  Select **Prioritization**, **Roadmap**, or **Hierarchy** tab.
5.  Select a planning item that you want to associate or update the primary goal or target with.

The side panel opens with the **Details** tab.

Alternatively, you can select **Full details** and open the item's record page. Select the **Details** tab from the record page.

</td></tr><tr><td id="d46444e186">

**From the Free-form Roadmaps tab**

</td><td>

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.
2.  On the Portfolio Planning page, select **Free-form Roadmaps**.
3.  From the list of roadmaps, select the required roadmap that the planning item belongs to.
4.  Select a planning item that you want to associate or update the primary goal or target with.

The side pane opens with the **Details** tab.

Alternatively, you can select **Full details** and open the item's record page. Select the **Details** or **Goal/Target Relationships** tab from the record page.

</td></tr></tbody>
</table>2.  On the Item details side panel or **Details** tab, fill in or update the **Primary goal** and **Primary target** fields with the goal and target respectively that you want to associate or update.

    Alternatively, you can select **Add** in the **Goal/Target Relationships** tab, populate the **Goal** and **Target** fields as needed, and then select **Primary**. The **Primary goal** and **Primary target** fields are then automatically populated on the planning item form.

    For a description of the field values, see [Planning item form](../../alignment-planner-workspace/reference/planning-item-form.md).

3.  Select either **Update** or **Save**.


## What to do next

If you want to remove the existing goal or target association, you can remove the association by selecting the association record and selecting the **Remove** option on the Goal/Target Relationships tab of the planning item record. If the planning item has the primary goal and secondary goal association, you can remove the primary association only after you make any other goal as primary for the planning item.

**Related topics**  


[Create a goal](create-goal-strategy.md)

[Add a target for goal](set-target-for-goal-strategy.md)

[Duplicate a goal or target](duplicate-goal-target-strategy.md)

[Align work with a goal or target](associate-work-with-goals-strategy.md)

[Send a reminder for target actuals check in](send-reminder-target-checkin-strategy.md)

