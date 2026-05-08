---
title: Run a test for a SAFe story
description: View the test scenario and execute all the steps of a test for verifying a SAFe story.
locale: en-US
release: australia
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Track your SAFe team work from the list view, SAFe Board — Team level, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Run a test for a SAFe story

View the test scenario and execute all the steps of a test for verifying a SAFe story.

## Before you begin

Role required: safe\_scrum\_user or safe\_admin

## Procedure

1.  Navigate to **All** &gt; **Scaled Agile Framework \(SAFe\)** &gt; **SAFe Board**.

2.  From the list at the top left corner, select the level as **Team**.

3.  From the adjacent list, select the required team value.

4.  Click the **Sprint Tracking** tab, and select the **List** view.

5.  From the list, select **Tests**.

6.  Verify a story by clicking the **Run** button.

    This action runs all tests of the story at once.

7.  In the pop-up, select the environment on which the test has to be run.

8.  In the Test Execution pop-up, mark a step as passed, failed, or blocked using the following icons.

<table id="choicetable_p33_dsw_dcb"><thead><tr><th align="left" id="d191893e125">

Icon

</th><th align="left" id="d191893e128">

Description

</th></tr></thead><tbody><tr><td id="d191893e134">

**![Icon to indicate a step as passed](../images/passed.png)**

</td><td>

Passed.

</td></tr><tr><td id="d191893e149">

**![Icon to indicate a step as failed](../images/failed.png)**

</td><td>

Failed. In this state, options to add comments and attachments are available. Option to delete attachments is also available.

</td></tr><tr><td id="d191893e164">

**![Icon to indicate a step as blocked](../images/blocked.png)**

</td><td>

Blocked. In this state, options to add comments and attachments are available. Option to delete attachments is also available. **Note:** If a test step is blocked, you will not be able to proceed and verify the remaining steps of the test.

</td></tr></tbody>
</table>    -   To select an icon, you can also press **Tab** and then press **Enter**.
    -   To pause and work on the test at a later point in time, click **Pause**.
9.  Click **Done**.


## Result

The test result is saved to the Test Result form. The latest test result of each test is displayed in the List view.

The overall status of the test is defined by statuses of the test steps:

-   If all the test steps are passed, the status of the test is **Passed**.
-   If at least one step of the test is not run, the status of the test is **Not finished**.
-   If at least one step of the test fails, the status of the test is **Failed**. This rule takes precedence over the previous rule.
-   If at least one step of the test is blocked, the status of the test is **Blocked**. This rule takes precedence over the previous two rules.

