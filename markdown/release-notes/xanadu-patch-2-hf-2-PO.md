---
title: Xanadu Patch 2 Hotfix 2
description: The Xanadu Patch 2 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-11-27"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 2 Hotfix 2

The Xanadu Patch 2 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-23-2024\_0851

    Build tag: glide-xanadu-07-02-2024\_\_patch2-hotfix2-11-20-2024


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

Haraka \(Glide\)

 PRB1824231

 [KB1709920](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1709920)

</td><td>

sys\_kagami\_query\_ engine has an error on the column decision\_last\_ msg

</td><td>

Queries are not routing to postgreSQL after upgrading to Xanadu. Queries with 'group by' are attempting to route to Haraka, but are failing due to a syntax error.

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 2 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705551)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

