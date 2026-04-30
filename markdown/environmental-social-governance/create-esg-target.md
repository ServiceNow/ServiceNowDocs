---
title: Create an Operational Sustainability Management \(formerly ESG Management\) target
description: Create an operational sustainability target to help track the progress towards your operational sustainability goal.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create an Operational Sustainability Management \(formerly ESG Management\) target

Create an operational sustainability target to help track the progress towards your operational sustainability goal.

## Before you begin

Role required: sn\_esg.program\_manager

## About this task

When you create a target, you can use the target to see how well you are meeting your goals. You can treat the status of the target as a report card about your goals. After you create a target, you can create and collect metrics to measure whether the targets are met.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Lists** &gt; **Program Setup** &gt; **Targets**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_lrv_yw4_brb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the target. For example, `Launch diversity programs each quarter`.

</td></tr><tr><td>

Goal

</td><td>

Goal that this target will track.

</td></tr><tr><td>

Start date

</td><td>

Date the target begins

</td></tr><tr><td>

Owner

</td><td>

Owner of the target.

</td></tr><tr><td>

Type

</td><td>

Target type that shows the direction of achievement. Choices are the following:-   **Maximize**: The direction of the progress is towards the **Target value** from the **Base value**. The base value must be less than the target value.
-   **Minimize**: The direction of the progress is towards the **Target value** from the **Base value**. The target value must be less than the base value.
-   **Milestone**: Fixed type. Only the progress field is available. The values of the field \(0-100\) capture the achievement of a milestone.


</td></tr><tr><td>

State

</td><td>

State of the target.

</td></tr><tr><td>

Status

</td><td>

Status to indicate the target progress. Choices are the following:-   Green: Indicates that the target is on track.
-   Yellow: Indicates that the target needs improvement.
-   Red: Indicates that the target needs immediate attention.


</td></tr><tr><td>

End date

</td><td>

Date when the target ends.

</td></tr><tr><td>

Contributors

</td><td>

Users who contribute to achieving the target.

</td></tr><tr><td>

Check in frequency

</td><td>

Option to specify how frequently should the owner or contributor be updating the actual value of the target. The available options are Daily, Weekly, Fortnightly, Monthly, and Quarterly.

</td></tr><tr><td>

Measure

</td><td>

Measure type for the specified value. The available measure types are stored in the Units \[sn\_gf\_units\] table.

</td></tr><tr><td>

Base value

</td><td>

Base value of the target. The base value can also be considered as the present or current value.

</td></tr><tr><td>

Actual value

</td><td>

Actual value of the target at a given time. This field is available only when the **Type** field is set to **Maximize** or **Minimize**.

</td></tr><tr><td>

Target value

</td><td>

Target value of the target. This value is the goal that your team wants to reach. This field is available only when the **Type** field is set to **Maximize** or **Minimize**.

</td></tr><tr><td>

Progress

</td><td>

Percentage of target that is complete. This value is calculated automatically. If the **Type** field is set to **Maximize**, then the progress value is calculated using the following formula.

```
Progress = (Actual value - Base value) / (Target value - Base value) x 100
```

 If the **Type** field is set to **Minimize**, then the progress value is calculated using the following formula.

```
Progress = (Actual value - Target value) / (Base value - Target value) x 100
```

</td></tr><tr><td>

Weight scale

</td><td>

A numerical value that represents the importance of the target relative to the other targets of the goal. If there are any sub-goals present, they are also considered for relative weights and consequent progress calculation. By default, the weight scale is 1.**Note:** This field is available only when the **sn\_gf.weighted\_average\_enabled** system property is set to **Yes**.

</td></tr><tr><td>

Source for target

</td><td>

The metric definition or the metric that acts as a source of the target. This field only appears when the **Type** field contains either **Maximize** or **Minimize**. For information on how to add a source, see [Add a source for a target](add-a-source-for-a-target.md).

</td></tr></tbody>
</table>4.  To mark a material topic as confidential, in the Security section, select the **Confidential** option.

    1.  In the **Allowed users** field, select the users who can view the record.

    2.  In the **Allowed groups**, select the groups that can view the record.

    This Security section only appears if the**sn\_grc.enable\_record\_confidentiality** property is enabled under GRC properties. By default, the logged in user is added to the list of confidential users.

5.  Click **Save**.

    The Metric Definitions and the Metric related lists appear.

6.  To add a metric definition, do the following:

    1.  Click the Metric Definition related list.

    2.  Click **Add**.

    3.  Select the metric definitions to add.

    4.  Click **Add**.


## Result

The target with metric definitions is created.

-   **[Add a source for a target](add-a-source-for-a-target.md)**  
After you create a target, you must add a source for the target. The source can be a metric or a metric definition that contributes to the parent target.

**Parent Topic:**[Configure ESG Management \(formerly ESG Management\)](../concept/configuring-esg.md)

