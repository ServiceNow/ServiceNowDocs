---
title: Yokohama Patch 5 Hotfix 3
description: The Yokohama Patch 5 Hotfix 3 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-08-05"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 5 Hotfix 3

The Yokohama Patch 5 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 07-31-2025\_0932

    Build tag: glide-yokohama-12-18-2024\_\_patch5-hotfix3-07-28-2025


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

Metric Intelligence \(Family\)

 PRB1921270

</td><td>

Ignite does not support IPv6

</td><td>

Fixing the implementation to support IPv6.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1920054

</td><td>

Condition with transitions are failing when viewing the 'Schedule task' results

</td><td>

This issue occurs when upgrading from Xanadu to Yokohama.

</td><td>

1.  Create Xanadu instance.
2.  Set up pre-upgrade data with all necessary configurations.
3.  Apply conditions \(for example: Active as 'false'\).
4.  Apply the transitions 'Process Start' \(for example: Process Start - Stop \(Incident\)\).
5.  Notice that eventually followed by Process Start - Stop \(Incident\) is Process End, with the constraints 'from condition 1 to condition'.
6.  Ensure that the min duration, max duration and relation constraint type is 'None'.
7.  Upgrade to Yokohama.
8.  Open the model which has condition with transition combination above.
9.  Select **View results** from the Scheduled task.

 Notice that an error occurred, 'Exception encountered processing path: /GlidePromin\_Query/scheduleModel - Constraint is empty. Please add either Field constraint or Duration constraint.'

</td></tr><tr><td>

Software Asset Management

 PRB1913658

 [KB2290496](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2290496)

</td><td>

On an upgrade to Yokohama, new entitlements may get created from entitlement import errors

</td><td>

Users may observe the issue as duplicate entitlements found after an upgrade to Yokohama, or, after an upgrade to Yokohama, a number of entitlements were added that were created by 'system'.

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 5 Hotfix 2](yokohama-patch-5-hf-2-PO.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

