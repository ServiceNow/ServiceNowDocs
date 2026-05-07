---
title: Add a target for goal
description: Create SMART targets for goals to track and measure the progress of your goals.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage enterprise goals, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Add a target for goal

Create SMART targets for goals to track and measure the progress of your goals.

## Before you begin

Role required: sn\_apw\_advanced.spw\_goal\_user

## About this task

If you’re using Now Assist for SPM, you can use the Target generation skill to generate targets for a goal. The skill uses the goal’s details and provided context to create a precise target for the goal. The more specific the input, the stronger the recommendations. For details, see [Generate targets for a goal in Strategic Planning Workspace using Now Assist for SPM](../../now-assist-spm/task/generate-targets-for-goal.md).

Configuring a target source for your target updates the **Actuals to date** field on the Target form automatically. For more information on target automation, see [Target actuals automation in Strategic Planning](../../spw-goals/concept/target-actuals-automation-spw.md).

A SMART target can be defined as S = Specific, M = Measurable, A = Attainable, R = Relevant, and T = Time-bound.

**Note:**

-   Only the owner or contributors of the goal can create targets for the goal.
-   You can also restrict the access for a target record to the specific users by enabling the **Confidential** field on the Target form if the ServiceNow® Operational Sustainability Management application is installed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Strategy and Goals**.

2.  On the Strategy and Goals page, select the strategy-based board or goal-based board for which your goal belongs to.

    The Strategy page opens if selected a strategy-based or combined strategy and goals-based board. The Goals page opens if selected a goals-based board.

3.  Add a target for your goal using one of the following methods depending on your board type.

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d138277e146">

Option

</th><th align="left" id="d138277e149">

Steps

</th></tr></thead><tbody><tr><td id="d138277e155">

**From the Goals page**

</td><td>

Next to the goal that you want to add a target for, select the row context menu icon \(![Row context menu icon.](../../alignment-planner-workspace/images/action-menu-icon.png)\) and select **Add target**.

</td></tr><tr><td id="d138277e173">

**From the Strategy page**

</td><td>

1.  From the list of strategic priorities, select the one for which your goal belongs to.

The strategic priority details page opens.

2.  Select the **Goals** tab.
3.  From the list of goals, select the goal for which you want to add a target.

The goal details page opens.

4.  Select the **Qualitative Targets** or **Quantitative Targets** tab.
5.  Select **New**.


</td></tr></tbody>
</table>4.  On the form, fill in the fields.

    For a description of the field values, see [Target form](../../spw-goals/reference/target-form-egm.md).

5.  Select **Save**.

    If you are adding a target from the New target window on the Goals page, you can also select **Save and add a new target** and add more targets for the goal on the flow.


## Result

The target progress records are automatically created when you save the target post populating the **Actuals to date** field. The target progress records specify the progress of each target for the goal.

**Note:** When you delete a goal, its associated targets \(if any\) and their progress records are also deleted even though the **Allow the deletion of targets** property is set to **No**.

## What to do next

[Update the progress of the target](update-progress-of-target-strategy.md) manually if the target isn’t enabled for target automation.

**Related topics**  


[Create a goal](create-goal-strategy.md)

[Duplicate a goal or target](duplicate-goal-target-strategy.md)

[Align work with a goal or target](associate-work-with-goals-strategy.md)

[Create a strategic plan](create-strategic-plan-strategy.md)

[Create a strategic priority](create-strategic-priority-strategy.md)

[Send a reminder for target actuals check in](send-reminder-target-checkin-strategy.md)

