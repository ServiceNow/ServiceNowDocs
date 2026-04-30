---
title: Goal Preferences form
description: Use the Goal Preferences form to manage goals such as the calendar type used for goal setting, weighted average calculation for goal progress, and deletion of goals and targets.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Form field information for Strategic Planning, Reference, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Goal Preferences form

Use the Goal Preferences form to manage goals such as the calendar type used for goal setting, weighted average calculation for goal progress, and deletion of goals and targets.

<table id="table_demand_benefit_plan_form"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable the weighted average logic to calculate the progress of goals from their sub-goals and targets.

</td><td>

When enabled, the fields, **Impact on parent goal** and**Impact on goal** appear in the Goal \[sn\_gf\_goal\] and Target \[sn\_gf\_goal\_target\] tables respectively. The progress value of the parent goal is calculated by applying the Weighted Average logic.The default value is **Yes**.

 The progress value of a parent goal is calculated based on the progress value and the value defined in the **Impact on parent goal** and**Impact on goal** fields for sub-goals and targets respectively.

 For more information on how the progress value is calculated, see [progress value calculation](../../goal-framework/concept/progress-value-calculation.md).

</td></tr><tr><td>

Allow deletion of goals.

</td><td>

Can delete the goals.The default value is **Yes**.

</td></tr><tr><td>

Allow deletion of targets.

</td><td>

Can delete the targets.The default value is **Yes**.

 **Note:** When you delete a goal, its associated targets \(if any\) are also deleted even though the **Allow the deletion of targets** property is set to **No**.

</td></tr><tr><td>

Calendar type used for setting goals.

</td><td>

Calendar type that is used for setting goals. The available calendar types are Gregorian calendar and Fiscal period.The default value is **Gregorian calendar**.

</td></tr><tr><td>

Disable target breakdowns at the instance level.

</td><td>

Can disable the target breakdowns feature. When the feature is enabled, target breakdowns are automatically created based on the breakdown interval set for the target.The default value is false.

</td></tr></tbody>
</table>**Parent Topic:**[Form field information for Strategic Planning](../../alignment-planner-workspace/reference/form-field-information-for-strategic-planning.md)

