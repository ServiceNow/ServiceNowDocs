---
title: Configure due dates for tasks
description: Configure due dates for different task types so that the Due date field is auto-populated when you create tasks for internal users and suppliers.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage supplier tasks, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure due dates for tasks

Configure due dates for different task types so that the **Due date** field is auto-populated when you create tasks for internal users and suppliers.

## Before you begin

Role required: sn\_slm.admin

## About this task

Although the **Due date** field is auto-populated for a task type, you can always update this field as required.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Administration** &gt; **Default Due Dates for Tasks**.

    The Decision Builder opens and displays the Decision table for configuring the default due dates.

    |Task type|Default due date|
    |---------|----------------|
    |Mark complete|3|
    |View link|3|
    |Play video|3|
    |Upload documents|3|
    |Complete a form|3|
    |Sign document|3|
    |Complete checklist|3|
    |Complete survey|3|

2.  Under the Default due date column, select a row next to the task type row and enter a positive number.

    The number that you enter for a task type is auto-populated in the **Due date** field the next time you create a task of that task type.

    For example, let's say that you enter 3 as the due date for the task type Mark complete. If you create a Mark complete task on September 12, the due date will be in three days from this date; that is, September 15.

3.  Select **Save**.


## Result

The default due dates for the different task types are configured.

**Parent Topic:**[Manage supplier tasks from the Source-to-Pay Workspace](../concept/managing-tasks.md)

**Related topics**  


[Create a task for a supplier case from the Source-to-Pay Workspace](create-new-task-for-supp-case.md)

[Submit a task from the Source-to-Pay Workspace](submit-supplier-task.md)

[Complete a supplier task from the Source-to-Pay Workspace](complete-supplier-task.md)

