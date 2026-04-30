---
title: Create a test for a story
description: Create a test from the Sprint Tracking view to automatically link it to a story and track whether the story meets its acceptance criteria.
locale: en-US
release: yokohama
product: Test Management
classification: test-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Sprint testing, Test Management 2.0, Test Management applications, Strategic Portfolio Management]
---

# Create a test for a story

Create a test from the Sprint Tracking view to automatically link it to a story and track whether the story meets its acceptance criteria.

## Before you begin

-   Role required: scrum\_user or scrum\_admin
-   You can create a test from the List view only when Agile Development 2.0 is installed along with Test Management 2.0.
-   You must be a member of an agile group.

## About this task

Create a test, add steps to the test, and create and maintain different versions of the test. A test is a collection of conditions or steps used to determine whether a story is working correctly. A test can also include an expected result, which determines whether the test passes or fails. When you create a test from the **Sprint Tracking** view, the test is automatically linked to the story displayed in that row. To confirm the link after creation, open the story record and locate the **Tests** related list.

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Agile Board**.

2.  Click the **Sprint Tracking** tab, and select the **List** view.

3.  From the **Show** list at the top right corner, select **Tests**.

4.  Click **Add Test**.

5.  To link an existing test to a story instead of creating a new one, open the story record from the sprint list and locate the **Tests** related list to add the pre-existing test.

    To create a standalone test to link later, see [Create a test in Test Management 2.0](create-test2.md).

6.  In the form, fill in the fields:

<table id="table_mty_wfd_scb"><thead><tr><th>

Field

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

Current state of the test.-   **Draft**: State of the test when it is created.
-   **Ready**: State of the test when it is not editable. When the test has multiple versions, only one test will be in the **Ready** state at any one time
-   **Retired**: State of the test when it is no longer used.


</td></tr><tr><td>

Short description

</td><td>

Brief description about the test.

</td></tr><tr><td>

Add Step

</td><td>

Button used to add step to a test.

</td></tr><tr><td>

Run

</td><td>

Button used to run steps, which is displayed only when the test is in the **Ready** state. See [Run your tests from the List view](run-test-plan-within-agile2.md).

</td></tr><tr><td>

Update

</td><td>

Button used to update the details of a test version.

</td></tr><tr><td>

Ready

</td><td>

Button used to change the state of the test version to ready.

</td></tr><tr><td>

Create New Version

</td><td>

Button used to create another version of the test.

</td></tr><tr><td>

Delete

</td><td>

Button used to delete the test version.

</td></tr><tr><td>

Change step order \(![Change step order icon](../../sdlc-scrum/image/draganddropicon.png)\)

</td><td>

Icon used to change the order of a test step. Select the icon and drag the step to the required location.

</td></tr><tr><td>

Needs Verification

</td><td>

Check box used to mark a test step for verification.

</td></tr><tr><td>

Delete a test step \(![Delete a test step icon](../images/deleteteststep.png)\)

</td><td>

Icon used to delete a test step.

</td></tr></tbody>
</table>
## What to do next

View information in the following related lists:

|Related list|Description|
|------------|-----------|
|Other versions|Displays all the versions of a test.|
|Test Results|Displays the run results of each test version.|
|Test Sets|Displays related tests in a test set.|

Tests created through this workflow are automatically linked to the story. To confirm the link, open the story record and locate the **Tests** related list, which displays all tests associated with that story.

**Parent Topic:**[Sprint testing](../concept/sprint-testing.md)

**Related topics**  


[Run your tests from the List view](run-test-plan-within-agile2.md)

