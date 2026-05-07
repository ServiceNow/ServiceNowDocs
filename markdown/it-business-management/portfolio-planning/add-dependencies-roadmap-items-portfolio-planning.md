---
title: Add dependencies for roadmap items
description: Create dependencies and visualize relationships between planning items of your portfolio or free-form roadmap, so that you can adjust their scheduling.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace, roadmap]
breadcrumb: [Plan roadmaps, Portfolio Planning, Strategic Portfolio Management]
---

# Add dependencies for roadmap items

Create dependencies and visualize relationships between planning items of your portfolio or free-form roadmap, so that you can adjust their scheduling.

## Before you begin

Role required: sn\_align\_core.apw\_user

## About this task

From the portfolio roadmap or the free-form roadmap, use the item details side panel to create dependencies between two planning items. Dependencies are supported for projects, epics, demands, initiatives, programs, or any custom planning item types that you may have created.

The dependency for a planning item on your roadmap can be on an item from the same roadmap, a different roadmap, or the item might not be planned yet. [Learn more about dependencies in the roadmap](../../spw-roadmap/concept/roadmap-planning-overview.md#section_spl_34r_1tb).

**Note:** Dependencies for free-form roadmaps are available only if the roadmap's source table is Planning Item \[sn\_align\_core\_planning\_item\] or one of its extensions.

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace** &gt; **Portfolio Planning** and open your roadmap.

<table id="choicetable_ngc_1zz_5wb"><thead><tr><th align="left" id="d141379e107">

Roadmap type

</th><th align="left" id="d141379e110">

Navigation

</th></tr></thead><tbody><tr><td id="d141379e116">

**Portfolio plan roadmap**

</td><td>

1.  From the Portfolio Plans tab, select a portfolio plan.
2.  From the Planning section, select **Roadmap**.


</td></tr><tr><td id="d141379e137">

**Free-form roadmap**

</td><td>

From the Free-form Roadmaps tab, select a roadmap.

</td></tr></tbody>
</table>2.  From the roadmap view, click a planning item for which you want to add the dependency.

    The side panel opens showing the item details.

3.  Select **More** &gt; **Dependencies**.

4.  From the Dependencies tab, select the Add dependency icon \(![Add dependency icon.](../../alignment-planner-workspace/images/icon-add.png)\).

5.  On the form, fill in the fields.

    For form field information, see [Dependency form](../reference/dependency-form-portfolio-planning.md).

6.  Select **Save**.


## Result

The dependency is created between the selected planning items and is listed in the Dependencies tab of the Item details side panel.![Dependency details in side panel.](../../spw-roadmap/images/dependencies-item-details-panel.png)

On the roadmap, you can see the dependency details from the roadmap item card or the dependency lines. [Learn about display settings available for dependencies on the roadmap.](../../alignment-planner-workspace/concept/customizing-dependencies-display-on-roadmap.md)

If one of the dependency items is not on the roadmap, then the dependency details are shown on the roadmap item card, with a redirect link to the external planning item. In this case, the items could belong to the same roadmap or not.

![Dependency pop-up card and dependency lines between the items.](../../spw-roadmap/images/dependency-line-card.png)

## What to do next

-   [Learn how to resolve a roadmap item dependency error.](../../alignment-planner-workspace/reference/error-state-for-planning-item-dependencies.md)
-   Update the dependency details or delete it. See [Update roadmap item dependencies](update-roadmap-item-dependencies-portfolio-planning.md).

-   **[Update roadmap item dependencies](update-roadmap-item-dependencies-portfolio-planning.md)**  
Update or delete the dependencies for the planning items on your roadmap so that they reflect any change of plans.

**Parent Topic:**[Planning roadmaps in Portfolio Planning](../concept/planning-roadmaps-in-portfolio-planning.md)

