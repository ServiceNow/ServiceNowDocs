---
title: Add or remove tasks from a work order task bundle
description: Add relevant tasks to a work order task bundle or remove tasks if the bundle becomes too large to manage.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Bundling work order tasks, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Add or remove tasks from a work order task bundle

Add relevant tasks to a work order task bundle or remove tasks if the bundle becomes too large to manage.

## Before you begin

Role required: wm\_dispatcher

## About this task

When you add tasks to a bundle, the order number assigned to the tasks continues sequentially, even if you removed the highest priority task from the bundle. For example, if you remove the task from the first order position while also adding a task, the new task is positioned last in order, after all the existing tasks.

When adding tasks to bundles, note the following restrictions:

-   Tasks can’t be schedule locked.
-   Tasks can’t be part of another bundle.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  In the left panel, select **Dispatcher Workspace**.

3.  Select the work order task bundle from which you want to add tasks to or remove tasks.

4.  Select the **Bundled tasks** tab.

5.  Either add a task to the bundle or delete a task from the bundle.

    -   To add a task, select **Add**, select the task, and select **Add**.
    -   To remove a task, select the task and select **Remove**.

