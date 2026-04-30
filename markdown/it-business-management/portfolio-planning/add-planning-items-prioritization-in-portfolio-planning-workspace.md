---
title: Add planning items to Prioritization page in Portfolio Planning Workspace
description: Add new planning items to your portfolio plan's work backlog in Portfolio Planning Workspace and ensure that the work pipeline is current.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Prioritize portfolio plan work, Portfolio Planning, Strategic Portfolio Management]
---

# Add planning items to Prioritization page in Portfolio Planning Workspace

Add new planning items to your portfolio plan's work backlog in Portfolio Planning Workspace and ensure that the work pipeline is current.

## Before you begin

[Create a portfolio plan](create-portfolio-plan-in-portfolio-planning-workspace.md).

Role required: sn\_align\_core.apw\_user

## About this task

Use the Prioritization page of your portfolio plan to add new planning items or import them from other ServiceNow execution system such as Project Portfolio Management \(PPM\).

You can use the List or Hierarchy views while you perform this task.

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select one and then select **Planning**.

3.  From the Prioritization page, add a new planning item for your portfolio plan.

    Use the More options drop-down to select the planning item that you want to create.

    ![Sample drop-down list actions showing options to select New epic and New project as a new planning item on the Prioritization page.](../../spw-prioritization/images/new-planning-item.png)

4.  On the form, fill in the short description and approved dates.

    For full field information, see [Demand planning item form](../reference/demand-form-portfolio-planning.md) or [Project planning item form](../reference/project-form-portfolio-planning.md).

5.  Select **Submit**.

6.  If you're using PPM to execute the planned work, you can also import your work items from the application.

    For more information, see [Executing Portfolio Planning work in PPM](../concept/executing-portfolio-planning-with-ppm.md).


## Result

The new item is created with its **Planning state** field is set to **New** and the position of the item is based on the view that you are in.

-   List view: Added to the bottom of the list.
-   Hierarchy view: Added to the appropriate grouping. For example, your selected lens is Organization. Then, the new item is added to the grouping of its department.

## What to do next

-   [Rank planning items in Portfolio Planning Workspace](rank-and-prioritize-work-portfolio-planning-workspace.md).
-   [Update planning item details from Prioritization view](modify-planing-item-details-from-prioritization-portfolio-planning-workspace.md).

