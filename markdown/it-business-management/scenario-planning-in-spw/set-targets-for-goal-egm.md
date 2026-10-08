---
title: Add targets for a goal in Strategic Planning
description: Create targets to track and measure progress toward your goals. Select a target type that matches the direction of each goal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/set-targets-for-goal-egm.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 3
breadcrumb: [Manage portfolio plan goals, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Add targets for a goal in Strategic Planning

Create targets to track and measure progress toward your goals. Select a target type that matches the direction of each goal.

## Before you begin

Role required: sn\_apw\_advanced.spw\_goal\_user and \(sn\_align\_core.apw\_user or sn\_gf.goal\_admin\)

## About this task

If you're using ServiceNow Otto for SPM, you can use the Target generation skill to generate targets for a goal. The skill uses the goal's details and provided context to generate a target for the goal. Review AI-generated targets for accuracy before you save them. For details, see [Generate targets for a goal in Strategic Planning Workspace using ServiceNow Otto for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/generate-targets-for-goal.md).

Configuring a target source for your target updates the **Actuals to date** field on the Target form automatically. For more information about target automation, see [Target actuals automation in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-actuals-automation-spw.md).

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

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d296612e148">

Option

</th><th align="left" id="d296612e151">

Steps

</th></tr></thead><tbody><tr><td id="d296612e157">

**From the Goals view**

</td><td>

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.
2.  From the list of portfolio plans, select the portfolio plan that the goal belongs to.
3.  In the Goals view, select the **Goals and targets** tab.
4.  Next to the goal, select the row context menu icon \[Omitted image "action-menu-icon.png"\] Alt text: and select **Add target**.


</td></tr><tr><td id="d296612e204">

**From the Targets tab**

</td><td>

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.
2.  From the list of portfolio plans, select the portfolio plan that the goal belongs to.
3.  In the Goals view, select the **Goals and targets** tab.
4.  Select the goal.

The Goal side panel opens with the **Details** tab.

5.  From the side panel, select **Full Details** to open the Goal form.
6.  On the **Quantitative Targets** or **Qualitative Targets** tab, select **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    For a description of the field values, see [Target form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-form-egm.md). In the **Type** field, select the target type that matches the direction of your goal.

3.  For Maintain-type targets, set up the check-in frequency to track performance across time periods.

    Maintain-type targets require periodic check-ins to track how often the metric stays within, above, or below the threshold. For example:

    -   Maintain above service uptime: Set check-in frequency to **Monthly** to track monthly uptime performance.
    -   Maintain constant staffing: Set check-in frequency to **Quarterly** to verify headcount stays within the tolerance band each quarter.
    For Maximize and Minimize targets, check-in frequency is optional.

4.  Select **Save**.

    You can also select **Save and add new target** to save this target and add another target for the goal.


## Result

Target progress records are created automatically when you save the target after you populate the **Actuals to date** field. The target progress records specify the progress of each target for the goal. Status is automatically calculated based on the target type and achievement criteria. For Maintain-type targets, status reflects the percentage of periods that meet the target criteria.

**Note:** When you delete a goal, its associated targets \(if any\) and their progress records are also deleted even if the **Allow the deletion of targets** property is set to **No**.

## What to do next

[Update the progress of the target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/update-progress-of-target-egm.md) manually if the target is not enabled for target automation. For Maintain-type targets with check-in frequency, enter the actual value for each time period to track achievement across the breakdown periods.

