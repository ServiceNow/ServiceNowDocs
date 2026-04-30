---
title: Zurich Patch 4 Hotfix 5
description: The Zurich Patch 4 Hotfix 5 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-01-29"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 4 Hotfix 5

The Zurich Patch 4 Hotfix 5 release contains fixes to these problems.

-   **Build information:**

    Build date: 01-26-2026\_0834

    Build tag: glide-zurich-07-01-2025\_\_patch4-hotfix5-01-23-2026


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

Identification and Reconciliation API

 PRB1972817

</td><td>

There's an NMA update exception

</td><td>

This results in various errors during the load test.

</td><td>

1.  Run OKR Mixed Load Test with CMDB Updates, Event Management, Discovery, and Order Management.
2.  Run 10M NMA Update using CISP.
3.  Check for errors during the load test.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 4 Hotfix 4](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2706229)
-   [Zurich Patch 4 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2695190)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

