---
title: Configure live updates for lists
description: Add a system property that enables you to configure live updates for lists.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [list, lists, live updates]
breadcrumb: [Lists, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure live updates for lists

Add a system property that enables you to configure live updates for lists.

## Before you begin

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


Use this procedure to enable the system property required to configure live updates for lists.

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Add a system property named **glide.lists.live\_list\_enabled**.

    For more information on adding a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

3.  Set the Value to **true**.

4.  Select **Submit**.


## What to do next

Configure live updates for a page without affecting other lists in your workspace. For instructions, see [Configure live updates for a list page](live-list-updates-page-level.md).

