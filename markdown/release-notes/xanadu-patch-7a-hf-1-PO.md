---
title: Xanadu Patch 7a Hotfix 1
description: The Xanadu Patch 7a Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-05-09"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 7a Hotfix 1

The Xanadu Patch 7a Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 05-06-2025\_1203

    Build tag: glide-xanadu-07-02-2024\_\_patch7a-hotfix1-04-27-2025


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

Service Portal

 PRB1502280

 [KB0994649](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0994649)

</td><td>

The **file attachment** field does not appear on the portal form page

</td><td>

The file attachment field **My file** doesn't appear on the form page of the incident record.

</td><td>

1.  Log in as an admin user.
2.  Open the form page of the incident record.

 Notice that the file attachment field **My file** doesn't appear on portal, but shows in native view.

</td></tr><tr><td>

List Administration

 PRB1810106

</td><td>

**Opened by** different states are overridden with the latest state value

</td><td>

When a new **Opened by** timestamp is created, the **State** field is changed and overrides the previous state value.

</td><td>

1.  Open the UI Builder.
2.  Add the **List page**template.
3.  Select **Incidents** &gt; **All**.
4.  Apply a filter matching Priority 4.
5.  Load the URL.
6.  Notice that in output 1, a new 'Opened by' timestamp is created with the Priority 4 filter.
7.  Apply a filter matching the **State** field.
8.  Load the URL.
9.  Notice that in output 2, a new 'Opened by' timestamp is created with the Priority 4 filter and the **State** field is changed.
10. Navigate to the list containing output 1.

 Expected behavior: A new 'Opened by' timestamp is created with the Priority 4 filter.

 Actual behavior: A new 'Opened by' timestamp is created with the Priority 4 filter and **State** field changes, and the previous state values are overridden.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 7a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2038547)
-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

