---
title: Create a test in Test Management 2.0
description: Create a test specifying conditions or steps to determine whether a feature is working correctly.
locale: en-US
release: australia
product: Test Management
classification: test-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Testing using Test Management 2.0, Test Management 2.0, Test Management applications, Strategic Portfolio Management]
---

# Create a test in Test Management 2.0

Create a test specifying conditions or steps to determine whether a feature is working correctly.

## Before you begin

Role required: sn\_test\_management.tester or sn\_test\_management.test\_manager

## Procedure

1.  Create a test using either of the following options.

<table id="choicetable_fmy_53j_5cb"><thead><tr><th align="left" id="d272195e61">

Option

</th><th align="left" id="d272195e64">

Description

</th></tr></thead><tbody><tr><td id="d272195e70">

**From Test Management 2.0**

</td><td>

1.  Navigate to **Test Management 2.0** &gt; **Tests**.
2.  To create a test, click **New**.


</td></tr><tr><td id="d272195e100">

**From Agile Development 2.0**

</td><td>

1.  Navigate to **Agile Development 2.0** &gt; **Agile Board**.
2.  Click the **Sprint Tracking** Tab.
3.  Select the **List** view.
4.  From the **Show** list at the top right corner, select **Tests**.
5.  Click **Add Test**.


</td></tr></tbody>
</table>2.  In the Test version form, fill in the test name and add steps for your test.

3.  Select **Submit**.

4.  From the list of Tests, open the test that you just created.

5.  From the Test versions related list, open the test version that you just created.

<table id="table_kfy_wl1_35b"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test

</td><td>

Unique name of the test.

</td></tr><tr><td>

Owner

</td><td>

Owner who created the test.

</td></tr><tr><td>

Version

</td><td>

Automatically generated version of the test.

</td></tr><tr><td>

State

</td><td>

Current state of the test. -   **Draft**: Initial state when a test is created. The test is editable in this state.
-   **Ready**: State when a test is approved for execution. The test is not editable in this state. To modify a test in Ready state, create a version using the **Create New Version** button.
-   **Retired**: State when the test is no longer used.
**Tip:**

To edit a test, open the test version, confirm that it is in **Draft** state, make your changes, and select **Update**.

</td></tr><tr><td>

Short description

</td><td>

Brief description about the test.

</td></tr><tr><td>

Add Step

</td><td>

Button used to add step to a test.

</td></tr><tr><td>

Change step order \(![Change step order icon](../../sdlc-scrum/image/draganddropicon.png)\)

</td><td>

Icon used to change the order of a test step. Select the icon and drag a step to the required location.This icon is displayed next to a test step.

</td></tr><tr><td>

Needs Verification

</td><td>

Check box used to mark a test step for verification.This icon is displayed after a test step is added.

If this checkbox is not selected, you need not verify that if this step passed, failed, or is blocked when you run the test.

</td></tr><tr><td>

Delete a test step \(![Delete a test step icon](../images/deleteteststep.png)\)

</td><td>

Icon used to delete a test step.

</td></tr><tr><td>

Run

</td><td>

Button used to run steps, which is displayed only when the test is in the **Ready** state.See [Run your test assignments in Test Management 2.0](run-your-test-assignments.md).

</td></tr><tr><td>

Update

</td><td>

Button used to update the details of a test version.

</td></tr><tr><td>

Ready

</td><td>

Button used to change the state of the test version to **Ready**.

</td></tr><tr><td>

Create New Version

</td><td>

Button used to create another version of the test.

</td></tr><tr><td>

Delete

</td><td>

Button used to delete the test version.

</td></tr></tbody>
</table>6.  Click **Submit**.


## What to do next

To add a test to a test set:

1.  Select the test from the Test list.
2.  Click **Add to Test Set**.

**Parent Topic:**[Testing using Test Management 2.0](../concept/release-readiness-testing.md)

**Related topics**  


[Create a test set in Test Management 2.0](create-test-set.md)

[Test Board in Test Management 2.0](../concept/test-board.md)

[Create a test execution suite in Test Management 2.0](create-test-execution-suite.md)

[Run your test assignments in Test Management 2.0](run-your-test-assignments.md)

