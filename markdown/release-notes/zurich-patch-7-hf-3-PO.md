---
title: Zurich Patch 7 Hotfix 3
description: The Zurich Patch 7 Hotfix 3 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-7-hf-3-PO.html
release: zurich
topic_type: reference
last_updated: "2026-06-30"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 7 Hotfix 3

The Zurich Patch 7 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 06-26-2026\_0905

    Build tag: glide-zurich-07-01-2025\_\_patch7-hotfix3-06-10-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

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

Internationalization Features

 PRB1892286

 [KB2277705](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2277705)

</td><td>

A non-admin user can't change a dashboard name by specific steps when the system language is set to Japanese

</td><td>

The dashboard name should be updated correctly and reflected in both the primary record and its translated fields, as it is in the Washington and Xanadu versions. In the Yokohama version, the update to the dashboard name fails silently when the Japanese language is enabled and the sys\_translated record exists.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1993476

 [KB2961192](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2961192)

</td><td>

sys\_translated records are deleted unexpectedly when updating a tab name on a dashboard in Japanese

</td><td>

sys\_translated records are deleted from the sys\_translated table unexpectedly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1998900

 [KB3060060](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3060060)

</td><td>

Tab name translations find an incorrect translation value

</td><td>

Tab names may not be translated correctly in the Next Experience dashboard.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2008600

 [KB3060098](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3060098)

</td><td>

Platform Analytics Experience \(PAE\) tab translations don't work in non-English instances

</td><td>

The tab names should be preserved and not overridden.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2025067

</td><td>

The sys\_translated record for par\_dashboard\_tab is overwritten

</td><td>

This can cause translations to be lost.

</td><td>

1.  In English, create a sys\_translated record as follows:
    -   Label: あいう
    -   Table: par\_dashboard\_tab
    -   Element: name
    -   Language: ja
    -   Value: TabName
2.  Create a PAE Dashboard.
3.  Add a tab with the same name as the sys\_translated value \(TabName\).
4.  Save the dashboard.
5.  Create another dashboard.
6.  Add a tab with the same name as the sys\_translated value again.
7.  Save the dashboard.
8.  Switch the language to Japanese.
9.  Return to one of the dashboards.
10. Rename the tab あいう to さしす.
11. Check the other dashboard tab.

 Observe that the translation is lost because the sys\_translated record is overwritten.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 7 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7-hf-1-PO.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)

