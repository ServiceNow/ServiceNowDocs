---
title: Configure live updates for a list page
description: Configure live updates at the list page level without affecting other lists in your Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [list, lists, live updates]
breadcrumb: [Lists, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure live updates for a list page

Configure live updates at the list page level without affecting other lists in your Configurable Workspace.

## Before you begin

To configure live updates for lists, you must enable the **glide.lists.live\_list\_enabled** system property. For information on enabling the system property, see [Enable live updates for lists](live-list-updates-configurable-workspace.md).

Role required: admin

## About this task

Live updates enable list data to refresh automatically or manually without reloading the page.

You can configure live updates using the following options:

-   **Template-level configuration**

    Configure live updates at the template level in UI Builder.

    UI Builder enables you to choose how live updates behave across a list template in your Configurable Workspace. The property **Let users control live updates** has three menu options:

    -   **Never**

        The default selection that disables live updates.

    -   **Only by refreshing**

        An indicator displays on the refresh button when updates are available. The list will only update once refreshed manually.

    -   **Automatically**

        Live updates display automatically without refreshing.

-   **Page-level configuration**

    Use this procedure to configure live updates at the list page level without affecting other lists in your Configurable Workspace. This configuration uses the **sys\_ux\_list** table.


## Procedure

1.  Navigate to `sys_ux_list.list`.

2.  Open the list page you want to edit.

3.  Select the **Extensible List Feature Flags** tab.

4.  In the Live Updates field, select an option for live updates.

    -   **Off**

        Disables live updates.

    -   **Manual refresh**

        An indicator displays on the refresh button when updates are available. The list will only update once refreshed manually.

    -   **Automatic refresh**

        Live updates display automatically without refreshing.

5.  Select **Update**.


