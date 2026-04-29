---
title: Monetary benefit plan form
description: The benefit plan form information is used to create monetary and non-monetary benefit plans for a demand.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Form field information, Reference, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Monetary benefit plan form

The benefit plan form information is used to create monetary and non-monetary benefit plans for a demand.

<table id="table_demand_benefit_plan_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the benefit plan.

</td></tr><tr><td>

Work

</td><td>

Demand number to which the benefit plan belongs.

</td></tr><tr><td>

Sponsor

</td><td>

Sponsor for the demand.

</td></tr><tr><td>

Category

</td><td>

Type of benefit:-   **Hard**: Benefits measured in terms of revenue.
-   **Soft**: Benefits measured in terms of value.

</td></tr><tr><td>

Sub category

</td><td>

Subcategories of hard and soft benefits. The selection in the **Category** field determines the available options in this field.

</td></tr><tr><td>

Benefit type

</td><td>

Type of the benefit: monetary or non-monetary.

</td></tr><tr><td>

Offset type

</td><td>

Indicates when the benefits start realizing. If the value in the selected offset type changes, the benefit plan start date shifts accordingly. For example, if the offset type is set to End Date and the demand due date changes, the benefit plan start date shifts to align with the new due date.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting fiscal period. Populated based on values in the Offset field relative to the selected Project or Demand start date or Project or Demand end date, and the Duration in period values.The field is editable if you select **None** in the **Offset type** field.

When you change the start fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period.When you change the end fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

Associated benefit

</td><td>

Benefits associated with this benefit plan.

</td></tr><tr><td>

Description

</td><td>

Description of the benefit plan.

</td></tr></tbody>
</table><table id="table_svx_dn3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entered benefit

</td><td>

Estimated amount of the potential benefit.Any change in the planned benefit on the benefit plan updates the associated benefit breakdown values for future fiscal periods.

</td></tr><tr><td>

Entered currency

</td><td>

Currency for the benefit plan. If the selected currency differs from the default currency configured in the Financial Management application, the budget reference rate is used to calculate the financial benefit of the demand. For more information, refer to [budget reference rate](../../project-management/concept/c_BudgetReferenceRates.md).

</td></tr><tr><td>

Functional currency

</td><td>

Default currency configured in the Financial Management application and used for managing the demand or project.

</td></tr><tr><td>

Total planned benefit

</td><td>

Total benefit value rolled up from the benefit breakdown.

</td></tr><tr><td>

Benefit in functional currency

</td><td>

Benefit incurred from demand in functional currency. The value in this field changes if the **Entered currency** differs from the functional currency.

</td></tr><tr><td>

Actual benefit

</td><td>

Actual benefit value rolled up from the actual benefit in the benefit breakdown.

</td></tr><tr><td>

Recurring

</td><td>

Indicates if the benefit is recurring for each fiscal period in the benefit breakdown.

</td></tr></tbody>
</table>