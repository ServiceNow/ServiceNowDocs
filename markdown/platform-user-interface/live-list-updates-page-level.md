---
title: Configure live updates for individual list pages
description: Configure live updates at the list page level without affecting other lists in your Configurable Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [list, lists, live updates]
breadcrumb: [Lists, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure live updates for individual list pages

Configure live updates at the list page level without affecting other lists in your Configurable Workspace.

## Before you begin

To configure live updates for lists, you must enable the **glide.lists.live\_list\_enabled** system property. For instructions, see [Configure live updates](live-list-updates-configurable-workspace.md#).

Role required: admin

## About this task

Live updates enable list data to refresh automatically or manually without reloading the page.

To configure live updates, you must enable the **glide.lists.live\_list\_enabled** system property.

Once enabled, you can configure live updates using the following options:

-   **Template-level configuration**

    Configure live updates at the template level in UI Builder.

    UI Builder enables you to choose how live updates behave across a list template in your Configurable Workspace. The property **Let users control live updates** provides three options:

    -   **Never**

        The default selection that disables live updates.

    -   **Only by refreshing**

        An indicator displays on the refresh button when updates are available. The list will only update once refreshed manually.

    -   **Automatically**

        Live updates display automatically without refreshing.

-   **Page-level configuration**

    Configure live updates at for a list page without affecting other lists in your workspace. This configuration uses the **sys\_ux\_list** table.


Use this procedure to configure live updates for a list page.

## Procedure

1.  Navigate to `sys_ux_list.list`.

    The entire list of UX lists in the UX Lists \[sys\_ux\_list\] table opens.

2.  From the UX Lists list, select the list page you want to edit.

    A UX List record opens.

3.  Select the **Extensible List Feature Flags** tab.

4.  In the Live Updates field, select an option for live updates.

    -   **Off**

        Disables live updates.

    -   **Manual refresh**

        An indicator displays on the refresh button when updates are available. The list will only update once refreshed manually.

    -   **Automatic refresh**

        Live updates display automatically without refreshing.

5.  Select **Update**.


