---
title: Xanadu Patch 5 Hotfix 2
description: The Xanadu Patch 5 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 5 Hotfix 2

The Xanadu Patch 5 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 03-02-2025\_0728

    Build tag: glide-xanadu-07-02-2024\_\_patch5-hotfix2-02-27-2025


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

Activity Stream

 PRB1858894

</td><td>

Application Programming Interface \(API\), ServiceNow AI Platform, and GraphQL is slow due to the Table Cleaner being throttled causing heavy replication lag

</td><td>

API, ServiceNow AI Platform, and GraphQL calls are slow specifically because of the Table Cleaner on sys\_activity shards. ​Using Instant Alter added an index, and as a result, all records were replicated with the load causing replication lag. When replication lag is detected, Table Cleaners are throttled, which can exacerbate the amount of data that is being replicated and cause timeouts. Timeouts are caused by the Table Cleaner running synchronously in the Activity Stream load request.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 5 Hotfix 1](xanadu-patch-5-hf-1-PO.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

