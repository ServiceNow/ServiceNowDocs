---
title: Add milestones for roadmap items in Strategic Planning Workspace
description: Track key outcomes of your planning items \(such as demands, scrum epics, or programs\) by creating milestones for them, directly from the roadmap view.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace, roadmap]
breadcrumb: [Plan roadmaps, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Add milestones for roadmap items in Strategic Planning Workspace

Track key outcomes of your planning items \(such as demands, scrum epics, or programs\) by creating milestones for them, directly from the roadmap view.

## Before you begin

Role required: sn\_align\_core.apw\_user

## About this task

Select a roadmap item and create a milestone for it. Use the roadmap side panel to fill in the details and submit.

For free-form roadmaps, milestones are supported only if the source table is Planning Item \[sn\_align\_core\_planning\_item\] or one of its extensions.

**Important:**

You can’t add a project milestone from the roadmap view. Creating or updating project milestones may impact the associated project plans. So, it’s recommended to create or update project milestones using Project Workspace in Project Portfolio Management \(PPM\).

However, any existing milestones of the project are visible on the roadmap if you've [integrated Strategic Planning with PPM](../../apw-internal-integrations/concept/configuring-apw-with-agile-safe-and-ppm.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning** and open your roadmap.

<table id="choicetable_vwv_t4z_5wb"><thead><tr><th align="left" id="d208634e129">

Roadmap type

</th><th align="left" id="d208634e132">

Navigation

</th></tr></thead><tbody><tr><td id="d208634e138">

**Portfolio plan roadmap**

</td><td>

1.  From the Portfolio Plans tab, select a portfolio plan.
2.  From the Planning section, select **Roadmap**.


</td></tr><tr><td id="d208634e159">

**Free-form roadmap**

</td><td>

From the Free-form Roadmaps tab, select a roadmap.

</td></tr></tbody>
</table>2.  From the roadmap view, click a planning item to which you want to add the milestone.

    The side panel opens showing the item details.

3.  Select the Milestones tab.

    Alternatively, you can click **Full details** and select the Milestones tab from the full details page.

4.  Select the Add milestone icon \(![Add milestone icon.](../../alignment-planner-workspace/images/icon-add.png)\).

    If the item doesn't have any milestones, select **New milestone**.

5.  On the form, fill in the fields.

    For field information, see [Planning item milestone form](../../alignment-planner-workspace/reference/planning-item-milestone-form.md).

6.  Select **Save**.

    When you go back to the Milestones tab, you can see the milestone listed there.

7.  Repeat steps 2 through 6 to add more milestones to your items.


## Result

-   Milestones that you created are indicated on the roadmap item bars.

    Here’s an image of a sample roadmap with the roadmap items indicating that they have milestones.![Planning item-level milestones.](../images/roadmap-item-milestones.png)

-   Pointing your cursor over these milestone indicators shows the details such as the milestone name, type, and due date.
-   Clicking one of these indicators opens the Milestones tab of the Item details side panel. Here, you can see a list of all the milestones for this planning item.

## What to do next

-   [Learn how to customize the display of milestones on the roadmap.](../../alignment-planner-workspace/concept/personalizing-the-milestones-display-on-the-roadmap.md)
-   [Learn when a planning item milestone can be in an error state.](../../alignment-planner-workspace/concept/error-states-for-planning-item-milestones.md)
-   [Learn how to manage the milestones for planning items.](manage-planning-item-milestones.md)

