---
title: Define user actions for task logging
description: Group workstation user actions as a task that can be logged to provide data for a Task activity analysis.
locale: en-US
release: zurich
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Defining the scope of projects, Use, Task Mining, Platform Analytics]
---

# Define user actions for task logging

Group workstation user actions as a task that can be logged to provide data for a Task activity analysis.

## Before you begin

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Navigate to the project you want to group tasks for.

3.  Select **Task scope** from the left navigation.

    If the list of active tasks is empty, no tasks have been defined for this project.

4.  Select **Skip** if you aren't adding any mapped or user-initiated tasks.

5.  Select **Add task scope**.

6.  Select the type of task scope you want to create.

    The available options are:

    -   **Automated**

        Activity collection is based on mapped task activities.

    -   **User-initiated**

        Activity collection is user-initiated tasks. Workstation users to start and stop activity collection by following instructions. Targeted activity collection only uses user-initiated task scopes, and at least one task must be defined if you choose this option.

    ![Screenshot showing task scope options.](../image/tm-add-task-scope.png)

7.  On the form, fill in the fields.

8.  |Field|Description|
|-----|-----------|
|Task name|Name for the automated task.|
|Source table|The table from which you choose what actions to group.|
|Edit conditions|Conditions based on the selected source table that determines the required task.|
|Activity|Activity that you want to group and from which you want to retrieve task state changes.|
|Start|State that triggers the starting point of the task.|
|End|State that triggers the end point of the task.|

    ![Screenshot showing automated task scope fields.](../image/tm-task-scope-project.png)

    |Field|Description|
    |-----|-----------|
    |Task name|Name for the user-initiated task.|
    |Task instructions|Directions for workstation users to start and stop activity collection.|

    ![Screenshot showing user-initiated task fields.](../image/tm-user-initiated-task.png)

9.  Repeat steps 5–7 for every task you want to add to this project.

10. Select **Save and continue**.


## Task definition for P1 incidents

To configure a task to track the status of P1 incidents from creation to closing, you would set the values in the following table.

|Field|Value|
|-----|-----|
|Source table|Incident|
|Activity|State|
|Start|New|
|End|Closed|

![Screenshot showing the example task.](../image/tm-task-example.png)

## What to do next

Select workstation users you want to collect activity data from and create data requests. For more information, see [Add workstation users to a Task Mining project](add-users-to-task-mining-project.md).

