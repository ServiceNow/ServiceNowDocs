---
title: Non-monetary benefit plan form
description: The non-monetary benefit plan form enables you to create non-monetary benefit plans for a demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/non-monetary-benefit-plan-form-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Forms, Reference, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Non-monetary benefit plan form

The non-monetary benefit plan form enables you to create non-monetary benefit plans for a demand.

<table id="table_demand_benefit_plan_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the benefit plan.

</td></tr><tr><td>

Work

</td><td>

Demand associated with the cost plan. This field is automatically set to the associated demand.

</td></tr><tr><td>

Sponsor

</td><td>

Sponsor for the demand.

</td></tr><tr><td>

Category

</td><td>

Type of the non-monetary benefit:-   Hard: Benefits measured in terms of revenue.
-   Soft: Benefits measured in terms of value.

</td></tr><tr><td>

Sub category

</td><td>

Subcategories of hard and soft benefits. The selection in the Category field determines the available options in this field.

</td></tr><tr><td>

Benefit type

</td><td>

Type of the benefit.The available values are:

-   Monetary benefits
-   Non-monetary benefits

</td></tr><tr><td>

Offset type

</td><td>

Indicates when benefits start to accrue. If the value in the selected offset type changes, the benefit plan start date shifts accordingly.The available values are:

-   None
-   Milestone
-   Start Date
-   End Date

For example, if the offset type is set to End Date and the demand due date changes, the benefit plan start date shifts accordingly.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting fiscal period. Populated based on values in the Offset field relative to the selected demand start date or demand end date, and the Duration in period values.The field is editable if you select None in the Offset type field.

Changing the start fiscal period also updates the associated benefit breakdown values.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period.Changing the end fiscal period also updates the associated benefit breakdown values.

</td></tr><tr><td>

Associated benefit

</td><td>

Benefits associated with this benefit plan.

</td></tr><tr><td>

Description

</td><td>

Summary of the benefit plan.

</td></tr></tbody>
</table><table id="table_svx_dn3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Non-monetary entered benefit

</td><td>

Estimated amount of the potential benefit.Changes to the planned benefit update the associated benefit breakdown values for future fiscal periods.

</td></tr><tr><td>

Measure

</td><td>

Type of measure for the non-monetary benefit plan. The available values are:-   Count
-   Percentage
-   Hours
-   Days
-   Score

The Yes/No options are used to track the benefits that aren't quantifiable. When this option is selected, the only field available is Benefits achieved. You can select the Benefits achieved check box to indicate that the benefits have been achieved.

</td></tr><tr><td>

Benefits achieved

</td><td>

Indicates whether the benefit is achieved.

</td></tr><tr><td>

Non-monetary planned benefit

</td><td>

Estimated value of the potential benefit.Changes to the planned benefit update the associated benefit breakdown values for future fiscal periods only.

</td></tr><tr><td>

Breakdown type

</td><td>

Type of breakdown creation when you save the benefit plan. The available values are:-   None: No breakdowns are created.
-   Automatic: A non-monetary benefit plan breakdown record is created automatically with data. The breakdown is calculated linearly.
-   Manual: A non-monetary benefit plan breakdown record is created automatically but without data in the entered benefit column.

</td></tr><tr><td>

Non-monetary actual benefit

</td><td>

Actual benefit value rolled up from the actual benefit in the benefit breakdown.

</td></tr><tr><td>

Aggregation mode

</td><td>

Determines how the roll-up happens from breakdowns to the benefit plan and updates the values in the Non-monetary planned benefit and Non-monetary actual benefit fields. The available values are:-   Sum: Aggregates data from all breakdowns.
-   Average: Average value from all breakdowns.
-   Most recent: Recent breakdown value.
-   Max: Maximum value among the breakdowns.
-   Min: Minimum value among the breakdowns.

</td></tr></tbody>
</table>