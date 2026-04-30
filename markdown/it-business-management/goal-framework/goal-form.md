---
title: Goal form
description: Use the Goal form to create goals for your organizational strategic priorities.
locale: en-US
release: yokohama
product: Goal Framework
classification: goal-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Goal form

Use the Goal form to create goals for your organizational strategic priorities.

**Note:** For Operational Sustainability Workspace and Strategic Planning users, to view the other fields \(that aren’t added to the default or your custom form view\) on the form in the workspace, configure the default/custom form layout. For information on how to configure the form layout, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_demand_benefit_plan_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the goal.

</td></tr><tr><td>

State

</td><td>

State of the goal. The state can be **Draft**, **In progress**, **Approved**, **Complete**, **Pending**, **Achieved**, or **Not Achieved**.

</td></tr><tr><td>

Parent goal

</td><td>

Name of the parent goal that this goal contributes to.

</td></tr><tr><td>

Strategic priority

</td><td>

Name of the strategic priority that this goal is created for.

</td></tr><tr><td>

Start date

</td><td>

Start date for the goal. By default, the start date of the current quarter is populated. For a subgoal, start date of its parent goal is populated.

</td></tr><tr><td>

End date

</td><td>

End date for the goal. By default, the end date of the current quarter is populated. For a subgoal, the end date of its parent goal is populated.

</td></tr><tr><td>

Owner

</td><td>

Owner of the goal. By default, the name of the user creating the goal is populated.

</td></tr><tr><td>

Category

</td><td>

Category of the goal. The available options are:-   **Total Applications**
-   **Total Cost**
-   **Opex**
-   **Capex**
-   **Cloud Applications**
-   **Homegrown Applications**
-   **Support Cost**
-   **Labor Cost**
-   **Standards Compliance**
-   **Strategic**
-   **Operational**
-   **Tactical**
-   **Artificial Intelligence**

</td></tr><tr><td>

Status

</td><td>

Status of the goal. Status can be **Red**, **Yellow**, **Green**, or **None**.

</td></tr><tr><td>

Contributors

</td><td>

Users who contribute to the achievement of the goal.

</td></tr><tr><td>

Team

</td><td>

Assignment group responsible for different activities in achieving the goal.

</td></tr><tr><td>

Impact on parent goal

</td><td>

A numerical value that represents the importance of this goal relative to sibling goals or other goals under its parent goal. By default, the value is \(1\) Neutral.The available options are:

-   **\(0\) No impact**
-   **\(1\) Neutral**
-   **\(2\) Moderate**
-   **\(3\) High**
-   **\(4\) Very high**
-   **\(5\) Maximum**

 **Note:** This field is available only when the **sn\_gf.weighted\_average\_enabled** system property is set to **Yes**.

</td></tr><tr><td>

Progress

</td><td>

Percentage complete for the goal. The progress value is calculated automatically if the goal has sub-goals or/and targets.For more information on how the progress value is calculated, see [Progress value calculation](../concept/progress-value-calculation.md).

</td></tr><tr><td>

Assigned entity type

</td><td>

Entity type to which the goal is assigned. For example, Business Unit, Department, Company, or Portfolio.

</td></tr><tr><td>

Assigned entity

</td><td>

Entity to which the goal is assigned.

</td></tr><tr><td>

Comments

</td><td>

Detailed comments for the goal to facilitate collaboration.

</td></tr><tr><td>

Classification

</td><td>

Goal classification type. The available options are **Environmental**, **Social**, and **Governance**. This field is applicable only for the Operational Sustainability Workspace users.

</td></tr></tbody>
</table>