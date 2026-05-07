---
title: Create new target form
description: Use the Create new target form to create a quantitative or qualitative target for your goal.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Create new target form

Use the Create new target form to create a quantitative or qualitative target for your goal.

<table id="table_eh1_4f1_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the target.

</td></tr><tr><td>

Goal

</td><td>

Goal that this target tracks.

</td></tr><tr><td>

Description

</td><td>

Description of the target.

</td></tr><tr><td>

State

</td><td>

The state of the target. The available options are:-   **Draft**
-   **In Progress**
-   **Approved**
-   **Complete**
-   **Pending**
-   **Achieved**
-   **Not Achieved**

</td></tr><tr><td>

Progress

</td><td>

Percentage of target that is complete. This value is calculated automatically. If the **Type** field is set to **Maximize**, then the progress value is calculated using the following formula.

`Progress = (Actual value - Base value) / (Target value - Base value) x 100`

If the **Type** field is set to **Minimize**, then the progress value is calculated using the following formula. `Progress = (Actual value - Target value) / (Base value - Target value) x 100`

</td></tr><tr><td>

Status

</td><td>

Status to indicate the target progress. The available options are:

-   **Green**: Indicates that the target is on track.
-   **Yellow**: Indicates that the target needs improvement.
-   **Red**: Indicates that the target needs immediate attention.

</td></tr><tr><td>

Impact on goal

</td><td>

A numerical value that represents the importance of this target to its parent goal. By default, the value is **\(1\) Neutral**.

 The available options are:

-   **\(0\) No impact**
-   **\(1\) Neutral**
-   **\(2\) Moderate**
-   **\(3\) High**
-   **\(4\) Very high**
-   **\(5\) Maximum**

**Note:** This field is available only when the**sn\_gf.weighted\_average\_enabled** system property is set to **Yes**.

</td></tr><tr><td>

Owner

</td><td>

Owner of the target.

</td></tr><tr><td>

Contributors

</td><td>

Users who contribute to achieving the target.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Start date|Start date for the target. By default, the start date of the current quarter is populated.|
|End date|End date for the target. By default, the end date of the current quarter is populated.|

<table id="table_yxb_nxt_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unit of measure

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

Type

</td><td>

Target type that shows the direction of achievement. The available options are:-   **Maximize**: The direction of the progress is toward the **Target value** from the **Base value**. The base value must be less than the target value.
-   **Minimize**: The direction of the progress is toward the **Target value** from the **Base value**. The target value must be less than the base value.

</td></tr><tr><td>

Target value

</td><td>

Target value of the target. This value is the goal that your team wants to reach. This field is available only when the **Type** field is set to **Maximize** or **Minimize**.

</td></tr><tr><td>

Review frequency

</td><td>

Option to specify how frequently should the owner or contributor be updating the actual value of the target. The available options are:

-   **Daily**
-   **Weekly**
-   **Fortnightly**
-   **Monthly**
-   **Quarterly**
-   **Yearly**

</td></tr><tr><td>

Remark

</td><td>

Remark entered for business justification when updating the target.

</td></tr><tr><td>

Review date

</td><td>

The date on which the target is to be reviewed.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Exploring goals](../../concept/eaw-concept/eaw-goals.md)

[Add a quantitative target to a goal](../../task/eaw-task/eaw-add-a-quantitative-target-to-a-goal.md)

[Add a qualitative target to a goal](../../task/eaw-task/eaw-add-a-qualitative-target-to-a-goal.md)

