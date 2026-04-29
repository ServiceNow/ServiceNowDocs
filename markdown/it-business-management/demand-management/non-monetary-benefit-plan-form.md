---
title: Non-monetary Benefit Plan form
description: Use the Non-monetary Benefit Plan form to specify the potential non-financial benefits accrued by the demand, when it's executed.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Demand Management forms, Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Non-monetary Benefit Plan form

Use the Non-monetary Benefit Plan form to specify the potential non-financial benefits accrued by the demand, when it's executed.

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

Subcategories of hard and soft benefits. The selection in the **Category** field determines the selections available in this field.

</td></tr><tr><td>

Benefit type

</td><td>

Type of benefit. Select **Non-monetary benefits**.

</td></tr><tr><td>

Offset type

</td><td>

Field to indicate when the benefits start to be realized.If the value in the selected offset type changes, the benefit plan start date shifts accordingly. For example, if the offset type is set to **End Date** and the due date of the demand changes, the benefit plan start date shifts to align with the new due date of the demand.

</td></tr><tr><td>

Work start date

</td><td>

Start date of the demand. This field appears only when **Start Date** is selected from the **Offset type** field.

</td></tr><tr><td>

Work end date

</td><td>

End date of the demand. This field appears only when **End Date** is selected from the **Offset type** field.

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

Starting fiscal period. Populated based on the value in the **Offset** field relative to the selected **Project/Demand start date** or **Project/Demand end date**, and the **Duration in periods** field values.The field is editable if you select **None** in the **Offset type** field.

 When you change the start fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period.When you change the end fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

Associated benefit

</td><td>

Monetary benefit that is associated with this non-monetary benefit plan.

</td></tr><tr><td>

Description

</td><td>

Description of the non-monetary benefit plan.

</td></tr></tbody>
</table><table id="table_mzx_y33_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Measure

</td><td>

Type of measure for the non-monetary benefit plan. The measure types are Count, Percentage, Hours, Days, and Score.Select the option **Yes/No** to track the benefits that aren’t quantifiable. When this option is selected, the only field available is **Benefits achieved**. You can select the check box to indicate that the benefits have been achieved.

</td></tr><tr><td>

Non-monetary entered benefit

</td><td>

Estimated value of the potential benefit.

Any change in the planned benefit on the benefit plan updates the associated benefit breakdown values for future fiscal periods only.

</td></tr><tr><td>

Non-monetary planned benefit

</td><td>

Benefit value that is rolled up from the benefit breakdown.

</td></tr><tr><td>

Benefits achieved

</td><td>

Option to indicate if the benefit is achieved.

</td></tr><tr><td>

Breakdown type

</td><td>

Type of breakdown creation when you save the benefit plan.-   **None**: No breakdowns are created.
-   **Automatic**: A Non-monetary Benefit Plan Breakdown record is created automatically with data. The breakdown is calculated linearly.
-   **Manual**: A Non-monetary Benefit Plan Breakdown record is created automatically but without data in the entered benefit column.

</td></tr><tr><td>

Aggregation mode

</td><td>

Determines how the roll-up happens from breakdowns to the benefit plan and updates the values in the **Non-monetary planned benefit** and **Non-monetary actual benefit** fields.-   **Sum**: Aggregates data from all breakdowns.
-   **Average**: Average value from all breakdowns.
-   **Most recent**: Recent breakdown value.
-   **Max**: Maximum value among the breakdowns.
-   **Min**: Minimum value among the breakdown

</td></tr><tr><td>

Non-monetary actual benefit

</td><td>

Actual benefit value that is rolled up from the actual benefit in the non-monetary benefit plan breakdown.

</td></tr></tbody>
</table>**Parent Topic:**[Demand Management forms](../concept/demand-management-forms.md)

