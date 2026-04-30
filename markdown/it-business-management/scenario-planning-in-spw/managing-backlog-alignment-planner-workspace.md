---
title: Prioritizing portfolio plan work in Strategic Planning Workspace
description: Review the work pipeline for your portfolio in Strategic Planning Workspace. Add, update, and rank planning items so that you can prioritize the right work for the right time.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [alignment planner workspace, portfolio planner, portfolio planning workspace, strategic planner, strategic planning workspace]
breadcrumb: [Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Prioritizing portfolio plan work in Strategic Planning Workspace

Review the work pipeline for your portfolio in Strategic Planning Workspace. Add, update, and rank planning items so that you can prioritize the right work for the right time.

## Views for prioritizing planning items

The Prioritization tab on the Planning page in Strategic Planning represents your backlog, displaying the items in your work pipeline. The Kanban and Hierarchy tabs also represent your backlog, each providing a different view of the same items. For an overview of these views, see [Prioritization in Strategic Planning](backlog-management-in-alignment-planner-workspace.md).

**Note:** The Prioritization feature is available only for portfolio plans.

## Planning items in the Prioritization tab

By default, portfolio plans show only the records that are created within the Planning Item \[sn\_align\_core\_planning\_item\] table and its child tables. Any records stored in other ServiceNow AI Platform tables aren't shown unless an integration is established.

Consider that you want to manage projects through a portfolio plan. Project records that are only stored in the Planning Item Project \[sn\_align\_project\] table are displayed in the Prioritization, Kanban, and Hierarchy tabs. But any projects created using the PPM Standard aren't shown by default because these project records are stored in the PPM Project \[pm\_project\] table. To enable their display in Strategic Planning Workspace, set up integration with PPM so that the tables of Strategic Planning are mapped to the tables of PPM.

The same is the case with Epics created using Agile Development 2.0 and SAFe applications. See [Configuring Strategic Planning with PPM, Agile 2.0, and SAFe](../../apw-internal-integrations/concept/configuring-apw-with-agile-safe-and-ppm.md).

## Prioritization features

In the Prioritization and Hierarchy tabs, you can perform the following actions:

<table id="table_vh2_spq_2xb"><thead><tr><th>

Feature

</th><th>

Description

</th><th>

Example UI

</th></tr></thead><tbody><tr><td>

[Add new planning items](../task/add-new-items-to-backlog-alignment-planner-workspace.md)

</td><td>

Add new items to your backlog directly from the Prioritization page.

 The type of planning items that you can create here depends on your portfolio plan configuration.

</td><td>

![Sample drop-down list actions showing options to select New epic and New project as a new planning item on the Prioritization page.](../images/new-planning-item.png)

</td></tr><tr><td>

[Update planning item details](../task/update-planning-item-details-from-backlog-in-alignment-planner-workspace.md)

</td><td>

Edit details of the planning items, add attachments, and collaborate on them with the stakeholders directly from the Prioritization page to facilitate smoother real-time backlog grooming.

</td><td>

 

</td></tr><tr><td>

MoSCoW values

</td><td>

Categorize planning items using the Must have, Could have, Should have, or Won't have \(MoSCoW\) values in the List and Hierarchy views. This categorization creates a baseline of priority that you can later use when you're grooming and prioritizing work for your portfolio.

</td><td>

![MoSCoW options for planning items in Strategic Planning Prioritization tab.](../images/moscow-hierarchy.png)

</td></tr><tr><td>

[Rank planning items](../task/rank-and-prioritize-backlog-alignment-planner-workspace.md)

</td><td>

Decide on the order of priority for the planning items by using the drag functionality to rearrange them.

</td><td>

 

</td></tr><tr><td>

[Prioritize items to roadmap](../task/prioritize-planning-items-strategic-planning-workspace.md)

</td><td>

Set the planning state of an item to **Prioritized** to add them to the portfolio's roadmap.

</td><td>

 

</td></tr><tr><td>

Open the planning item in the Execution app

</td><td>

If you're using ServiceNow PPM, Agile Development 2.0, or SAFe applications to execute the planned work, you can open the planning items in their own application.

 For example, if your planning item is an epic, you can navigate to the epic form directly from the Prioritization page.

</td><td>

![Open planning item in execution app from Prioritization page.](../images/open-execution-app.png)

</td></tr><tr><td>

[Personalize the Prioritization page views](../task/personalize-backlog-in-alignment-planner-workspace.md)

</td><td>

Change the way that the Prioritization page is displayed so that you can view the information in the format that you need.

 All settings, such as row and column personalization, grouping, and sorting, are saved as the portfolio plan preferences. So, these settings are applied to all the users or user groups that the portfolio plan is shared with.

</td><td>

 

</td></tr><tr><td>

Apply filters for Prioritization

</td><td>

Apply filters to all the views of Prioritization, Roadmap, Hierarchy, or Scoring so that you can view a consistent data set for your portfolio plan.

</td><td>

![Apply filters for Prioritization.](../images/apply-quick-filters-for-prioritization.png)

</td></tr><tr><td>

Reorder the columns by dragging them horizontally

</td><td>

Reorder the position of the columns in the Prioritization tab by dragging them horizontally.

</td><td>

![Reorder columns in prioritization by dragging.](../images/reorder-columns-in-prioritization-by-dragging.gif)

</td></tr></tbody>
</table>