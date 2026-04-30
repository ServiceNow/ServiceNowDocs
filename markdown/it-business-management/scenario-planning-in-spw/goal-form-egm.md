---
title: Goal form
description: Use the Goal form to create goals for your organizational strategic priorities.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Form field information for Strategic Planning, Reference, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Goal form

Use the Goal form to create goals for your organizational strategic priorities.

**Note:** For ESG Workspace and Strategic Planning users, to view the other fields \(that are not added to the default or your custom form view\) on the form in the workspace, configure the default/custom form layout. For information on how to configure the form layout, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

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

</td></tr><tr><td>

Status

</td><td>

Status of the goal. Status can be **Red**, **Yellow**, **Green**, or **None**.

</td></tr><tr><td>

Progress

</td><td>

Percentage complete for the goal. The progress value is calculated automatically if the goal has sub-goals or/and targets.For more information on how the progress value is calculated, see [Progress value calculation](../../alignment-planner-workspace/concept/progress-value-calculation-egm.md).

</td></tr><tr><td>

Description

</td><td>

Brief description of the goal.

</td></tr></tbody>
</table><table id="table_mkc_jyz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Strategic priority

</td><td>

Name of the strategic priority that this goal is created for.

</td></tr><tr><td>

Parent goal

</td><td>

Name of the parent goal that this goal contributes to.

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

</td></tr></tbody>
</table><table id="table_rhx_jyz_fdc"><thead><tr><th>

FIeld

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned entity type

</td><td>

Entity type to which the goal is assigned. For example, Business Unit, Department, Company, or Portfolio.

</td></tr><tr><td>

Assigned entity

</td><td>

Entity to which the goal is assigned. For example,if the portfolio plan is created with Business Units, HR and IT, populate the Assigned entity type as Business Unit and Assigned entity type as HR or IT.**Note:** Populating the Assigned entity type and Assigned entity fields are required to display the goals in the portfolio plan.

</td></tr><tr><td>

Owner

</td><td>

Owner of the goal. By default, the name of the user creating the goal is populated.

</td></tr><tr><td>

Contributors

</td><td>

Users who contribute to the achievement of the goal.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Start date|Start date for the goal. By default, the start date of the current quarter is populated. For a sub-goal, start date of its parent goal is populated.|
|End date|End date for the goal. By default, the end date of the current quarter is populated. For a sub-goal, the end date of its parent goal is populated.|

|Field|Description|
|-----|-----------|
|Comments|Detailed comments for the goal to facilitate collaboration.|
|Team|Assignment group responsible for different activities in achieving the goal.|
|Classification|Goal classification type. The available options are **Environmental**, **Social**, and **Governance**. This field is applicable only for the ESG Workspace users.|

**Parent Topic:**[Form field information for Strategic Planning](../../alignment-planner-workspace/reference/form-field-information-for-strategic-planning.md)

**Related topics**  


[Iteration goals and work item goals in EAP](../../spw-eap/concept/iteration-goals-in-eap.md)

