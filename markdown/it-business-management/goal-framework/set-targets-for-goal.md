---
title: Create targets for a goal using Goal Framework or Goal Framework for SPM
description: Create SMART targets for goals to track and measure the progress of the goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/goal-framework/set-targets-for-goal.html
release: brazil
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Manage goals, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Create targets for a goal using Goal Framework or Goal Framework for SPM

Create SMART targets for goals to track and measure the progress of the goals.

## Before you begin

Role required: sn\_gf.goal\_user or sn\_gf.goal\_admin

## About this task

SMART targets are specific, measurable, attainable, relevant, and time-bound. When selecting a target type, consider your goal's direction:

-   **Maximize**: Use for goals when the goal is to increase a metric \(for example, revenue, customer satisfaction\).
-   **Minimize**: Use for goals when the goal is to decrease a metric \(for example, costs, defects\).
-   **Maintain above**: Use for goals where a metric must stay above a threshold \(for example, service uptime, compliance rating\).
-   **Maintain below**: Use for goals where a metric must stay below a threshold \(for example, operating costs cap\).
-   **Maintain constant**: Use for goals where a metric must stay stable within a tolerance range \(for example, staffing levels, quality scores\).
-   **Milestone**: Use for qualitative goals with Yes/No achievement status \(for example, project completion, regulatory approval\).

**Note:**

-   Only the owner or contributors of the goal can create targets for the goal.
-   You can also restrict access to a target record to specific users by selecting the **Confidential** check box on the Target form if the Operational Sustainability Management application is installed.

## Procedure

1.  Create a target for a goal using one of the following options.

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d105976e122">

Option

</th><th align="left" id="d105976e125">

Steps

</th></tr></thead><tbody><tr><td id="d105976e131">

**From the Targets related list**

</td><td>

1.  Navigate to **Enterprise Goal Management** &gt; **Goals**.
2.  Open the required goal that you want to set a target for.
3.  In the Quantitative Targets or Qualitative Targets related list, click **New**.


</td></tr><tr><td id="d105976e164">

**From the Targets module**

</td><td>

1.  Navigate to **Enterprise Goal Management** &gt; **Targets**.
2.  Click **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    For a description of the field values, see [Target form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/target-form.md). In the **Type** field, select the target type that matches the direction of your goal.

3.  For Maintain-type targets, set up the check-in frequency to track performance across time periods.

    Maintain-type targets require periodic check-ins to track how often the metric stays within, above, or below the threshold. For example:

    -   Maintain above service uptime: Set check-in frequency to **Monthly** to track monthly uptime performance.
    -   Maintain constant staffing: Set check-in frequency to **Quarterly** to verify headcount stays within the tolerance band each quarter.
    For Maximize and Minimize targets, check-in frequency is optional.

4.  Click **Submit**.


## Result

The target progress records are automatically created when you save the target post populating the **Actuals to date** field. The target progress records specify the progress of each target for the goal.

**Note:** When you delete a goal, its associated targets \(if any\) and their progress records are also deleted even though the **Allow the deletion of targets** property is set to **No**.

## What to do next

[Update the progress of the target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/update-progress-of-target.md) manually if the target is not enabled for target automation. For Maintain-type targets with check-in frequency, enter the actual value for each time period to track achievement across the breakdown periods.

