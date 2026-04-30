---
title: Yokohama Patch 3 Hotfix 3
description: The Yokohama Patch 3 Hotfix 3 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-06-17"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 3 Hotfix 3

The Yokohama Patch 3 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 06-11-2025\_2210

    Build tag: glide-yokohama-12-18-2024\_\_patch3-hotfix3-06-09-2025


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

Activity Stream

 PRB1893483

</td><td>

No activity displays in UI16 when a blank journal event is added to the Activity Stream

</td><td>

After upgrading to Yokohama, some records display 'No Activity' on the platform view. A null pointer exception displays.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1898714

</td><td>

Connection becomes vulnerable to sharing when it is marked for recycle

</td><td>

When a connection is marked for recycle, it is returned to the pool and can be picked up for allocation, in which it will be marked as 'Assigned'. The connection is checked for recycling and a new physical connection is established. Glide marks the connection as 'Available', which allows it to serve other requesters in the pool, causing connection sharing.

</td><td>

1.  Get a connection from the pool.
2.  Mark it for recycle by calling pool.setConnectionNeedsRecycle\(connectionID\).
3.  Launch the threads attempting to get a connection from the pool.
4.  Check the IDs of the connections.

 Notice that none of the connections are equal to the ID of the original connection, and if there is a connection with the same ID, sharing occurs.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 3 Hotfix 2](yokohama-patch-3-hf-2.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

