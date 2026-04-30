---
title: Monetary Benefit Plan form
description: Use the Monetary Benefit Plan form to specify the estimated benefit accrued by a demand for a fiscal period.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Demand Management forms, Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Monetary Benefit Plan form

Use the Monetary Benefit Plan form to specify the estimated benefit accrued by a demand for a fiscal period.

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

Type of benefit:-   **Hard**: Benefits that can be measured in terms of revenue.
-   **Soft**: Benefits that are measured in terms of value.

</td></tr><tr><td>

Sub category

</td><td>

Subcategories of hard and soft benefits. The selection in **Category** field determines the selections available in this field.

</td></tr><tr><td>

Benefit type

</td><td>

Type of benefit. Select **Monetary benefits**.

</td></tr><tr><td>

Offset type

</td><td>

Offset type field indicates when the benefits start realizing. If the value in the selected offset type changes, the benefit plan start date shifts accordingly. For example, if the offset type is set to **End Date** and the due date of the demand changes, the benefit plan start date shifts to align with the new due date of the demand.

</td></tr><tr><td>

Work start date

</td><td>

Start date of the demand. The field appears if you select **Start Date** in the **Offset type** field.

</td></tr><tr><td>

Work end date

</td><td>

End date of the demand. The field appears if you select **End Date** in the **Offset type** field.

</td></tr><tr><td>

Offset

</td><td>

Number of periods before or after the offset type when the benefit plan starts. For example, if the offset type is set to **End Date** and the offset is -2, the benefit plan is two periods before the demand end date. If the demand end date shifts, the benefit plan start date shifts to two periods before the new demand due date.

</td></tr><tr><td>

Duration in periods

</td><td>

The length, in periods, of the benefit plan.

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

Non-monetary benefit that is associated with this monetary benefit plan.

</td></tr><tr><td>

Description

</td><td>

Description of the monetary benefit plan.

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

Currency for the benefit plan.If the selected currency is different from the default currency configured in the Financial Management application, the [budget reference rate](../../project-management/concept/c_BudgetReferenceRates.md) is used to calculate the financial benefit of the demand.

</td></tr><tr><td>

Functional currency

</td><td>

The default currency configured in the Financial Management application and used for managing the demand or project.

</td></tr><tr><td>

Total planned benefit

</td><td>

Total benefit value that is rolled up from the benefit breakdown.

</td></tr><tr><td>

Benefit in functional currency

</td><td>

Benefit incurred from demand in functional currency. The value in this field changes if the **Entered currency** is different from the functional currency.

</td></tr><tr><td>

Actual benefit

</td><td>

Actual benefit value that is rolled up from the actual benefit in the benefit breakdown.

</td></tr><tr><td>

Recurring

</td><td>

Check box to indicate if the benefit is recurring for each fiscal period in the benefit breakdown.

</td></tr></tbody>
</table>**Parent Topic:**[Demand Management forms](../concept/demand-management-forms.md)

