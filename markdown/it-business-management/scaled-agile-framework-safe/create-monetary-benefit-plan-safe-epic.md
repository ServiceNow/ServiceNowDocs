---
title: Create a monetary benefit plan for an epic
description: Epic benefit plans capture the potential benefits accrued by the epic when the epic is executed. Create a monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.
locale: en-US
release: australia
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Define an epic in SAFe, SAFe entities, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Create a monetary benefit plan for an epic

Epic benefit plans capture the potential benefits accrued by the epic when the epic is executed. Create a monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.

## Before you begin

Role required: safe\_product\_owner, safe\_scrum\_master, or safe\_admin

## About this task

The monetary benefit plan breakdown records are automatically created when you save the benefit plan.

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Epics**.

2.  Open the required epic.

3.  Click the hamburger icon \(![Hamburger icon](../../agile-development/image/hamburger-icon.png)\) and navigate to **View** &gt; **Benefit**.

4.  On the form, fill in the fields in the Planning section.

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

6.  In the Monetary Benefit Plans related list, click **New**.

7.  On the form, fill in the fields.

<table id="table_benefit_plan_form"><thead><tr><th>

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

Sub-categories of hard and soft benefits.The selection in **Category** field determines the selections available in this field.

</td></tr><tr><td>

Benefit type

</td><td>

Type of benefit. Select **Monetary benefits**.

</td></tr><tr><td>

Offset type

</td><td>

Field to indicate when the benefits start realizing. Select any of the following options:-   **None**: The default value is None. When you select **None**, you need to manually enter the benefit plan start and end fiscal periods.
-   **Milestone**: After completion of a milestone.
-   **Start Date**: At the start of the epic.
-   **End Date**: After the epic ends.
 If the value in the selected offset type changes, the benefit plan start date shifts accordingly. For example, if the offset type is set to **End Date** and the end date of the epic changes, the benefit plan start date shifts to align with the new end date of the epic.

</td></tr><tr><td>

Milestone

</td><td>

Epic milestones to which the benefit plan belongs. The field appears if you select **Milestone** in the **Offset type** field.

</td></tr><tr><td>

Milestone start date

</td><td>

Start date of the selected milestone. The field appears if you select **Milestone** in the **Offset type** field.

</td></tr><tr><td>

Work start date

</td><td>

Start date of the epic. The field appears if you select **Start Date** in the **Offset type** field.

</td></tr><tr><td>

Work end date

</td><td>

End date of the epic. The field appears if you select **End Date** in the **Offset type** field.

</td></tr><tr><td>

Offset

</td><td>

Number of periods before or after the offset type when the benefit plan starts. For example, if the offset type is selected as **End Date** and the offset is -2, the benefit plan is two periods prior to the epic end date. If the epic end date shifts, the benefit plan start date shifts to two periods prior to the new epic due date.

</td></tr><tr><td>

Duration in periods

</td><td>

The length, in periods, of the benefit plan.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting fiscal period. Populated based on the value in the Offset field relative to the selected **Milestone**, **Work start date**, or **Work end date**, and **Duration in period** values.The field is editable if you select **None** in the **Offset type** field.

 When you change the start fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period. Populated based on the value in the Offset field relative to the selected **Milestone**, **Work start date**, or **Work end date**, and **Duration in period** values.The field is editable if you select **None** in the **Offset type** field.

 When you change the end fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

Associated benefit

</td><td>

Non-monetary benefit that is associated to this monetary benefit plan.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Entered benefit|Benefit incurred from the epic specified in terms of entered currency.|
    |Entered currency|Currency in which you want the benefit plan to be created.|
    |Functional currency|Currency that is obtained from the **glide.system.locale** property.|
    |Total planned benefit|Estimated amount of potential benefit of the epic.|
    |Benefit in functional currency|Benefit incurred from epic in terms of functional currency. The value in this field changes if the **Entered currency** is different from the functional currency.|
    |Actual benefit|Actual benefit that is incurred from the epic. This value is rolled up from the **Actual benefit** field of all the benefit plan breakdowns.|
    |Recurring|Option to indicate that the benefit is recurring for all the fiscal periods in the benefit plan.|

8.  Click **Submit**.


## What to do next

On the Benefit Plan form, view the benefit breakdown by fiscal period in the Monetary Benefit Plan Breakdowns related list.

-   **[Update a monetary benefit plan breakdown for an epic](update-monetary-benefit-plan-breakdown-safe-epic.md)**  
Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.

**Parent Topic:**[Define an epic in SAFe](create-SAFeepic.md)

