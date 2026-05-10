---
title: Run your test assignments in Test Management 2.0
description: Run your test assignments and capture the results.
locale: en-US
release: australia
product: Test Management
classification: test-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Testing using Test Management 2.0, Test Management 2.0, Test Management applications, Strategic Portfolio Management]
---

# Run your test assignments in Test Management 2.0

Run your test assignments and capture the results.

## Before you begin

Before you begin, ensure the following conditions are met:

-   Your test manager has set the tests to **Ready** state and assigned them to you.
-   At least one execution environment is configured in your instance.

Role required: sn\_test\_management.tester

## Procedure

1.  Navigate to **All** &gt; **Test Management 2.0** &gt; **Tests Assigned to me**.

2.  Select the required tests and click **Run**.

    Only the tests that are in the Ready state can be run.

    If no tests appear in the **Tests Assigned to me** list, confirm with your test manager that tests have been assigned to you and set to **Ready** state.

3.  In the pop-up, select the execution environment on which the tests must be run.

    An execution environment specifies the hardware or software configuration on which tests run, such as a browser version or operating system. If no environments appear in the list, contact your system administrator to configure one.

4.  In the Test Execution pop-up, mark a step as passed, failed, or blocked using the following icons.

<table id="choicetable_p33_dsw_dcb"><thead><tr><th align="left" id="d278807e123">

Icon

</th><th align="left" id="d278807e126">

Description

</th></tr></thead><tbody><tr><td id="d278807e132">

**![Icon to indicate a step as passed](../../sdlc-scrum/image/passedtest.png)**

</td><td>

Passed.

</td></tr><tr><td id="d278807e147">

**![Icon to indicate a step as failed](../../sdlc-scrum/image/failedtest.png)**

</td><td>

Failed. In this state, options to add comments and attachments are available. **Note:**

To log a defect in Test Management 2.0, create a defect record manually and include the test name and step number in the defect description.

</td></tr><tr><td id="d278807e171">

**![Icon to indicate a step as blocked](../../sdlc-scrum/image/blockedtest.png)**

</td><td>

Blocked. In this state options to add comments and attachments are available.

</td></tr></tbody>
</table>    To pause and work on the test at a later point in time, click **Pause**.

5.  Click **Done**.


## Result

Test results are saved to the Test Result form. The overall status of the test is defined by statuses of the test steps:

-   If all the test steps are passed, the status of the test is **Passed**.
-   If at least one step of the test is not run, the status of the test is **Not finished**.
-   If at least one step of the test fails, the overall status of the test is **Failed**.This rule takes precedence over the previous rule.
-   If at least one step of the test is blocked, the overall status of the test is **Blocked**. This rule takes precedence over the previous two rules.

## What to do next

To view the full history of test runs and results across all test plans, navigate to **Test Management 2.0** &gt; **Test Runs**. For more information about monitoring test plan progress, see [Test Board in Test Management 2.0](../concept/test-board.md).

**Parent Topic:**[Testing using Test Management 2.0](../concept/release-readiness-testing.md)

**Related topics**  


[Create a test in Test Management 2.0](create-test2.md)

[Create a test set in Test Management 2.0](create-test-set.md)

[Test Board in Test Management 2.0](../concept/test-board.md)

[Create a test execution suite in Test Management 2.0](create-test-execution-suite.md)

