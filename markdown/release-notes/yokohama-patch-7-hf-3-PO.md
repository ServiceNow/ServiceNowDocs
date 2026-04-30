---
title: Yokohama Patch 7 Hotfix 3
description: The Yokohama Patch 7 Hotfix 3 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-10-01"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 7 Hotfix 3

The Yokohama Patch 7 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 09-30-2025\_0847

    Build tag: glide-yokohama-12-18-2024\_\_patch7-hotfix3-09-24-2025


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

 PRB1843211

</td><td>

Only the 'Save a copy' option should be available for the 'Shared with me' and 'Opened by link' sections

</td><td>

The rename, delete, save, and share options are all available for a list in the 'Shared with me' or 'Opened by link' sections. Only the 'Save a copy' option should be available.

</td><td>

1.  Navigate to **UI Builder** &gt; **List page template**.
2.  Add the filters to the default list.
3.  Copy and paste the URL in a new tab.
4.  Save the list in the 'Created by me' section.
5.  Share the list with a user.
6.  Impersonate that user.
7.  Load the list in the 'Shared with me' section.
8.  Select the three dots.

 Expected behavior: Only the 'Save a copy' option is available.

 Actual behavior: The rename, delete, save, and share options are available.

</td></tr><tr><td>

Condition Builder

 PRB1927599

</td><td>

The condition builder on the presentational list displays all the options instead of the one that was searched

</td><td>

When the user searches for an option, the condition builder displays all the options in a drop-down list and highlights the one that was searched. Instead, only the option that was searched should be displayed.

</td><td>

1.  Create a UI Builder page.
2.  Configure the presentational list component.
3.  Open the page in run time.
4.  Select the filter icon.
5.  In one of the fields, search for an option.

 Expected behavior: The list displays only the option that was searched.

 Actual behavior: The list displays multiple options and highlights the one that was searched.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 7 Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2524621)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

