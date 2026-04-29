---
title: Hide a global form or list action from a table or view
description: Configure a global form or list action to exclude a specified table or view.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage action visibility, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Hide a global form or list action from a table or view

Configure a global form or list action to exclude a specified table or view.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** and select either **Form Actions** or **List Actions**.

2.  From the Action Assignments list, select an action.

    An Action Assignment record opens.

3.  Select the **Action Exclusions** related list tab.

4.  Select **New**.

    An Action Exclusion record opens.

5.  Complete the following fields:

    -   **Action assignment**

        Select the action the exclusion will apply to.

    -   **Table**

        Select a table to exclude the action from.

    -   **Exclude this table**

        Select to exclude the action from the selected table.

    -   **Exclude all child tables**

        Select to exclude the action from all child tables.

    -   **View**

        Select a view to exclude from action from.

    **Note:**

    -   You’re required to select either a table or view to submit an Action Exclusion record.
    -   If you select a table, you must select **Exclude this table** or **Exclude all child tables** for an exclusion to occur.
    -   If you specify both a table and view, the action is only excluded from the corresponding table within the specified view.
    -   If you only select a view, the action is excluded from the specified view regardless of the table.
6.  Select **Submit**.


## Result

The global form or list action is excluded from the specified table or view.

