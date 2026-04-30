---
title: Create a non-monetary benefit plan for an epic
description: Epic benefit plans capture the potential non-financial benefits accrued by the epic when the epic is executed. Create a non-monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.
locale: en-US
release: zurich
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Define an epic in SAFe, SAFe entities, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Create a non-monetary benefit plan for an epic

Epic benefit plans capture the potential non-financial benefits accrued by the epic when the epic is executed. Create a non-monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.

## Before you begin

Role required: safe\_product\_owner, safe\_scrum\_master, or safe\_admin

## About this task

The non-monetary benefit plan breakdown records are automatically created when you save the benefit plan by selecting **Automatic** or **Manual** in the **Breakdown Type** field. The non-monetary benefit plan breakdown records specify the estimated and actual non-financial benefits at a granular level for specific fiscal periods, such as FY16: April and FY16: May. The Non-monetary Benefit Plan Breakdowns related list shows the aggregated benefits for estimated and actual non-financial benefits for each fiscal period for the epic.

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Epics**.

2.  Open the required epic.

3.  Click the hamburger icon \(![Hamburger icon](../../agile-development/image/hamburger-icon.png)\) and navigate to **View** &gt; **Benefit**.

4.  On the form, fill in the required fields in the Planning section.

    This section is available when the Benefit view is selected.

    |Field|Description|
    |-----|-----------|
    |Planned start date|Projected start date for the epic. The planned start date can be the current date or a future date.|
    |Planned end date|Projected end date for the epic. The planned end date must be after the planned start date.|
    |Planned benefit|Benefit value that is rolled up from the benefit breakdown.|
    |Actual start date|Actual start date for the epic. The actual start date can be on or before the planned start date.|
    |Actual end date|Actual end date for the epic. The actual end date can be before the planned start date but not before the actual start date.|
    |Actual benefit|Actual benefit value that is rolled up from the actual benefit in the benefit breakdown.|

5.  Save the record.

6.  Click the Non-monetary Benefit Plans related list.

7.  To create a non-monetary benefit plan, click **New**.

8.  On the form, fill in the fields.

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

Epic to which the benefit plan belongs.

</td></tr><tr><td>

Sponsor

</td><td>

Sponsor for the epic.

</td></tr><tr><td>

Category

</td><td>

Type of benefit:-   **Hard**: Benefits that can be measured in terms of revenue.
-   **Soft**: Benefits that are measured in terms of value.


</td></tr><tr><td>

Sub category

</td><td>

Subcategories of hard and soft benefits.The value of the **Category** field determines the choices available in this field.

</td></tr><tr><td>

Benefit type

</td><td>

Type of benefit. Select **Non-monetary benefits**.

</td></tr><tr><td>

Offset type

</td><td>

Field to indicate when the benefits start to be realized. Select any of the following options:-   **None**: The default value is None. When you select **None**, you must manually enter the benefit plan start and end fiscal periods.
-   **Milestone**: After completion of a milestone.
-   **Start Date**: At the start of the epic.
-   **End Date**: After the epic ends.
 If the value in the **Offset type** field changes, the benefit plan start date shifts accordingly. For example, if the **Offset type** field is set to **End Date** and the end date of the epic changes, the start date of the benefit plan shifts to align with the new end date of the epic.

</td></tr><tr><td>

Milestone

</td><td>

Epic milestones to which the benefit plan belongs. This field appears only when **Milestone** is selected from the **Offset type** field.

</td></tr><tr><td>

Milestone start date

</td><td>

Start date of the selected milestone. This field appears only when **Milestone** is selected from the **Offset type** field.

</td></tr><tr><td>

Work start date

</td><td>

Start date of the epic. This field appears only when **Start Date** is selected from the **Offset type** field.

</td></tr><tr><td>

Work end date

</td><td>

End date of the epic. This field appears only when **End Date** is selected from the **Offset type** field.

</td></tr><tr><td>

Offset

</td><td>

Number of periods before or after the offset type when the benefit plan starts. For example, if the offset type is selected as **End Date** and the offset is -2, the benefit plan is two periods prior to the epic end date. If the epic end date changes, the benefit plan start date shifts to two periods prior to the new epic due date.

</td></tr><tr><td>

Duration in periods

</td><td>

The length, in periods, of the benefit plan.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting fiscal period. This field is populated based on the value in the **Offset** field relative to the selected **Milestone**, **Work start date**, or **Work end date**, and **Duration in periods** field values.This field is editable if you select **None** in the **Offset type** field.

 When you change the start fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period. This field is populated based on the value in the **Offset** field relative to the selected Milestone, Project or Demand start date, or Project or Demand end date, and Duration in period values.This field is editable if you select **None** in the **Offset type** field.

 When you change the end fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

Associated benefit

</td><td>

Monetary benefit that is associated to this non-monetary benefit plan.

</td></tr></tbody>
</table><table id="table_ucg_gvh_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Measure

</td><td>

Type of measure for the non-monetary benefit plan. The measure types are Count, Percentage, Hours, Days, and Score.Select the option **Yes/No** to track the benefits that are not quantifiable. When this option is selected, the only field available is **Benefits achieved**. You can select the check box to indicate that the benefits have been achieved.

</td></tr><tr><td>

Non-monetary entered benefit

</td><td>

Estimated value of the potential benefit.

Any change in the planned benefit in the benefit plan updates the associated benefit breakdown values for future fiscal periods only.

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
</table>9.  Click **Submit**.


## What to do next

-   On the Benefit Plan form, view the benefit breakdown by fiscal period in the Non-monetary Benefit Plan Breakdowns related list.
-   [Associate monetary and non-monetary benefit plans](associate-benefit-plans-safe-epic.md), so that you can capture the potential benefits \(financial and non-financial\) accrued by the epic for the hybrid benefit plans.

-   **[Update a non-monetary benefit plan breakdown for an epic](update-non-monetary-benefit-plan-breakdown-safe-epic.md)**  
Update a non-monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.

**Parent Topic:**[Define an epic in SAFe](create-SAFeepic.md)

