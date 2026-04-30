---
title: Hide a global list or form action from a table or view
description: Use an action exclusion record to exclude a list or form action from a specified table, view, or table within a view.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing Configurable Workspace with declarative actions, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Hide a global list or form action from a table or view

Use an action exclusion record to exclude a list or form action from a specified table, view, or table within a view.

## Before you begin

Role required: admin

## About this task

An action exclusion record enables you to hide a global list or form action from a table, view, or table within a view. For example, you can hide a list action from a specific workspace, an Incident table, or an Incident table in a specific workspace.

## Procedure

1.  Navigate to `sys_workspace_declarative_action_exclusion.do`.

    A new action exclusion record opens.

2.  Complete the following fields.

    -   **Action assignment**

        Select the action that you want to exclude.

    -   **Table**

        Select the table that you want to exclude the action from.

    -   **Exclude this table**

        Select the check box to exclude the action from the selected table.

    -   **Exclude all child tables**

        Select the check box to exclude the action from all child tables of the selected table.

    -   **View**

        Select a view to exclude the action from.

    **Note:**

    -   To save an action exclusion record, you must select a table or view.
    -   If you select a table, you must also select **Exclude this table** or **Exclude all child tables** for an exclusion to occur.
    -   If you select a table but not a view, the action is excluded from the selected table regardless of the view.
    -   If you select a view but not a table, the action is excluded from the selected view regardless of the table.
    -   If you select both a table and a view, the action is excluded from the selected table within the selected view.
3.  Select **Submit**.


