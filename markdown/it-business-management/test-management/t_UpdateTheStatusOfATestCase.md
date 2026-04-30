---
title: Update the status of a test case
description: Manually update the status of a test case. The status of the individual tests in a test case does not affect the overall status of the test case.
locale: en-US
release: xanadu
product: Test Management
classification: test-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Test Management 1.0, Test Management applications, Strategic Portfolio Management]
---

# Update the status of a test case

Manually update the status of a test case. The status of the individual tests in a test case does not affect the overall status of the test case.

## Before you begin

Role required: tm\_test\_manager or tm\_tester

## Procedure

1.  Navigate to **All** &gt; **Test Management** &gt; **Test Repository** &gt; **Test Plans**.

2.  Open the test plan that contains your test case.

3.  From the **Test Cases** related list, click your test case.

4.  In the **Execution Status** field, select a status.

    -   **Unexecuted**: Test is not executed yet.
    -   **In Progress**: Testing is in progress for this test case.
    -   **Passed**: All tests assigned to this test case have a status of **Passed**.
    -   **Failed**: One or more of the tests assigned to this test case have a status of **Failed**.
    -   **Blocked**: One or more of the tests assigned to this test case have a status of **Blocked**.
    -   **Retest**: Test is ready to be run again as a defect resulting from a failed test has been set to Closed Complete.
5.  If you select **Blocked** as the status, enter a reason for this test being blocked in the **Blocked Reason** field.

6.  Save the update by using one of the following choices.

    -   Click **Submit** to save and return to the Test Cases list.
    -   Click **Save** to save and remain on the Test Case form.
    The test results are updated in the test plan.


## What to do next

If a test case has failed, you can create a defect for this test case from the failed test by clicking the **Report Defect** related link. For more information, see [Report a defect from a failed test](t_ReportADefectFromAFailedTest.md).

You can link an existing defect to the test case by clicking the **Assign Defect** related link. For more information, see [Assign a defect to a test case](t_AssignADefectToATestCase.md).

The reported and assigned defects are listed in the Defects for Test Case related list.

