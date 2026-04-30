---
title: Assign a defect to a test case
description: Assign an existing defect to a test case to track the relationship between defects and test cases.
locale: en-US
release: xanadu
product: Test Management
classification: test-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Test Management 1.0, Test Management applications, Strategic Portfolio Management]
---

# Assign a defect to a test case

Assign an existing defect to a test case to track the relationship between defects and test cases.

## Before you begin

-   [Activate Agile Development 2.0](../../agile-development/task/activate-agile-development.md)

    The ability to assign a defect is available only if the Agile Development 2.0 plugin is activated.

-   A defect record must exist in your instance. If no defect exists, create one first. For more information, see [Report a defect from a failed test](t_ReportADefectFromAFailedTest.md).
-   Perform tests and update the test status. For more information, see [Performing tests and updating the test status](../concept/c_Tester.md).
-   Role required: tm\_tester

## About this task

When you link a defect to a test case, a reference to the defect is added both to the test case and the test plan of this test case.

## Procedure

1.  Navigate to **All** &gt; **Test Management** &gt; **Test Execution** &gt; **Test Plans**.

2.  Open a test plan which contains your test case.

3.  From the Test Cases related list, open the test case to which you want to assign the defect.

4.  Click **Assign Defect.**

5.  Select a defect from the **Defect** field..

6.  Click **OK**.


## Result

The defect that you assigned to the test case is added to the following related lists:

-   Defects for Test Case related list of the test case.
-   Test Plan Defects related list of the test plan associated with the test case.

You can also configure the Defect form to display the Test Cases related list so that you can see the test case associated with this defect.

