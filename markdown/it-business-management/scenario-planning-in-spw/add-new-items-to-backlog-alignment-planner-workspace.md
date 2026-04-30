---
title: Add planning items to Prioritization page of Strategic Planning Workspace
description: All references to "Backlog" are changed to "Prioritization" following the change of the feature name in the app.Add new planning items to your portfolio plan's work backlog in Strategic Planning Workspace and ensure that the work pipeline is current.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Prioritize portfolio plan work, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Add planning items to Prioritization page of Strategic Planning Workspace

Add new planning items to your portfolio plan's work backlog in Strategic Planning Workspace and ensure that the work pipeline is current.

## Before you begin

[Create a portfolio plan in Strategic Planning](../../alignment-planner-workspace/task/create-portfolio-plans-in-alignment-planner-workspace.md)

Role required: sn\_align\_core.apw\_user

## About this task

Use the Prioritization page of your portfolio plan to add new planning items or import them from other ServiceNow execution system such as PPM, Agile Development 2.0, or SAFe.

You can use the List, Kanban, or the Hierarchy views while you perform this task.

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select one and then select **Planning**.

3.  From the Prioritization page, add a new planning item for your portfolio plan.

    Use the More options drop-down to select the planning item that you want to create.

    ![Sample drop-down list actions showing options to select New epic and New project as a new planning item on the Prioritization page.](../images/new-planning-item.png)

4.  On the form, fill in the short description and approved dates.

    For full information, see [Planning item form](../../alignment-planner-workspace/reference/planning-item-form.md).

    You can refine planning item descriptions—for item types such as Demand, Epic, Project, Capability, Feature, and Story—using the Write planning item skill, if the Now Assist for SPM application is installed.

5.  Select **Submit**.

6.  If you're using PPM, Agile Development 2.0, or SAFe to execute the planned work, you can also import your work items from these applications.

    For more information, see [Executing Strategic Planning work in PPM, Agile 2.0, and SAFe](../../apw-internal-integrations/concept/using-apw-with-agile-safe-and-ppm.md).


## Result

The new item is created with its **Planning state** field is set to **New** and the position of the item is based on the view that you are in.

-   List view: Added to the bottom of the list.
-   Kanban view: Added to the **4-Low priority** horizontal lane.
-   Hierarchy view: Added to the appropriate grouping.

    For example, your selected lens is Organization. Then, the new item is added to the grouping of its department.


## What to do next

-   [Rank planning items in Strategic Planning](rank-and-prioritize-backlog-alignment-planner-workspace.md).
-   [Update planning item details from Prioritization page of Strategic Planning Workspace](update-planning-item-details-from-backlog-in-alignment-planner-workspace.md).
-   Learn about [Personalizing Prioritization page views in Strategic Planning](../concept/personalize-prioritization-page-in-strategic-planinng-workspace.md)

