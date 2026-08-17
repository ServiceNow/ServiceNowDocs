---
title: Create goal form
description: Use the Goal form to create goals for organizational strategic priorities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-create-new-goal-form.html
release: australia
topic_type: reference
last_updated: "2024-07-03"
reading_time_minutes: 2
keywords: [goals, strategic priorities, goal form]
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Create goal form

Use the Goal form to create goals for organizational strategic priorities.

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

Start date for the goal. The start date of the current quarter is automatically set.

</td></tr><tr><td>

Owner

</td><td>

Owner of the goal. The name of the user creating the goal is automatically set.

</td></tr><tr><td>

Status

</td><td>

Status of the goal. The available options are:

 -   **Red**: Goal needs immediate attention.
-   **Yellow**: Target needs improvement.
-   **Green**: Target is on track.
-   **None**

</td></tr><tr><td>

Impact on parent goal

</td><td>

Numerical value representing the importance of this goal relative to sibling goals or other goals under its parent goal. The value is automatically set to \(1\) Neutral.

 The available options are:

-   **\(0\) No impact**
-   **\(1\) Neutral**
-   **\(2\) Moderate**
-   **\(3\) High**
-   **\(4\) Very high**
-   **\(5\) Maximum**

**Note:** This field appears only when the **sn\_gf.weighted\_average\_enabled** property is set to **Yes**.

</td></tr><tr><td>

Assigned entity type

</td><td>

Entity type to which the goal is assigned. For example, Business Unit or Department.

</td></tr><tr><td>

State

</td><td>

State of the goal. The available options are:

 -   **Draft**
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

End date for the goal. The end date of the current quarter is automatically set.

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

Percentage complete for the goal. The progress value is calculated automatically if the goal has subgoals, targets, or both.

</td></tr><tr><td>

Assigned entity

</td><td>

Entity to which the goal is assigned.

</td></tr><tr><td>

Comments

</td><td>

Detailed comments for the goal to facilitate collaboration.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[Exploring goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-goals.md)

[Add or edit a goal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-or-edit-a-goal.md)

[Create a sub-goal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-a-sub-goal.md)

[Add goal to driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-goal-to-driver.md)

[Add a goal to a business capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-goal-to-business-capability.md)

