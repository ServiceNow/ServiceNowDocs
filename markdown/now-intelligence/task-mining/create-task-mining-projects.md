---
title: Create a Task Mining project
description: Create a Task Mining project to analyze data for a specific purpose, and define how long project data is collected for.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/task-mining/create-task-mining-projects.html
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Defining the scope of projects, Use, Task Mining, Platform Analytics]
---

# Create a Task Mining project

Create a Task Mining project to analyze data for a specific purpose, and define how long project data is collected for.

## Before you begin

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select **New project**.

3.  On the form, fill in the fields.

4.  |Field|Description|
|-----|-----------|
|Name|Name for the project.|
|Description|Description of the project.|
|Start date|Date to start collecting workstation user data.|
|End date|Date to stop collecting workstation user data.|

    \[Omitted image "tm-project-details.png"\] Alt text: Screenshot showing project details interface

5.  Select the analysis you want to use for this project to determine how the Task Mining project aggregates your workstation data.

    The available options are:

    -   **Task activity**

        View the time spent and frequency of activities and applications workstation users use during tasks you grouped, such as resolving incidents. Workstation user actions are grouped as tasks to provide the data. For more information about defining tasks, see [Define user actions for task logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/mine-data.md).

    -   **Overall activity**

        Creates a layered overview of all categorized applications workstation users use. Use the Overall activity analysis to see how workstation users use applications in your organization.

    -   **Task timeline**

        Provides a detailed view of collected task activities. These tasks are the bases for taking task improvement actions, that is opening automation requests or sharing details of the task. Workstation user actions must be grouped as a task that can be logged to provide data for a Task timeline analysis. For more information about defining tasks, see [Define user actions for task logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/mine-data.md).

    \[Omitted image "tm-project-goal.png"\] Alt text: Screenshot showing Task Mining goal options.

6.  Select the activity collection cadence to use for this project.

    The available options are:

    -   **Continuous**

        Continuously collects workstation user activity over a specified period.

    -   **Targeted**

        Allows workstation users to start and stop activity collection by following instructions. Targeted activity collection uses only user-initiated tasks scopes, and at least one task must be defined.

    \[Omitted image "tm-project-collection.png"\] Alt text: Screenshot showing activity collection options.

7.  Select **Save and continue**.


## What to do next

Group actions as a task for a Task activity or Task timeline analysis. For more information, see [Define user actions for task logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/mine-data.md).

Select workstation users you want to collect activity data from and create data requests. For more information, see [Add workstation users to a Task Mining project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/add-users-to-task-mining-project.md).

