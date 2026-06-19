---
title: Define user actions for task logging
description: Group workstation user actions as a task that can be logged to provide data for a Task activity analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/task-mining/mine-data.html
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [task scope]
breadcrumb: [Defining the scope of projects, Use, Task Mining, Platform Analytics]
---

# Define user actions for task logging

Group workstation user actions as a task that can be logged to provide data for a Task activity analysis.

## Before you begin

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Navigate to the project you want to group tasks for.

3.  Select **Task scope** from the navigation pane.

    If the list of active tasks is empty, no tasks have been defined for this project.

4.  Select **Skip** if you aren't adding any mapped or user-initiated tasks.

5.  Select **Add task scope**.

6.  Select the type of task scope you want to create.

    The available options are:

    -   **__Automated__**

        Activity collection is based on mapped task activities.

    -   **__User-initiated__**

        Activity collection is user-initiated tasks. Workstation users start and stop activity collection by following instructions. Targeted activity collection only uses user-initiated task scopes, and at least one task must be defined if you choose this option.

    \[Omitted image "tm-add-task-scope.png"\] Alt text: Screenshot showing task scope options.

7.  On the form, fill in the fields.

8.  |Field|Description|
|-----|-----------|
|Task name|Name for the automated task.|
|Source table|The table from which you choose what actions to group.|
|Edit conditions|Conditions based on the selected source table that determine the required task.|
|Activity|Activity that you want to group and from which you want to retrieve task state changes.|
|Start|State that triggers the starting point of the task.|
|End|State that triggers the end point of the task.|

    \[Omitted image "tm-task-scope-project.png"\] Alt text: Screenshot showing automated task scope fields.

    |Field|Description|
    |-----|-----------|
    |Task name|Name for the user-initiated task.|
    |Task instructions|Directions for workstation users to start and stop activity collection.|

    \[Omitted image "tm-user-initiated-task.png"\] Alt text: Screenshot showing user-initiated task fields.

9.  Select **Capture screenshots to create desktop actions** to collect desktop actions automation properties.

    Capture both steps and desktop actions automation properties in a single recording session, instead of recording the same process twice. When a Task Mining analyst submits the automation request, the recording is delivered to the automation team with all UI properties needed to build desktop actions.

10. Repeat the task scope creation flow \(steps 5–8\) for every task you want to add to this project.

11. Select **Save and continue**.


## Defining a P1 incident tracking task

To configure a task to track the status of P1 incidents from creation to closing, set the values in the following table.

|Field|Value|
|-----|-----|
|Source table|Incident|
|Activity|State|
|Start|New|
|End|Closed|

\[Omitted image "tm-task-example.png"\] Alt text: Screenshot showing the example task.

## What to do next

Select workstation users you want to collect activity data from and create data requests. For more information, see [Add workstation users to a Task Mining project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/add-users-to-task-mining-project.md).

