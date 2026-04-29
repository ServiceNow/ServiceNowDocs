---
title: Exploring Goal Framework and Goal Framework for SPM
description: The Goal Framework application helps you create goals, set targets for them, and evaluate the progress of the goals and targets to accomplish your organizational plans and drive business outcomes.
locale: en-US
release: australia
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Exploring Goal Framework and Goal Framework for SPM

The Goal Framework application helps you create goals, set targets for them, and evaluate the progress of the goals and targets to accomplish your organizational plans and drive business outcomes.

The Goal Framework for Strategic Portfolio Management \(SPM\) application enables you to automate the actual value of your targets by collecting the actuals from different target sources such as benefit plans, cost plans, assessments/surveys, and PA Indicators.

-   **Goal Framework key components:**
    -   Strategic priorities: Actions of a strategic plan that help to orient your organizational strategic plan toward your goal.
    -   Goals: Objectives that you want to reach based on your strategic plans.
    -   Targets: Targets for goals to track and measure the progress of the goals.
-   **Goal Framework for SPM key component:**

    Target source is the key component of Goal Framework for SPM. Target source is a configuration for a target that is used to auto-update the actual value of the target, so that the progress of the target and its goal is auto-updated.


## Strategic priorities

Strategic priorities are the objectives of your organizational plans. Strategic priorities help you to achieve your goals over a designated time period. The strategic priorities are also known as focus areas or long-term strategies. Defining strategic priorities helps to orient your organizational strategic plans toward your goals.

## Goals

Goals refer to objectives that an organization sets for itself to accomplish their organizational plans. Goals are typically qualitative in nature. Goals should be ambitious and are expected to motivate and challenge your teams. Some examples of goals are as follows:

-   Using renewable energy by the end of the year 2022.
-   Increase diversity in the workplace by 50 percent.

A goal can also have sub-goals. You can also associate work and planning items to a goal so that you can track who is responsible for fulfilling the goal.

If you use Goal Framework with other products, you can also do the following:

-   If you're a ServiceNow® Project Portfolio Management user, you can associate demands, projects, and programs with a goal to capture the work being done to meet your goal.
-   If you're a ServiceNow® Agile Development 2.0 user, you can associate scrum epics with a goal to capture the work being done to meet your goal.
-   If you're a ServiceNow® Scaled Agile Framework \(SAFe\) user, you can associate SAFe epics and SAFe features with a goal to capture the work being done to meet your goal.
-   If you're a Strategic Planning user, you can associate planning items - Demand, Project, and Epic, and strategic items - Program and Initiative - with a goal to capture the work being done to meet your goal.

## Targets

Targets help you to measure your goal. For example, to meet the goal of increasing diversity in the workplace by 50 percent, the target can be to hire a 30 percent-diverse workforce by the first quarter of 2022.

Targets can be set as a quantitative or qualitative by defining the unit of measure for the target. Quantitative targets are numbers-based, countable, and measurable. Qualitative targets are interpretation-based, descriptive, typically yes or no type.

You can also breakdown a target into smaller periods \(example, Quarterly\) which helps you set a target for each quarter and focus on the specific breakdown targets. The target breakdowns are automatically created based on the breakdown interval set for the target. For details on how the target breakdowns feature works, see [Target breakdowns](target-breakdowns-gf.md).

-   **Qualitative targets**

    Qualitative targets are typically non-measurable but can be tracked whether the target has been achieved. The available unit of measure for qualitative targets is Yes/No. You can also define a custom unit of measure \(for the available choice set\) for qualitative targets as per your need and set qualitative targets for your goals.

    For example, to achieve a target of conducting hackathon in Q2-2023, the target can be set as conduct hackathon in Q2-2023 with the unit of measure Yes/No. Base and target value of the target can be No and Yes respectively. After the target is successful with the hackathon event, the target value can be updated to Yes.


## Target sources

Target source is a configuration for a target that is used to auto-update the actual value of the target, so that the progress of the target and its goal is auto-updated. Any table or a combination of tables \(for example, benefit plans, cost plans, surveys, incidents, and PA indicators\) present on the ServiceNow AI Platform® can be configured as a target source.

The following target source types are supported for automating the actual value of a target.

-   PA Indicator: Updates the **Actual value** field on the target form by fetching the required data from the PA Indicator.
-   Assessment/Survey: Updates the **Actual value** field on the target form by fetching the required data from the Assessment metric type and Assessment metric category records.
-   Custom script: The Custom script fetches the required data from any ServiceNow AI Platform table that is configured. With the Custom script option, any table or a combination of tables present on the ServiceNow AI Platform can be configured as a target source.

    [Predefined target automation script for benefit plans](../reference/target-automation-script-benefit-plans.md): The predefined, default script is a target source that updates the **Actual value** field on the target form by fetching the value from the **Actual benefit** field or **Non-monetary actual benefit** field from the monetary or non-monetary benefit plans of relevant work items.


-   **Context variable**

    The context variable is an additional configuration for the target source. The context variable provides information that can be used on the target form to fetch the required data and update the **Actual value** field on the Target form. The context variable is required for target source types Assessment/Survey and PA Indicator. If the Goal Framework for SPM scope is selected while creating a target source, the context variable is automatically created for the target source \(of type Assessment/Survey and PA Indicator\). For more information on context variables, see [Context variable in target source](context-variable-in-target-source.md).


## Benefits and workflow

Use the Goal Framework or Goal Framework for SPM application to do the following activities:

-   Create a strategic plan for your organization \(If Strategic Planning is installed\). For more information, see [Create a strategic plan](../task/create-strategic-plan.md).
-   Create a strategic priority to orient your organization strategic plan toward your goal. For more information, see [Create a strategic priority for a strategic plan](../task/create-strategic-priority.md).
-   Create a goal. For more information, see [Create a goal](../task/create-goal.md).
-   \(For Goal Framework users\) Set targets for a goal to track and measure the progress of the goal. For more information, see [Set targets for a goal](../task/set-targets-for-goal.md).
-   \(For Goal Framework for SPM users\) Set targets and automate the actual value of the targets. For more information, see [Configuring target source for target automation using Goal Framework for SPM](setting-targets-for-a-goal-and-automating-the-actual-value-using-agf.md).
-   Create a goal relationship with a work, planning, strategic, or any other item to identify and associate your current or future work and achieve your goals. For more information, see [Associate a work or planning item with goals or targets](../task/associate-work-with-goals.md).
-   Associate the primary goal for a work and planning item. For more information, see [Associate the primary goal for work and planning items](associating-primary-goal.md).

For an example of the structure of a strategy from the strategic plan level down to targets, see [Enterprise strategy example](enterprise-goal-example-strategy-gf.md).

## Comparing Goal Framework with Goal Framework for SPM

-   Goal Framework: Create goals, set targets for them, and evaluate the progress of the goals and targets to accomplish the organizational plans and drive business outcomes.
-   Goal Framework for SPM: Automate the actual value of your targets by collecting the actuals from different target sources such as benefit plans, cost plans, assessments/surveys, and PA Indicators.

|Feature|Goal Framework|Goal Framework for SPM|
|-------|--------------|----------------------|
|Create strategic plans|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Create strategic priorities|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Create goals|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Set targets|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Set target breakdowns|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Associate work with goals|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Automate actual value of targets|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Monitor goals and strategies in ServiceNow AI Control Tower|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|

**Note:** The Goal Framework for SPM application is an extension to the Goal Framework application. When you install the Goal Framework for SPM application, you get all the features of Goal Framework as well as the target automation feature.

