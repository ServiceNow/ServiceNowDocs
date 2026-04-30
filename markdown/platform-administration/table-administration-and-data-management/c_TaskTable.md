---
title: Working with the Task table
description: The Tasks \[task\] table is one of the core tables provided with the base system.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Table admin, Tables and data, Configure core features, Administer]
---

# Working with the Task table

The Tasks \[task\] table is one of the core tables provided with the base system.

The Tasks \[task\] table provides a series of [standard fields](../reference/r_ImportantTaskTableFields.md) used on each of the tables that extend it, such as the Incident \[incident\] and Problem \[problem\] tables. In addition, any table that extends the Tasks \[task\] table can take advantage of task-specific functionality for driving tasks.

The Planned Task plugin provides the Planned Task \[planned\_task\] table, which extends the Tasks \[task\] table to provide more fields for tasks to measure duration and effort.

## Creating tasks

The Tasks \[task\] table provides means for creating and completing tasks, as well as tracking their workflow in your instance.

Tasks aren't created directly on the Tasks \[task\] table. Instead, tasks are created on task child tables. To create a record in a task child table, access the Tasks \[task\] table by entering `task.list` in the navigation filter, and then select **New**. In the Task Interceptor, select the desired task child table.

## Tools for completing tasks

These tools can be run on any table which extends Task.

-   Approvals

    Approvals can be generated to a list of Approvers, either manually or automatically, according to Approval Rules. Approvals can be incorporated into workflows or can stand alone. For more information, see [Process approvals](https://www.servicenow.com/docs/access?context=c_ProcessApprovals&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    Approvals can be used on tables that do not extend Task.

-   Assignments

    Assignment rules can automatically assign tasks to users or groups, ensuring that the most appropriate team members handle the tasks. For more information, see [Defining Assignment Rules](c_DefineAssignmentRules.md).

-   Service levels

    Service level agreements can track the amount of time that a task has been open, to ensure that tasks are completed within an allotted time.

-   Inactivity monitors

    Inactivity monitors ensure that tasks do not fall by the wayside by notifying users when tasks have been untouched for a predefined period of time. For more information, see [Set an inactivity monitor](../../time/task/t_SetAnInactivityMonitor.md).

-   Workflow Studio

    A process owner can design a flow for tasks that meet certain conditions. After a task is created that meets the conditions, the flow applies an automated process to the task. The process is defined in Workflow Studio. For more information, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US).


## Modifying the Task table

Modifications made to the Tasks \[task\} table are applied to all child tables.

Be sure that changes are appropriate for all the child tables. Adding fields is a low-impact change, because you can hide fields on tables that don't need them. However, if the fields are being used across tables, deleting fields may cause unwanted data loss.

**Note:** When adding choice list entries to a choice list on the Tasks \[task\] table, make sure that the entry value is unique.

You can use [dictionary overrides](../../data-dictionary-tables/concept/c_DictionaryOverrides.md) to change some parts of a field definition in a way that does not to not apply to all child tables.

## Tasks workflow

An administrator can specify a specific workflow process to apply to tasks that meet certain conditions.

Once a task is created that meets the conditions, the workflow applies the process to the task, asking for approvals, notifying users, generating other tasks, running scripts, and so on.

-   **[Task table structure](../../table-administration/concept/task-table-structure.md)**  
The Task table structure provides a framework to organize and store task-related data, and includes extensive customization options.
-   **[Defining assignment rules](c_DefineAssignmentRules.md)**  
The instance can automatically assign a task to a user or group based on pre-defined conditions by using data lookup rules and assignment rules.
-   **[Extending the Task table with Planned tasks](c_PlannedTask.md)**  
The Planned Task plugin provides a Planned Task `[planned_task]` table that extends the Task `[task]` table.
-   **[Creating many-to-many task relations](c_ManyToManyTaskRelations.md)**  
By default, tasks can be related to each other using a parent/child relationship, such as a Problem with a group of child Incidents or a Catalog Request with a group of child Catalog Tasks.
-   **[Time Card Management](time-card-management.md)**  
The Time Card Management feature enables time card users such as task assignees to report and track their time for the assigned tasks.

**Parent Topic:**[ServiceNow AI Platform tables and data](../../general/concept/tables-fields-and-forms.md)

