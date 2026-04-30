---
title: Xanadu Patch 8 Hotfix 1
description: The Xanadu Patch 8 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-04-17"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 8 Hotfix 1

The Xanadu Patch 8 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 04-14-2025\_2301

    Build tag: glide-xanadu-07-02-2024\_\_patch8-hotfix1-04-10-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Code Signing

 PRB1860810

</td><td>

Generate signatures for sys\_auto\_script table with wildcard mode

</td><td>

Generating signatures for sys\_suto\_script table records as they are invoking scripts writing to ecc\_queue directly from sys\_auto\_Script.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1820684

</td><td>

Some legacy dashboard widgets don't render

</td><td>

Legacy dashboard widgets don't render after the dashboard has been migrated to Platform Analytics and setting sys\_property glide.ui. choices.show\_missing to 'false'.

</td><td>

1.  Navigate to **sys\_widgets**.
    1.  Open the 'Filters' record.
    2.  Check **Active**.
    3.  Save the record.
2.  Create a new dashboard.
3.  Navigate to the **Add Widgets icon** &gt; **Widget Category** &gt; **Filters**.
4.  Add the record previously created to the dashboard.
5.  Migrate the dashboard to Platform Analytics.
6.  Open the migrated dashboard.
7.  Observe the legacy widget loads.
8.  Set sys\_property glide.ui. choices.show\_missing to 'false'.
9.  Refresh the migrated dashboard.

 Notice that now it will not render the legacy widget, and will only show \{\}.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1788955

</td><td>

Core UI dashboard list **Delete migrated Experience Dashboard** UI action is not working as expected

</td><td>

This problem is not related to the Next Experience migration, although it involves removing the migrated Experience dashboard.

</td><td>

1.  Navigate to **pa\_dashboards.list**.
2.  Select a dashboard.
3.  Select the **Delete migrated Experience Dashboard** UI action.

 Notice the info message, 'Dashboard has not been migrated'.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 8](xanadu-patch-8.md)
-   [Xanadu Patch 7](xanadu-patch-7.md)
-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

