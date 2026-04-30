---
title: Define user actions for task logging
description: Group workstation user actions as a task that can be logged to provide data for a Task activity analysis.
locale: en-US
release: yokohama
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2024-08-28"
reading_time_minutes: 1
breadcrumb: [Defining the scope of projects, Use, Task Mining, Platform Analytics]
---

# Define user actions for task logging

Group workstation user actions as a task that can be logged to provide data for a Task activity analysis.

## Before you begin

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the name of the project you want to group tasks for.

3.  Select the **Task scope** tab.

    If the list of active tasks is empty, no tasks have been defined for this project.

4.  Select **Create task**.

5.  On the form, fill in the fields.

6.  |Field|Description|
|-----|-----------|
|Name|Name for the task.|
|Source Table|The table from which you choose what actions to group.|
|Filter|Condition based on the selected source table that determines the required task.|
|Activity Mapping|Activity that you want to group and from which you want to retrieve task state changes.|
|Start Pattern Point|State that triggers the starting point of the task.|
|End Pattern Point|State that triggers the end point of the task.|

7.  Select **Submit**.


## Task definition for P1 incidents

To configure a task to track the status of P1 incidents from creation to closing, you would set the values in the following table.

|Field|Value|
|-----|-----|
|Source Table|Incident|
|Activity Mapping|State|
|Start Pattern Point|New|
|End Pattern Point|Closed|

## What to do next

Select an analysis from available templates to tailor how the Task Mining project aggregates your workstation data. For more information, see [Define how your data is analyzed and visualized](create-and-edit-categorization-rules.md).

