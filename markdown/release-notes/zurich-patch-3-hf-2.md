---
title: Zurich Patch 3 Hotfix 2
description: The Zurich Patch 3 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-18"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 3 Hotfix 2

The Zurich Patch 3 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-13-2025\_2045

    Build tag: glide-zurich-07-01-2025\_\_patch3-hotfix2-11-10-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

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

Configuration Management Database \(CMDB\)

 PRB1949356

</td><td>

Exact count match check results in an incorrect duplicate task creation

</td><td>

After upgrading to Zurich, de-duplication \(dedupe\) tasks are created incorrectly under certain scenarios. As a result, a large number of records are created in the duplicate\_audit\_result table, causing significant database growth. Instead of updating existing entries, new records are inserted during each subsequent run. In one scenario, the de-duplication tasks are created when they were previously working. In another scenario, users with many hosts that contain cmdb\_serial\_number records with the same serial\_number and serial\_number\_type notice that the number of duplicate\_audit\_result can grow to be tens of millions daily.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 3 Hotfix 1](zurich-patch-3-hf-1-PO.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

