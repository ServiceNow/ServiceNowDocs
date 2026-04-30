---
title: Report a defect from a failed test
description: Report a defect from an individual test that has failed so that you can further investigate the test failure.
locale: en-US
release: zurich
product: Test Management
classification: test-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Test Management 1.0, Test Management applications, Strategic Portfolio Management]
---

# Report a defect from a failed test

Report a defect from an individual test that has failed so that you can further investigate the test failure.

## Before you begin

-   [Activate Agile Development 2.0](../../agile-development/task/activate-agile-development.md)

    The ability to report a defect is available only if the Agile Development 2.0 plugin is activated.

-   Perform tests and update the test status. For more information, see [Performing tests and updating the test status](../concept/c_Tester.md).
-   Role required: tm\_tester

    **Important:**

    Verify that the rm\_tester role is assigned to you in your instance. This role is required to use the Report Defect link. If the role is not available, contact your system administrator to confirm the correct role for your organization.


## About this task

Use the Test form to report a defect for a test that has failed. The reported defect is also linked to the test case which this test is related to.

## Procedure

1.  Navigate to **All** &gt; **Test Management** &gt; **Test Execution** &gt; **Test Plans**.

2.  Open the test plan which has the failed test.

3.  From the Test Cases related list, open the test case which has the failed test.

4.  From the Tests related list, open the test that failed.

5.  On the Test form, click one of the following links:

    -   The **Report Defect** link next to the **Status** field.
    -   The **Report defect** related link.
6.  On the form, fill in the fields.

<table id="table_sfp_lmk_br"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier for the defect.

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to fix this defect.

</td></tr><tr><td>

Assigned to

</td><td>

Individual assigned to fix this defect.

</td></tr><tr><td>

Priority

</td><td>

Priority of the defect. Choose one from the following:-   1- Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning


</td></tr><tr><td>

State

</td><td>

The current state of the defect. Select one from the following:-   Draft
-   Scoping
-   Awaiting Approval
-   Work in Progress
-   Testing/QA
-   Deploy/Launch
-   Closed/Complete
-   On hold
-   Canceled


</td></tr><tr><td>

Short description

</td><td>

Brief explanation of the defect.

</td></tr><tr><td>

Description

</td><td>

Detailed explanation of the defect.

</td></tr><tr><td>

Work notes

</td><td>

Any comments, notes, or other information related to the defect.

</td></tr></tbody>
</table>7.  Click **Submit**.


## Result

A defect is created and added to the following related lists:

-   Defects for Test Case related list of the test case associated with the failed test.
-   Test Plan Defects related list of the test plan associated with the failed test.

## What to do next

After submitting the defect, you can modify it from the defect record. The role required to modify a defect depends on your organization's configuration. By default, the defect is assigned to the group or individual specified in the **Assignment group** and **Assigned to** fields.

