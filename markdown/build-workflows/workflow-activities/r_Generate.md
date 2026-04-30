---
title: Generate workflow activity
description: The Generate activity immediately creates task or approval records from any task or approval activities placed after the Generate activity in the workflow path. These pre-generated tasks and approvals start when the task and approval activities are reached during flow execution. This allows a task to have a set of associated pre-generated sequential tasks or approvals, but still require them to be completed in order.
locale: en-US
release: xanadu
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Approval and rollback workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Generate workflow activity

The **Generate** activity immediately creates task or approval records from any task or approval activities placed after the **Generate** activity in the workflow path. These pre-generated tasks and approvals start when the task and approval activities are reached during flow execution. This allows a task to have a set of associated pre-generated sequential tasks or approvals, but still require them to be completed in order.

**Note:** This activity is only available when the workflow runs on a table that extends Task.

By default, the workflow does not create any tasks or approvals until it reaches them in the workflow.

The **Generate** activity follows all transitions through the workflow to each activity. For each activity:

-   If it is a [task activity](https://www.servicenow.com/docs/access?context=r_TaskActivities&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US), creates the task and sets:

    -   The **State** to **Pending**
    -   The **Expected Start Date**
    -   The **Due Date**
    **Note:** Task activities run as the user whose actions complete the task the workflow was waiting for and advances the workflow.

-   If it is an approval activity, creates the approvals and sets:

    -   The approval **State** to **Not Requested**
    -   The **Expected Start Date**
    -   The **Due Date**
    **Note:** Approval activities run as the user whose actions match the approve or reject conditions the workflow was waiting for and advances the workflow.


Expected start dates and due dates are calculated based on the **Expected Duration** of all of the tasks and approvals between the **Generate** activity and the activity being updated. In the case of a branched path \(between a **Branch** and **Join** activity\), the longer duration will be used for any post-branch activities.

The **Generate** activity can be used more than once, and any tasks or approvals will be refreshed with updated information. This is useful in situations where the list of approvers or other important information is still editable while the workflow is in process and it may be necessary to update or correct the generated approvals or tasks.

To exclude a set of activities from the **Generate** activity, select the **Skip during generate** check box on any condition and its transitions will not be followed during the generate process. By default, the following conditions have the **Skip during generate** check box selected:

-   **Rejected** \(for any of the approval activities\)
-   **No** condition of **If** activity
-   **Continue** condition of **Turnstile** activity
-   **Incomplete** condition of **Join** activity

## Input variables

Input variables determine the initial behavior of the activity.

|Field|Description|
|-----|-----------|
|Generate approvals|If selected, approvals are created when running the **Generate** activity. If cleared, the approvals are used to compute their estimated duration, but no approvals are created.|
|Generate tasks|If selected, tasks are created when running the **Generate** activity. If cleared, the tasks are used to compute their estimated duration, but no tasks are created.|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The activity is executing.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|

## Example

![Sample workflow that uses the Generate activity](../image/GenerateWorkflow.png "Generate workflow")

In this example, the following approvals are generated:

-   Approval-2
-   Approval-3

Approval-4 is skipped since the **Rejected** condition of Approval-3 has **Skip during generate** selected.

Here is an example of using the **Generate** activity that describes the expected start and due dates:

![](../image/GenerateWorkflowStartAndDueDate.png "Generate workflow start and due date")

In this example, if the **Generate** activity is run on Jan 1, 2016, the following expected start dates and due dates would be set for the generated tasks.

|Task|Expected Start Date|Reason|Due Date|
|----|-------------------|------|--------|
|Task 1 \(1 day\)|Jan. 1, 2016| |Jan. 2, 2016|
|Task 2 \(1 day\)|Jan. 2, 2016|Task 1 is 1 day|Jan. 3, 2016|
|Task 3 \(2 days\)|Jan. 1, 2016| |Jan. 3, 2016|
|Task 4 \(1 day\)|Jan. 3, 2016|Task 3 is 2 days|Jan. 4, 2016|
|Task 5 \(1 day\)|Jan. 4, 2016|Task 4 ends the latest before the Join|Jan. 5, 2016|

Notice that Task 5 starts on Jan. 4, 2016 since the longest path \(based on due dates\) to the **Join** is Task 3/Task 4.

