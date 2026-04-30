---
title: Xanadu Patch 6 Hotfix 2
description: The Xanadu Patch 6 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-04-10"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 6 Hotfix 2

The Xanadu Patch 6 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 04-07-2025\_0716

    Build tag: glide-xanadu-07-02-2024\_\_patch6-hotfix2-04-01-2025


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

UI Form Administration

 PRB1843602

</td><td>

Issue with the date picker position

</td><td>

The date picker position doesn't change when scrolling through the page.

</td><td>

1.  Open a form with a date field.
2.  Select the date picker.
3.  Scroll the page.

 Notice that the date picker remains in the same position on the screen even when scrolling.

</td></tr><tr><td>

Platform Analytics Filters

 PRB1838937

</td><td>

When a non-admin user creates a Platform Analytics Date filter, **Field** flashes briefly and is then cleared when selected, depending on the table chosen

</td><td>

Depending on the table chosen in the Data to filter modal, entries selected in **Field** flash briefly and are then cleared, and do not remain selected.

</td><td>

1.  Grant a non-admin user the analytics\_filter\_admin role.
2.  Impersonate the user.
3.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Filters**.
4.  Select **New**.
5.  Navigate to **Filter Type** &gt; **Date** &gt; **Data to filter** &gt; **Add**.
6.  Select **Task** in the field **Table** in the Data to filter modal.
7.  Select **Created** under **Field**.

 Observe that **Created** flashes briefly and is then cleared, and the selection does not remain.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 6 Hotfix 1](xanadu-patch-6-hf-1-PO.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

