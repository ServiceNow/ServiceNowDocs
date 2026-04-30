---
title: Initiate guided test execution
description: Create assessments for the assigned testers of each test case in a test plan by notifying them to start testing. The test manager can initiate guided test execution from the Test Plan form.
locale: en-US
release: yokohama
product: Test Management
classification: test-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Guided test execution, Setting up the manual testing process, Test Management 1.0, Test Management applications, Strategic Portfolio Management]
---

# Initiate guided test execution

Create assessments for the assigned testers of each test case in a test plan by notifying them to start testing. The test manager can initiate guided test execution from the Test Plan form.

## Before you begin

-   [Create a test plan](t_CreateATestPlan.md#).
-   Add test cases to the test plan.
-   [Assign testers from the Test Plan form](t_AssignTestersFromTheTestPlanForm.md).
-   Role required: tm\_test\_manager or tm\_tester

## About this task

If you are using guided test execution, you can notify testers to start testing directly from the Test Plan form. The testers are notified through an email about their assigned assessments. Testers can find these assessments by navigating to **Self-Service** &gt; **My Tests** or **Self-Service** &gt; **My Assessments**.

## Procedure

1.  Navigate to **Test Management** &gt; **Test Execution** &gt; **Test Plans**.

2.  Open the test plan that you want to start executing.

3.  From the Test Cases related list, use the **Assigned to** field to assign the test cases to testers.

4.  Click the **Notify Tester** related link.

5.  Enter a date in the **Testing end date** field and click **OK**.

    This date is used as the due date for the assessment.


## Result

Assessments for each tester are created and email is sent to each tester with the assessment and testing details. After the testers are notified through the email, the **Notify Tester** related link on the Test Plan form changes to **Cancel test execution**.

**Parent Topic:**[Guided test execution](../concept/c_GuidedTestExecution.md)

