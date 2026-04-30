---
title: Start a project
description: Starting a project is the next step after setting up the project, populating it with tasks, and assigning resources.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Start a project

Starting a project is the next step after setting up the project, populating it with tasks, and assigning resources.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  Open the project you want to start.

2.  Change the **State** field to **Work in Progress** and click **Save** to save the change.

    **Note:** You can not restart a project \(changing the state to Work in Progress\) or reopen it after it is closed. Updating the project state from Closed to Work In Progress, Pending, or Open is not allowed. Instead of reopening the project, reopen an existing project task or add a new task to the project. This moves the project from Closed to Work in Progress state without affecting the other closed tasks.


## Result

After you start the project:

-   The read-only **Actual start date** field of the project is populated with the planned date.
-   If a task or set of tasks are scheduled to start immediately upon project start \(meaning that their time constraints are set to **Start ASAP** and they have no other start dependencies\), the actual start dates of those tasks also get populated with the planned date.
-   The planned start dates of all other tasks adjust accordingly based on the time you started the project. Their new planned start dates depend on several factors, including dependent relationships with other tasks and the duration for each task.

    **Note:** Once a project is in the **Work in Progress** state, it does not mean that the state of every task will start updating automatically based on planned start date. Other than the project tasks that you schedule to start **ASAP** when the project starts, project tasks are not started automatically. Continue to manage the project and change the state of each task to **Work in Progress**.


