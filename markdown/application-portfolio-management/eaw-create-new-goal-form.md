---
title: Create new goal form
description: Use the Goal form to create goals for your organizational strategic priorities.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create new goal form

Use the Goal form to create goals for your organizational strategic priorities.

<table id="table_ogv_rzz_xbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the goal.

</td></tr><tr><td>

Parent goal

</td><td>

Name of the parent goal that this goal contributes to.

</td></tr><tr><td>

Start date

</td><td>

Start date for the goal. By default, the start date of the current quarter is populated.

</td></tr><tr><td>

Owner

</td><td>

Owner of the goal. By default, the name of the user creating the goal is populated.

</td></tr><tr><td>

Status

</td><td>

Status of the goal. The available options are:

-   **Red**: Indicates that the goal needs immediate attention.
-   **Yellow**: Indicates that the target needs improvement.
-   **Green**: Indicates that the target is on track.
-   **None**

</td></tr><tr><td>

Impact on parent goal

</td><td>

A numerical value that represents the importance of this goal relative to sibling goals or other goals under its parent goal. By default, the value is \(1\) Neutral.

 The available options are:

-   **\(0\) No impact**
-   **\(1\) Neutral**
-   **\(2\) Moderate**
-   **\(3\) High**
-   **\(4\) Very high**
-   **\(5\) Maximum**

**Note:** This field is available only when the **sn\_gf.weighted\_average\_enabled** system property is set to **Yes**.

</td></tr><tr><td>

Assigned entity type

</td><td>

Entity type to which the goal is assigned. For example, Business Unit or Department.

</td></tr><tr><td>

State

</td><td>

State of the goal. The available options are:-   **Draft**
-   **In Progress**
-   **Approved**
-   **Complete**
-   **Pending**
-   **Achieved**
-   **Not Achieved**

</td></tr><tr><td>

Strategic priority

</td><td>

Name of the strategic priority that this goal is created for.

</td></tr><tr><td>

End date

</td><td>

End date for the goal. By default, the end date of the current quarter is populated.

</td></tr><tr><td>

Category

</td><td>

Category of the goal. The available options are:

-   **Total Applications**
-   **Total Cost**
-   **Opex Capex**
-   **Cloud Applications**
-   **Homegrown Applications**
-   **Support Cost Labor Cost**

</td></tr><tr><td>

Contributors

</td><td>

Users who contribute to the achievement of the goal.

</td></tr><tr><td>

Progress

</td><td>

Percentage complete for the goal. The progress value is calculated automatically if the goal has subgoals or/and targets.

</td></tr><tr><td>

Assigned entity

</td><td>

Entity to which the goal is assigned.

</td></tr><tr><td>

Comments

</td><td>

Detailed comments for the goal to facilitate collaboration.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Exploring goals](../../concept/eaw-concept/eaw-goals.md)

[Add or edit a goal](../../task/eaw-task/eaw-add-or-edit-a-goal.md)

[Create a sub-goal](../../task/eaw-task/eaw-create-a-sub-goal.md)

