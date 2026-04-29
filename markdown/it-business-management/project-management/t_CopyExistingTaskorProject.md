---
title: Copy an existing task or project
description: Save time when building a project by copying tasks from other projects.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a project task from a project, Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Copy an existing task or project

Save time when building a project by copying tasks from other projects.

## Before you begin

Role required: it\_project\_manager

## About this task

The **Copy partial project** option copies a selected task and its child tasks into the project, or all project tasks into a sub-project. It also preserves all dependencies and relationships among the copied tasks and their child tasks. Any relationships or dependencies that involve tasks outside of the scope of the copied task are not preserved.

## Procedure

1.  In the Project or Project Task form, right-click the header bar and select **Copy partial project**.

2.  In the **Task** field, select a project task or project to copy.

    By default, projects begin with PRJ and project tasks begin with PRJTASK.

3.  Enter a **Name** for the new project or task.

4.  Select **OK**.

    The copied task is added to the current task or project. If a project was copied, then all the tasks are inserted into a new sub-project.


## Result

The copied tasks are inserted as a child of whatever task or project that you are currently viewing. Actual duration and the actual start and end dates are reset to null values. The state is set to **New** and percent complete is set to **0**.

By default only the short description, planned dates and duration fields are copied from source project to the target project. If additional columns must be copied, they should be declared in the [project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) **List of attributes that will be copied from the originating project task**.

-   **[Change default values of copied fields](t_ChangeDefaultValCopiedProjTasks.md)**  
Change the default values of in the new partial project.

**Parent Topic:**[Create a project task from a project](t_CreateATaskFromAProject.md)

**Related topics**  


[Change default values of copied fields](t_ChangeDefaultValCopiedProjTasks.md)

