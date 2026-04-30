---
title: Run tests for a story in Agile Development 2.0
description: For a story whose tests are marked ready to be run, run those tests and execute all the test steps using the Sprint Tracking tab of the Agile board in Agile Development 2.0.
locale: en-US
release: yokohama
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Agile Development 2.0, Strategic Portfolio Management]
---

# Run tests for a story in Agile Development 2.0

For a story whose tests are marked ready to be run, run those tests and execute all the test steps using the Sprint Tracking tab of the Agile board in Agile Development 2.0.

## Before you begin

Role required: scrum\_user

## About this task

From the Agile board, use the List view of the Sprint Tracking tab to check stories that have test versions ready to be run. These stories have a **Run** option next to their state. Run those tests by executing and verifying each test step.

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Agile Board**.

2.  From the Sprint Tracking tab, select the **List**view.

    All stories scheduled for the current sprint are listed as sections, which can be expanded and collapsed.

3.  From the **Show** field, select **Tests**

4.  For the story that you want to run the tests on, select **Run**.

5.  Select the environment on which the test is to be run and confirm by selecting **Run**.

6.  In the Test Execution window, execute each test step and mark them as passed, failed, or blocked accordingly.

    -   Passed \(![Step passed icon](../image/passedtest.png)\)
    -   Failed \(![Step failed icon](../image/failedtest.png)\)
    -   Blocked \(![Step blocked icon](../image/blockedtest.png)\)
    If you select Failed or Blocked for a test step, you can enter comments and attach files to support your selection.

7.  If you're running multiple tests for the story, use the Next Test option \(![Next test icon](../image/icon-next-test.png)\) to move to the next test after verifying the current one.

8.  Repeat step 6 and 7 until you've executed and verified all the test steps.

9.  You can pause the test for the moment by selecting **Pause**

    If you've paused the test, skip step 10.

    When you want to resume the paused test run later, you can find it at **Test Management** &gt; **Runs**.

10. After marking all test steps, select **Done**.


## Result

The result of each test is indicated on the Agile board as Passed, Failed, Blocked, or Not finished according to the following conditions.

-   If all the test steps are passed, the status is **Passed**.
-   If at least one step of the test is not executed, the status of the test is **Not finished**.
-   If at least one step of the test fails, the overall status of the test is **Failed**. This rule takes precedence over the previous rule.
-   If at least one step of the test is blocked, the overall status of the test is **Blocked**. This rule takes precedence over the previous two rules.

## What to do next

[View the test results for a story in Agile Development 2.0](view-test-result-form.md)

**Parent Topic:**[Using Agile Development 2.0](../../agile-development/concept/using-agile-development-2-0.md)

