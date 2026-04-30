---
title: Run your tests from the List view
description: View the test scenario, execute all the steps of the test, and review the test result.
locale: en-US
release: zurich
product: Test Management
classification: test-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sprint testing, Test Management 2.0, Test Management applications, Strategic Portfolio Management]
---

# Run your tests from the List view

View the test scenario, execute all the steps of the test, and review the test result.

## Before you begin

Role required: scrum\_user

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Agile Board**.

2.  Click the **Sprint Tracking** tab and select the **List** view.

3.  Click a test.

4.  Verify a story by clicking **Run** on the story.

    This step runs all tests of the story at once.

5.  In the pop-up, select the environment on which the test is to be run.

    1.  Click **Lookup using list** icon.
    2.  Click **Run**.
6.  In the Test Execution pop-up, mark a step as passed, failed, or blocked using the following icons.

    |Icon|Description|
    |----|-----------|
    |**![Step passed icon](../../sdlc-scrum/image/passedtest.png)**|Passed.|
    |**![Step failed icon](../../sdlc-scrum/image/failedtest.png)**|Failed. In this state, options to add comments and attachments are available. Option to delete attachments is also available.|
    |**![Step blocked icon](../../sdlc-scrum/image/blockedtest.png)**|Blocked. In this state, options to add comments and attachments are available. Option to delete attachments is also available.|

    -   To select an icon, you can also use the **Tab** key. Press **Tab** and then press **Enter**.
    -   To pause and work on the test at a later point in time, click **Pause**.
7.  Click **Done**.


## Result

Test result is saved to the Test Result form, and the latest test result of each test is displayed in the List view.

The overall status of the test is defined by statuses of the test steps:

-   If all the test steps are passed, the status of the test is **Passed**.
-   If at least one step of the test is not run, the status of the test is **Not finished**.
-   If at least one step of the test fails, the overall status of the test is **Failed**. This rule takes precedence over the previous rule.
-   If at least one step of the test is blocked, the overall status of the test is **Blocked**. This rule takes precedence over the previous two rules.

**Parent Topic:**[Sprint testing](../concept/sprint-testing.md)

**Related topics**  


[Create a test for a story](create-test-plan-for-story-agile2.md)

