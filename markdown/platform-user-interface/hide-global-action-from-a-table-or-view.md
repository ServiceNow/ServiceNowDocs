---
title: Hide the global list and form actions from a table or view
description: Configure the list and form actions to exclude specified tables and views.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizing Configurable Workspace with declarative actions, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Hide the global list and form actions from a table or view

Configure the list and form actions to exclude specified tables and views.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_declarative_action_assignment`.

2.  Open the global list or form action that you want to hide by selecting your action.

3.  Open the **Action Exclusions** related list and select **New**.

4.  Apply the following configurations to the Action Exclusion record.

    |Field|Configuration|
    |-----|-------------|
    |Action assignment|The action exclusion record.|
    |Table|Table that excludes the action.|
    |Exclude this table|Option to exclude the action from the selected table.|
    |Exclude all child tables|Option to exclude the action from all child tables.|
    |View|View to exclude from the action.|

    **Note:**

    -   You’re required to select a table or view to save an Action Exclusion record.
    -   If you specify both a table and a view for exclusion, the action only excludes the action under the corresponding table within the specified view.
    -   If you only select a view to exclude, the action excludes from the specified view regardless of the table.
    -   In all cases that you select a table to exclude, you must select **Exclude this table** or **Exclude all child tables** for an exclusion to occur.

