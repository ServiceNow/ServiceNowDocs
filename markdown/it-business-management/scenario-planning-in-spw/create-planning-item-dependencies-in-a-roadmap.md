---
title: Add dependencies for roadmap items
description: Create dependencies and visualize relationships between planning items of your portfolio or free-form roadmap, so that you can adjust their scheduling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/create-planning-item-dependencies-in-a-roadmap.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace, roadmap]
breadcrumb: [Plan roadmaps, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Add dependencies for roadmap items

Create dependencies and visualize relationships between planning items of your portfolio or free-form roadmap, so that you can adjust their scheduling.

## Before you begin

Role required: sn\_align\_core.apw\_user

## About this task

From the portfolio roadmap or the free-form roadmap, use the item details side panel to create dependencies between two planning items. Dependencies are supported for projects, epics, demands, initiatives, programs, or any custom planning item types that you may have created.

The dependency for a planning item on your roadmap can be on an item from the same roadmap, a different roadmap, or the item might not be planned yet. [Learn more about dependencies in the roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/roadmap-planning-overview.md).

**Note:** Dependencies for free-form roadmaps are available only if the roadmap's source table is Planning Item \[sn\_align\_core\_planning\_item\] or one of its extensions.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning** and open your roadmap.

<table id="choicetable_vwv_t4z_5wb"><thead><tr><th align="left" id="d131451e107">

Roadmap type

</th><th align="left" id="d131451e110">

Navigation

</th></tr></thead><tbody><tr><td id="d131451e116">

**Portfolio plan roadmap**

</td><td>

1.  From the Portfolio Plans tab, select a portfolio plan.
2.  From the Planning section, select **Roadmap**.


</td></tr><tr><td id="d131451e137">

**Free-form roadmap**

</td><td>

From the Free-form Roadmaps tab, select a roadmap.

</td></tr></tbody>
</table>2.  From the roadmap view, click a planning item for which you want to add the dependency.

    The side panel opens showing the item details.

3.  Select **More** &gt; **Dependencies**.

4.  From the Dependencies tab, select the Add dependency icon \(\[Omitted image "icon-add.png"\] Alt text: Add dependency icon.\).

5.  On the form, fill in the fields.

    For form field information, see [Dependency form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/dependency-form.md).

6.  Select **Save**.


## Result

The dependency is created between the selected planning items and is listed in the Dependencies tab of the Item details side panel.\[Omitted image "dependencies-item-details-panel.png"\] Alt text: Dependency details in side panel.

On the roadmap, you can see the dependency details from the roadmap item card or the dependency lines. [Learn about display settings available for dependencies on the roadmap.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/customizing-dependencies-display-on-roadmap.md)

If one of the dependency items is not on the roadmap, then the dependency details are shown on the roadmap item card, with a redirect link to the external planning item. In this case, the items could belong to the same roadmap or not.

\[Omitted image "dependency-line-card.png"\] Alt text: Dependency pop-up card and dependency lines between the items.

## What to do next

-   [Learn how to resolve roadmap item dependency errors.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/error-state-for-planning-item-dependencies.md)
-   Update the dependency details or delete it. See [Update roadmap item dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/manage-planning-item-dependencies-apw.md).

