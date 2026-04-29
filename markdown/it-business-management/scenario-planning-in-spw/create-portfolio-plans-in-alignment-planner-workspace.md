---
title: Create a portfolio plan
description: Use lens and build a personalized portfolio plan in Strategic Planning Workspace so that you can start to prioritize and align work.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [alignment planner workspace, strategic planner, portfolio planning workspace, strategic planning workspace, portfolio planner]
breadcrumb: [Manage portfolio plans, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Create a portfolio plan

Use lens and build a personalized portfolio plan in Strategic Planning Workspace so that you can start to prioritize and align work.

## Before you begin

Role required: sn\_align\_core.apw\_user or business\_stakeholder

## About this task

Use a four-step wizard to select a lens, add conditions to filter the planning items that you need, and enter additional details to create a portfolio plan.

\(For Enterprise Architecture Workspace users only\) You must install Enterprise Architecture Workspace to create a portfolio plan using the Business Capability lens. You must have the sn\_apm.apm\_user role to create a portfolio plan using the Business Capability lens.

This task guides you on creating a regular work item-level portfolio plan. To create high-level portfolio plans, see [Create a high-level portfolio plan](high-level-portfolio-plan-strategic-wkspc.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the Portfolio Plans page, select **New**.

    If there are no existing plans, select **Create your first portfolio plan**.

3.  Make your selections by using the Create Portfolio plan wizard.

    1.  Select a lens.

    2.  For the selected lens, choose an entity type and the desired entities of that type.

        The entity type represents the level that you plan your work in.

        For example, to plan work for the HR department, select the **Organization** as lens, **Department** as your entity type, and **HR** from the list of departments. This selection ensures that only the work associated with the HR department is added to your portfolio plan.

    3.  Select the type of planning items that you want to include in your portfolio plan.

        You can further filter the planning item data with additional conditions.

        For example, to plan and track progress for all HR projects created this year, select **Project** as your planning item and add a condition to filter all the HR projects created this year.

        You can also add multiple conditions to set a complex filter and add the right planning items to your portfolio plan.

        ![Select planning items and add conditions for portfolio plan.](../images/portfolio-plan-wizard.png)

    4.  Fill in the details of the portfolio plan.

        Provide the portfolio plan's name, owner, start and end dates, and description.

        **Important:** The start and end dates for your portfolio plan act as a date range filter for all the planning items that get added to the plan.

        For example, if your portfolio plan spans from March 1, 2023, to July 6, 2024, then the projects approved with start and end dates in Feb 2023 won't appear in the plan, despite meeting the "created in 2023" criteria.

    5.  Select a scoring framework using the drop-down values or from the Scoring framework window.

        To create a custom scoring framework for your portfolio plan, select **Explore scoring frameworks**.![Select a scoring framework for your portfolio plan.](../images/scoring.png)

    You can use **Previous** and **Next** to navigate between the steps.

4.  Select **Create**.


## Result

The portfolio plan is created and the page is refreshed to show the Goals, Scoring, and Planning pages for this new portfolio plan. You can view the list of all portfolio plans that you own or are shared with you from the Home page.

Planning items that meet the following criteria appear in the portfolio plan:

-   Planning items that belong to one of the entity types selected in Step 3\(b\)
-   Planning items that match the planning item types selected in Step 3\(c\)
-   Planning items with an approved start date or an end date that falls within the portfolio plan timeline
-   Planning items that don't have both Approved start and Approved end dates

**Note:** If any demands were converted into projects in Project Portfolio Management, only the resulting project planning items \(converted from demands\) appear in the portfolio plan.

## What to do next

-   Define goals for your portfolio plan and align your work to them. See [Managing portfolio plan goals in Strategic Planning Workspace](../../spw-goals/concept/managing-goals-in-alignment-planner-workspace.md).
-   Analyze the backlog and prioritize work for your portfolio plan. See [Prioritizing portfolio plan work in Strategic Planning Workspace](../../spw-prioritization/concept/managing-backlog-alignment-planner-workspace.md).
-   Show or hide features for your portfolio plan according to your requirement while sharing a portfolio plan with your stakeholders. See, [Show or hide the features for a portfolio plan](show-or-hide-the-features-for-your-portfolio-plan-spw.md).

