---
title: Non-monetary benefit plans form
description: Learn about the fields of non-monetary benefit plans form.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Form field information for Project Management, Reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Non-monetary benefit plans form

Learn about the fields of non-monetary benefit plans form.

<table id="table_jz2_svy_jpb"><thead><tr><th>

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

Project or demand to which the benefit plan belongs.

</td></tr><tr><td>

Sponsor

</td><td>

Sponsor for the project.

</td></tr><tr><td>

Category

</td><td>

Type of benefit:-   **Hard**: Benefits that can be measured in terms of revenue.
-   **Soft**: Benefits that are measured in terms of value.

</td></tr><tr><td>

Sub category

</td><td>

Subcategories of hard and soft benefits.The selection in the **Category** field determines the selections available in this field.

</td></tr><tr><td>

Benefit type

</td><td>

Type of benefit. Select **Non-monetary benefits**.

</td></tr><tr><td>

Offset type

</td><td>

Field to indicate when the benefits start to be realized. Select any of the following options:-   **None**: The default value is None. When you select **None**, you must manually enter the benefit plan start and end fiscal periods.
-   **Milestone**: After completion of a milestone.
-   **Start Date**: At the start of the project.
-   **End Date**: After the project ends.

 If the value in the selected **Offset type** field changes, the benefit plan start date shifts accordingly. For example, if the **Offset type** field is set to **End Date** and the end date of the project changes, the benefit plan start date shifts to align with the new end date of the project.

</td></tr><tr><td>

Milestone

</td><td>

Project milestones to which the benefit plan belongs. This field appears only when **Milestone** is selected from the **Offset type** field.

</td></tr><tr><td>

Milestone start date

</td><td>

Start date of the selected milestone. This field appears only when **Milestone** is selected from the **Offset type** field.

</td></tr><tr><td>

Work start date

</td><td>

Start date of the project or demand. This field appears only when **Start Date** is selected from the **Offset type** field.

</td></tr><tr><td>

Work end date

</td><td>

End date of the project or demand. This field appears only when **End Date** is selected from the **Offset type** field.

</td></tr><tr><td>

Offset

</td><td>

Number of periods before or after the offset type when the benefit plan starts. For example, if the offset type is selected as **End Date** and the offset is -2, the benefit plan is two periods prior to the project end date. If the project end date shifts, the benefit plan start date shifts to two periods prior to the new project due date.

</td></tr><tr><td>

Duration in periods

</td><td>

The length, in periods, of the benefit plan.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting fiscal period. Populated based on the value in the **Offset** field relative to the selected **Milestone**, **Project/Demand start date**, or **Project/Demand end date**, and **Duration in periods** field values.The field is editable if you select **None** in the **Offset type** field.

 When you change the start fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period. Populated based on the value in the Offset field relative to the selected Milestone, Project or Demand start date, or Project or Demand end date, and Duration in period values.The field is editable if you select **None** in the **Offset type** field.

 When you change the end fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

Associated benefit

</td><td>

Monetary benefit that is associated to this non-monetary benefit plan.

</td></tr></tbody>
</table><table id="table_gzx_mdg_mcc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Measure

</td><td>

Type of measure for the non-monetary benefit plan. The measure types are Count, Percentage, Hours, Days, and Score.Select the option **Yes/No** to track the benefits that are not quantifiable. When this option is selected, the only field available is **Benefits achieved**. You can select the check box to indicate that the benefits have been achieved.

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
-   **Automatic**: A Non-monetary Benefit Plan Breakdowns record is created automatically with data. The breakdown is calculated linearly.
-   **Manual**: A Non-monetary Benefit Plan Breakdown record is created automatically but without data in the **Entered benefit** column.

</td></tr><tr><td>

Aggregation mode

</td><td>

Determines how the roll-up happens from breakdowns to the benefit plan and updates the values in the **Non-monetary planned benefit** and **Non-monetary actual benefit** fields.-   **Sum**: Aggregates data from all breakdowns.
-   **Average**: Average value from all breakdowns.
-   **Most recent**: Recent breakdown value.
-   **Max**: Maximum value among the breakdowns.
-   **Min**: Minimum value among the breakdowns.

</td></tr><tr><td>

Non-monetary actual benefit

</td><td>

Actual benefit value that is rolled up from the actual benefit in the non-monetary benefit plan breakdown.

</td></tr></tbody>
</table>**Related topics**  


[Create a non-monetary benefit plan for a project](../task/create-a-non-monetary-benefit-plan-for-a-project.md)

[Update a non-monetary benefit plan breakdown for a project](../task/update-a-non-monetary-benefit-plan-breakdown-for-a-project.md)

