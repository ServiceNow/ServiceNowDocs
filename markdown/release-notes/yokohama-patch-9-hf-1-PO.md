---
title: Yokohama Patch 9 Hotfix 1
description: The Yokohama Patch 9 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-11-21"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 9 Hotfix 1

The Yokohama Patch 9 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-18-2025\_1045

    Build tag: glide-yokohama-12-18-2024\_\_patch9-hotfix1-11-14-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

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

List Administration

 PRB1844590

</td><td>

Fixed queries don't work on 'My list' in workspace

</td><td>

When the user creates 'My List' and adds a condition, the list results don't change and the fixed filter isn't visible. However,it works in the backend view.

</td><td>

1.  Navigate to Service Operations Workspace \(SOW\) or HR workspace.
2.  Navigate to the 'My List' tab.
3.  Add a new list.
4.  Use 'Start from existing' or 'Create your own' to create 'My List' without conditions.
5.  After 'My List' is created, navigate to the sys\_ux\_my\_list table.
6.  Open the list.
7.  Add the 'Fixed query' condition 'Active=True' \(or any other condition\).

 Expected behavior: The list has fixed filters and filtered results.

 Actual behavior: The list results don't change and the fixed filter isn't visible \(but it's working on backend view\).

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 9](yokohama-patch-9.md)
-   [Yokohama Patch 8](yokohama-patch-8.md)
-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

