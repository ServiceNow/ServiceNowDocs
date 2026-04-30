---
title: Create planning items from the roadmap view
description: Create and add new planning items to your portfolio roadmap or free-form roadmap directly from the roadmap view.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace, edit free-form roadmap]
breadcrumb: [Plan roadmaps, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Create planning items from the roadmap view

Create and add new planning items to your portfolio roadmap or free-form roadmap directly from the roadmap view.

## Before you begin

Role required: sn\_align\_core.apw\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning** and open your roadmap.

<table id="choicetable_vwv_t4z_5wb"><thead><tr><th align="left" id="d128954e93">

Roadmap type

</th><th align="left" id="d128954e96">

Navigation

</th></tr></thead><tbody><tr><td id="d128954e102">

**Portfolio plan roadmap**

</td><td>

1.  From the Portfolio Plans tab, select a portfolio plan.
2.  From the Planning section, select **Roadmap**.


</td></tr><tr><td id="d128954e123">

**Free-form roadmap**

</td><td>

From the Free-form Roadmaps tab, select a roadmap.

</td></tr></tbody>
</table>2.  From the roadmap view, select the **New &lt;item type&gt;** option.

    -   For a free-form roadmap, the option depends on the roadmap's source table.
    -   For a portfolio plan roadmap, the option depends on the portfolio plan configuration.
<table id="table_s2x_tll_hvb"><thead><tr><th>

One planning item type

</th><th>

Multiple planning item types

</th></tr></thead><tbody><tr><td>

![New planning item on simple roadmap](../images/new-planning-item-simple.png)

</td><td>

![Sample actions for a new planning item on hybrid roadmap.](../../spw-prioritization/images/new-planning-item.png)

</td></tr></tbody>
</table>    For a free-form roadmap, if the source table is Planning Item \[sn\_align\_core\_planning\_item\] table, then the options depend on the values configured for the **freeform\_planning\_items\_creation\_list** property. By default, project and demand are available. Work with your admin to configure these options. See [Enable custom item types in Strategic Planning](../../alignment-planner-workspace/task/enable-custom-item-types-strategic-planning-workspace.md).

3.  On the form, fill in the required field information.

    For full field information, see [Planning item form](../../alignment-planner-workspace/reference/planning-item-form.md).

    You can refine planning item descriptions—for item types such as Demand, Epic, Project, Capability, Feature, and Story—using the Write planning item skill, if the Now Assist for SPM application is installed.

4.  Select **Submit**.


## Result

The new item appears on the roadmap, at a place based on its approved start and end dates.

If you don’t fill both the approved start and end date fields, the item that you created would be moved to the list of unscheduled items. You can add them to your roadmap plan later. For more information, see [Plan unscheduled items into a roadmap](schedule-unscheduled-items-to-a-roadmap.md).

-   **[Modify planning items from the roadmap view](manage-planning-items-from-the-roadmap-view.md)**  
Update the details of planning items or delete them from a portfolio plan or free-form roadmap so that your roadmap reflects the latest plans.

**Parent Topic:**[Planning roadmaps in Strategic Planning Workspace](../concept/roadmaps-in-alignment-planner-workspace.md)

