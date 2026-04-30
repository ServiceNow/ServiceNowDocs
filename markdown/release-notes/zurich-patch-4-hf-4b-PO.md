---
title: Zurich Patch 4 Hotfix 4b
description: The Zurich Patch 4 Hotfix 4b release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-11"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 4 Hotfix 4b

The Zurich Patch 4 Hotfix 4b release contains fixes to these problems.

-   **Build information:**

    Build date: 03-05-2026\_1840

    Build tag: glide-zurich-07-01-2025\_\_patch4-hotfix4b-03-03-2026


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

Inbound API Integration Usage Framework

 PRB1997896

</td><td>

HttpServletRequest is recycled during long transactions, which causes unhandled exceptions in HttpRequest AttributeAccessor

</td><td>

Long-running SOAP transactions, including ODBC queries, can fail to complete on Zurich instances due to an unhandled error during telemetry collection.

</td><td>

Scenario 1:

 Attempt to query large datasets using ODBC.

 Scenario 2:

 To reproduce using only SOAP, increase the max limit and query 30k+ records in a single request.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 4 Hotfix 3b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2774148)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

