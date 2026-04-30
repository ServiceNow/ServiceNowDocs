---
title: Create a test plan
description: Create a test plan to detail how a product or a feature is to be tested.Add the planned and actual start and end date fields on the Test Plan form to see the execution date information.
locale: en-US
release: yokohama
product: Test Management
classification: test-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Test plans, Setting up the manual testing process, Test Management 1.0, Test Management applications, Strategic Portfolio Management]
---

# Create a test plan

Create a test plan to detail how a product or a feature is to be tested.

## Before you begin

Role required: tm\_test\_manager or tm\_tester

## Procedure

1.  Navigate to **All** &gt; **Test Management** &gt; **Test Execution** &gt; **Test Plans**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_akn_d4q_wq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short Description

</td><td>

Brief description of the test plan indicating what the test plan is for.

</td></tr><tr><td>

Owner

</td><td>

Owner of the test plan.

</td></tr><tr><td>

Test environment

</td><td>

Specific environment to be used for testing.Users can see the details of the assigned test environment by clicking to the information icon \(![Information icon.](../image/info-icon.png)\) next to the Test environment field.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the test plan is active. If indicated as active, this test plan is visible to users when they try to add a test suite to this plan from the Test Suite form.

</td></tr><tr><td>

Instructions

</td><td>

Any specific instructions for this test plan.

</td></tr><tr><td>

Project

</td><td>

The name of the associated project. This field appears on the Test Plan form if the Test Management PPM Integration is activated as part of the Project Portfolio Suite plugin \(com.snc.project\_portfolio\_suite\).

</td></tr><tr><td>

Project Phase

</td><td>

The name of the associated project phase in the Project Workbench. This field appears on the Test Plan form if the Test Management PPM Integration is activated as part of Project Portfolio Suite plugin \(com.snc.project\_portfolio\_suite\).

</td></tr><tr><td>

Planned start date

</td><td>

Projected start date for the test plan. The planned start date can be the current date or a future date. This field is automatically set to the current date. To change the planned start date, click the calendar icon \(![Calendar icon.](../../project-management/image/calendar-icon.png)\) and select a new date.

 You may need to configure the form to add this field. For more information, see [Display test plan execution start and end dates](t_CreateATestPlan.md#).

</td></tr><tr><td>

Planned end date

</td><td>

Projected end date for the test plan. The planned end date must be after the planned start date. This field is automatically set to the current date. To change the planned end date, click the calendar icon \(![Calendar icon.](../../project-management/image/calendar-icon.png)\) and select a new date.

 You may need to configure the form to add this field. For more information, see [Display test plan execution start and end dates](t_CreateATestPlan.md#).

</td></tr><tr><td>

Actual start date

</td><td>

Actual start date for the test plan. The actual start date can be on or before the planned start date.You may need to configure the form to add this field. For more information, see [Display test plan execution start and end dates](t_CreateATestPlan.md#).

</td></tr><tr><td>

Actual end date

</td><td>

Actual end date for the test plan. The actual end date can be before the planned start date but not before the actual start date.You may need to configure the form to add this field. For more information, see [Display test plan execution start and end dates](t_CreateATestPlan.md#).

</td></tr></tbody>
</table>4.  Save the test plan by using one of the following choices.

    -   Click **Submit** to return to the Test Plans list.
    -   Click **Save** to remain on the Test Plan form.

## What to do next

You can use the related links and related lists of the new test suite for the following actions:

-   Add existing test cases to this test plan from a test suite by clicking the **Add Test Cases from Test Suite** related link.
-   Add new test cases to this test plan from the Test Cases related list. For more information, see [Add a new test case to a test plan](t_AddANewTestCaseToATestPlan.md).
-   Save this test plan as a new test suite by clicking the **Save as Test Suite** related link. A new test suite is created with all the test cases of this plan making them available to add to another test plan.
-   Start the test plan and notify the testers about the target end date for testing by using the **Notify Tester** related link. For more information, see [Initiate guided test execution](t_InitiateGuidedTestExecution.md).
-   Cancel the test execution by clicking **Cancel test execution** related link. This link is available only if you've used the **Notify Tester** related link and started the test plan. For more information, see [Cancel guided test execution](t_CancelGuidedTestExecution.md).
-   View all the test cases in a Visual Task Board \(VTB\) by clicking **Show Visual task Board** related link. The VTB shows test cases in lanes organized by their execution states.
-   Create a copy of this test plan by clicking **Copy Test Plan**.
-   View the test execution summary and sign off the test plan by clicking the **Sign-off Test Plan** related link.
-   View the Test Plan Defects related list for the list of all the defects logged from the test cases.

**Parent Topic:**[Test plans](../concept/c_TestPlans.md)

## Display test plan execution start and end dates

Add the planned and actual start and end date fields on the Test Plan form to see the execution date information.

### Before you begin

Role required: tm\_test\_manager or tm\_tester

### About this task

Configure the Test Plan form layout to display the planned and actual start and end dates for the test plan.

### Procedure

1.  Navigate to **All** &gt; **Test Management** &gt; **Test Execution** &gt; **Test Plans**.

2.  Open a test plan for which you want to see the execution start and end dates.

3.  Open the form layout configuration.

    1.  Right-click the form header.

    2.  Select **Configure**.

    3.  Select **Form Layout**.

4.  Move the following fields from the Available list to the Selected list.

    -   Planned start date
    -   Planned end date
    -   Actual start date
    -   Actual end date
5.  Rearrange the order of the fields in the Selected list.

6.  Click **Save**.


### Result

The Test Plan form is displayed with the newly added date fields.

