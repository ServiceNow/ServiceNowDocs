---
title: Create a high-level portfolio plan
description: Build a portfolio plan for high-level strategic items in the Strategic Planning Workspace so that you can prioritize, roadmap, and manage work aligned to these strategic items.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage portfolio plans, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create a high-level portfolio plan

Build a portfolio plan for high-level strategic items in the Strategic Planning Workspace so that you can prioritize, roadmap, and manage work aligned to these strategic items.

## Before you begin

Role required: sn\_align\_core.apw\_user or business\_stakeholder

## About this task

By default, you can select the Strategic Investments lens and use Initiatives or Strategic Programs, or select the Project Program lens and use Programs as your high-level planning items. You can also select the Digital Product lens and use the Product Enhancement entity for high-level planning. If you want to plan using a different item, work with your admin to enable those items in your ServiceNow instance. For more information on the configuration, see [High-level planning configuration in Strategic Planning](high-level-portfolio-planning-configuration.md).

In this task, select a lens, add conditions to filter the planning item data that you need, and enter additional details to build a portfolio plan.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the Portfolio Plans page, select **New**.

    If there are no existing portfolio plans, select **Create your first portfolio plan**.

3.  Select a lens for your high-level planning.

    By default, the Strategic Investments and Project Program lenses are enabled for high-level planning.

    **Note:** Don’t select Goals lens because the Goal \[sn\_gf\_goal\] table doesn't support high-level planning.

    The Create portfolio plan wizard is shown.

4.  Make your selections by using the Create portfolio plan wizard.

    1.  For the selected lens, choose the type of work that you want to plan.

        For example, you want to manage work for initiatives in your company. Select Initiatives as your high-level planning item. This enables you to plan for initiatives and review the work aligned to these initiatives.

        ![High-level planning wizard.](../images/HLP-wizard.png)

    2.  Add conditions to further filter the data of your planning items.

        For example, you’re responsible for the initiatives of the Customer Support department. You can set a condition to filter initiatives of only the Customer Support department from the Initiative table.

        You can also add multiple conditions to help you set a complex filter and add the right information to your portfolio plan.

    3.  Fill in the details of the portfolio plan.

        Provide the information of the portfolio plan's name, owner, start and end dates, and description.

    4.  Select a scoring framework using the drop-down values or from the Scoring framework window.

        To create a custom scoring framework for your portfolio plan, select **Explore scoring frameworks**.![Select a scoring framework for your portfolio plan.](../images/scoring.png)

    Use the **Previous** and **Next** buttons to navigate between the steps.

5.  Select **Create**.


## Result

The portfolio plan is created and the page is refreshed to show the Goals, Scoring, and Planning pages. You can view the list of all portfolio plans that you own or shared with you from the Home page.

## What to do next

-   Define goals for your portfolio plan and align work to them. See [Managing goals in Strategic Planning Workspace](../../spw-goals/concept/managing-goals-in-alignment-planner-workspace.md).
-   Analyze the backlog and prioritize work for your portfolio plan. See [Prioritizing portfolio plan work in Strategic Planning Workspace](../../spw-prioritization/concept/managing-backlog-alignment-planner-workspace.md).
-   Show or hide features for your portfolio plan according to your requirement while sharing a portfolio plan with your stakeholders. See, [Show or hide the features for a portfolio plan](show-or-hide-the-features-for-your-portfolio-plan-spw.md).

**Parent Topic:**[Managing portfolio plans in Strategic Planning Workspace](../concept/managing-portfolio-plans-in-alignment-planner-workspace.md)

