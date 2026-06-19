---
title: Add targets for a goal in Strategic Planning
description: Create SMART targets for goals to track and measure the progress of your goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/scenario-planning-in-spw/set-targets-for-goal-egm.html
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage portfolio plan goals, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Add targets for a goal in Strategic Planning

Create SMART targets for goals to track and measure the progress of your goals.

## Before you begin

Role required: sn\_apw\_advanced.spw\_goal\_user and \(sn\_align\_core.apw\_user or sn\_gf.goal\_admin\)

## About this task

If you’re using Now Assist for SPM, you can use the Target generation skill to generate targets for a goal. The skill uses the goal’s details and provided context to create a precise target for the goal. The more specific the input, the stronger the recommendations. For details, see [Generate targets for a goal in Strategic Planning Workspace using Now Assist for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/now-assist-for-strategic-portfolio-management-spm/generate-targets-for-goal.md).

Configuring a target source for your target updates the **Actuals to date** field on the Target form automatically. For more information on target automation, see [Target actuals automation in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/target-actuals-automation-spw.md).

A SMART target can be defined as S = Specific, M = Measurable, A = Attainable, R = Relevant, and T = Time-bound.

**Note:**

-   Only the owner or contributors of the goal can create targets for the goal.
-   You can also restrict the access for a target record to the specific users by enabling the **Confidential** field on the Target form if the ServiceNow® ESG Management application is installed.

## Procedure

1.  Create a target for a goal using one of the following options.

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d194322e120">

Option

</th><th align="left" id="d194322e123">

Steps

</th></tr></thead><tbody><tr><td id="d194322e129">

**From the Goals view**

</td><td>

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.
2.  From the list of portfolio plans, select the required portfolio plan that the goal belongs to.
3.  In the Goals view, select the **Goals and targets** tab.
4.  Next to the goal that you want to create a target for, select the row context menu icon \(\[Omitted image "action-menu-icon.png"\] Alt text: Row context menu icon.\) and select **Add target**.


</td></tr><tr><td id="d194322e177">

**From the Targets tab**

</td><td>

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.
2.  From the list of portfolio plans, select the required portfolio plan that the goal belongs to.
3.  In the Goals view, select the **Goals and targets** tab.
4.  Select the goal that you want to create a target for.

The Goal side panel opens with the **Details** tab.

5.  From the side pane, select **Full Details** to open the goal form.
6.  On the **Quantitative Targets** or **Qualitative Targets** tab, select **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    For a description of the field values, see [Target form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/target-form-egm.md).

3.  Select **Save**.

    You can also select **Save and add new target** and add more targets for the goal on the flow.


## Result

The target progress records are automatically created when you save the target post populating the **Actuals to date** field. The target progress records specify the progress of each target for the goal.

**Note:** When you delete a goal, its associated targets \(if any\) and their progress records are also deleted even though the **Allow the deletion of targets** property is set to **No**.

## What to do next

[Update the progress of the target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/update-progress-of-target-egm.md) manually if the target is not enabled for target automation.

