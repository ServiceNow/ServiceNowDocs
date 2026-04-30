---
title: Add external dependencies between projects from Project Workspace
description: Set up a dependency between tasks of different projects using the new Project Workspace.
locale: en-US
release: xanadu
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Add external dependencies between projects from Project Workspace

Set up a dependency between tasks of different projects using the new Project Workspace.

## Before you begin

Role required: it\_project\_manager

## About this task

External dependencies help you understand the impact on project schedules when there is a change in the predecessor task. Use the row context menu of your project task to add a dependency from the task of a different project.

## Procedure

1.  Open a project from the planning page of Project Workspace.

    For information on how to navigate to the planning page, see [Access the new Project Workspace](access-new-project-workspace.md).

2.  From the data grid, select the project task to which you want to add the dependency.

3.  Select the row context menu \(![Row context menu.](../image/icon-row-context-menu.png)\) of the task and select **Add external dependency**.

4.  On the External Dependency form, select the **Project** to which the external task belongs.

5.  Select the **Task** for which the dependency is added.

6.  Select the **Dependency type**.

7.  Select **Submit**.

    The default selection is **Hard**. In a hard dependency, any changes made in the predecessor project are automatically propagated to the successor project.


## Result

-   Dependency is created for the tasks of the two projects.
-   The short description of your project is greyed out and is renamed to indicate the external dependency in the format of **External project name: External task name**
-   A link icon \(![External dependency icon](../image/icon-dependency.png)\) is added to the short description cell of the task, to indicate the dependency.

## What to do next

You can navigate to the external project directly from the current project to view the status or update the details of the predecessor task. From the row context menu of the dependent task, select **View project**.

**Parent Topic:**[Managing projects with Project Workspace](../concept/use-projects-pw.md)

**Related topics**  


[External dependencies](../../project-management/concept/external-dependencies.md)

