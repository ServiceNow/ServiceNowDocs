---
title: Create a scenario
description: Create a scenario from a live plan or another scenario in a simulated environment to compare the scenario with the live plan and other scenarios.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Optimize planning with scenario planning, Portfolio Planning, Strategic Portfolio Management]
---

# Create a scenario

Create a scenario from a live plan or another scenario in a simulated environment to compare the scenario with the live plan and other scenarios.

## Before you begin

Role required:

-   sn\_align\_core.apw\_user
-   sn\_align\_ws.spw\_financial\_user - to view and edit financial details.

## About this task

Creating a scenario enables you to visualize and anticipate potential outcomes. You can create a scenario based on the live plan or on another existing scenario. Once you have created one or more scenarios, you can compare them side by side with the live plan and approve the most desirable scenario. The scenario you approve becomes the live plan.

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select one and then select **Planning**.

3.  Select **Create scenario**.

    **Note:** Before you have created your first scenario, you see the **Scenario planning** button on the Scenario page. In such a case, select **Scenario planning** and then you see the **Create scenario** button.

    1.  Enter a name for your scenario in the **Scenario name** field.

    2.  Enter the details of your scenario in the **Description** field.

    3.  In the **Copy From** field, select the Current Plan or the name of an existing scenario based on which you want to create the scenario.

    4.  Select **Create**.

    The Scenario planning- \[Scenario Name\] page appears with the Prioritization tab open. The Prioritization tab lists all the planning items that you have in the live plan, or in the existing scenario that you copied the scenario from. The planning item start and end dates are determined based on the dates specified in the live plan or the actual execution dates.

    -   **In Plan** toggle: By default, the **In Plan** toggle is switched on for planning items that have the planning state as Prioritized or Done and have their start dates within the portfolio plan timeline. The **In Plan** toggle is turned off for items that have the status New, In Review, or Canceled.
    -   Yellow highlights for out of range dates: The planning item dates that are out of range of the portfolio plan timeline are highlighted with a yellow background. For such items, the **In Plan** toggle is turned off.
4.  Use the Prioritization tab to include or exclude additional planning items in the scenario.

    ![Prioritization tab of the Scenario screen](../image/prioritization-tab-ppw.png)

    1.  To exclude a planning item from the scenario, turn off the **In Plan** toggle.

    2.  To include a planning item in the scenario, edit the start and end dates of the item to fall within the portfolio plan timeline, and then turn on the **In Plan** toggle.

    If you include out-of-timeline items in a scenario, these items remain in the scenario during the planning and prioritization process. When the scenario is approved, the dates of these items are updated to align with the scenario dates. However, because these updated dates fall outside the original portfolio plan timeline, the items are moved out of the live portfolio plan.

5.  Use the **Roadmap** tab to view planning item dependencies and adjust planning item dates:

    ![Roadmap tab of the Scenario screen](../image/roadmap-tab-create-scenario-ppw.png)

    1.  Drag the start or end of the planning item bars to change their start or end dates.

    2.  Drag the planning item bars to shift them in the plan timeline.

    3.  View the dependencies and milestones of the various planning items.

6.  Use the **Financials** tab view the prioritize, invest, and execute the right items to provide best returns on investments for your organization.

    ![Financials tab in Scenario planning.](../../spw-scenario-planning/image/financials-tab-in-strategic-planning.png)

    1.  Set target for your portfolio budget.

        1.  Select the **Set Targets** \(![Set target button.](../../spw-financials/images/fin-set-targets-button.png)\) button.
        2.  In the Set Targets window, set budget for an expense type or a cost type using the inline edit feature.

            **Tip:** You can change the **Time scale** and **Range** to set targets for each fiscal period at monthly, quarterly, or yearly cadence to meet your organization's planning cycle. The target set for a higher timescale, it is equally split it between the fiscal periods.

        Once the target is set for a scenario, the **Target** row displays the defined target amount by fiscal period and budget allocation choices.

    2.  Include or exclude planning items in scenario using the **In-plan** toggle.

    3.  Add or reduce budget for individual planning items using the inline editing feature.

        Changes made to the budget using while creating a scenario are marked with ![Analog time indicator inside an incomplete circle with arrow ending indicating unapproved changes](../../spw-financials/images/fin-inline-edit-icon.png) icon.


## What to do next

-   Create more scenarios, if necessary.
-   [Compare scenarios](compare-scenarios-in-portfolio-planning.md). You can directly compare scenarios from simulation mode by selecting **Compare scenarios** from the Scenario actions list.
-   [Approve a scenario](approve-a-scenario-in-portfolio-planning.md).

