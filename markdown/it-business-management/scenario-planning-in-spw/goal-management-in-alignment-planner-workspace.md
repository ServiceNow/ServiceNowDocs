---
title: Goals in Strategic Planning
description: Create goals for your portfolio plan, set targets for them, and evaluate the progress of these goals and targets to accomplish your organizational plans and drive business outcomes.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Explore, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Goals in Strategic Planning

Create goals for your portfolio plan, set targets for them, and evaluate the progress of these goals and targets to accomplish your organizational plans and drive business outcomes.

Goals key components:

-   Goals: Objectives that you want to reach based on your strategic plans.
-   Targets: Targets for goals to track and measure the progress of the goals.
-   Target source: A configuration for a target to auto-update the actual value of the target.

## Goals

Goals refer to objectives that an organization sets for itself to accomplish their organizational plans. Goals are typically qualitative by nature. Goals should be ambitious and are expected to motivate and challenge your teams. Some examples of goals are as follows:

-   Using renewable energy by the end of the year 2022.
-   Increase diversity in the workplace by 50 percent.

A goal can also have subgoals. You can associate work \(planning items\) to a goal so that you can track who is responsible for fulfilling the goal.

You can associate planning items - Demand, Project, and Epic, and strategic items - Program and Initiative - with a goal to capture the work being done to meet your goal.

## Targets

Targets help you measure your goal. For example, to meet the goal of increasing diversity in the workplace by 50 percent, the target can be to hire a 30 percent diverse workforce by the first quarter of 2022.

Targets can be quantitative or qualitative, by defining the unit of measure for the target. Quantitative targets are numbers-based, countable, and measurable. Qualitative targets are interpretation-based, descriptive, and typically a yes or no type.

You can also break down a target into smaller periods \(for example, Quarterly\), which helps you set a target for each quarter and focus on the specific breakdown targets. The target breakdowns are automatically created based on the breakdown interval set for the target. For details on how the target breakdowns feature works, see [Target breakdowns in Strategic Planning](target-breakdowns.md).

-   **Qualitative targets**

    Qualitative targets are typically non-measurable but can be tracked if the target has been achieved. The available unit of measure for qualitative targets is Yes/No. You can also define a custom unit of measure \(for the available choice set\) for qualitative targets according to your need and set qualitative targets for your goals.

    For example, to achieve a target of conducting a hackathon in Q2-2023, the target can be set as conduct a hackathon in Q2-2023 with the unit of measure Yes/No. The base and target value of the target can be No and Yes, respectively. After the target is successful with the hackathon event, the target value can be updated to Yes.


## Target sources

A target source is a configuration for a target to auto-update the actual value of the target, so that the progress of the target and its goal are auto-updated. Any table or a combination of tables \(for example, benefit plans, cost plans, surveys, incidents, and PA indicators\) present on the ServiceNow AI Platform® can be configured as a target source.

The following target source types are supported for automating the actual value of a target:

-   PA Indicator: Updates the **Actual to date** field on the target form by fetching the required data from the PA Indicator.
-   Assessment/Survey: Updates the **Actual to date** field on the target form by fetching the required data from the Assessment metric type and Assessment metric category records.
-   Custom script: The Custom script fetches the required data from any ServiceNow AI Platform table that is configured. With the Custom script option, any table or a combination of tables present on the ServiceNow AI Platform can be configured as a target source.

    [Predefined target automation script for benefit plans](../reference/target-automation-script-benefit-plans-apw.md): The predefined, default script is a target source that updates the **Actual to date** field on the target form by fetching the value from the **Actual benefit** field or **Non-monetary actual benefit** field from the monetary or non-monetary benefit plans of relevant work items.


-   **Context variable**

    The context variable is an additional configuration for the target source. The context variable provides information that can be used on the Target form to fetch the required data and update the **Actual to date** field on the Target form. The context variable is required for target source types Assessment/Survey and PA Indicator. If the Goal Framework for SPM scope is selected while creating a target source, the context variable is automatically created for the target source \(of type Assessment/Survey and PA Indicator\). For more information on context variables, see [Context variable in target source](context-variable-in-target-source-apw.md).

    ![Example goals view with multiple goals and targets.](../images/goals-module-example-view-exploring.png "Example goals view")


## Goals workflow in Strategic Planning

Using the Goals view in the Strategic Planning Workspace, you can do the following activities:

-   Create a goal for an entity such as company, business unit, department, and so on. For more information, see [Create a goal in Strategic Planning](../task/create-goal-egm.md).
-   Set targets and automate the actual value of the targets. For more information, see [Create targets for a goal in Strategic Planning](../task/set-targets-for-goal-egm.md).

    **Note:**

    -   Automating the actual value of the targets is optional. If you don't want to automate the actual value of your targets, you can still update the actual value of the targets manually.
    -   You can also generate targets for your goals using the Target generation skill, if the Now Assist for SPM application is installed.
-   Associate a planning item with goals. For more information, see [Associate a planning item with goals or targets](../task/associate-work-with-goals-egm.md).
-   Associate or update the primary goal for a planning item. For more information, see [Associate or update the primary goal or target for a planning item](../task/associate-update-primary-goal-egm.md).

For more information on how to define and manage your goals in Strategic Planning see [Managing goals in Strategic Planning Workspace](managing-goals-in-alignment-planner-workspace.md).

**Parent Topic:**[Exploring Portfolio Planning in Strategic Planning Workspace](../../alignment-planner-workspace/concept/alignment-planner-workspace.md)

