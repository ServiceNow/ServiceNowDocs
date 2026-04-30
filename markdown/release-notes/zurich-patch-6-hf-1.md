---
title: Zurich Patch 6 Hotfix 1
description: The Zurich Patch 6 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-02-11"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 6 Hotfix 1

The Zurich Patch 6 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 02-09-2026\_1234

    Build tag: glide-zurich-07-01-2025\_\_patch6-hotfix1-02-05-2026


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

Application Manager

 PRB1986694

</td><td>

App Manager and My Company Applications incorrectly shows available updates after Update Checker

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CMDB Query Builder

 PRB1977703

 [KB2727703](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2727703)

</td><td>

Query Builder in V2 mode can cause memory issues due to a static variable

</td><td>

An internal variable which is declared as static keeps being appended and thus creates a large memory footprint. This would happen if one or more queries are executed enough times to bloat this variable.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1988503

 [KB2764725](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2764725)

</td><td>

Active subflow executions with clean parent flow executions are listed as 'Unreferenced Records' and are deleted by DMUnreferenced RecordCleaner

</td><td>

This issue was observed in Zurich. If a parent flow completes while an associated asynchronous subflow continues running, the completed parent flow context is cleaned up by the retention policy by routine system cleanup. As a result, the running subflow becomes unreferenced, and may be removed during routine system cleanup.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1935825

</td><td>

Skip\_schedule\_cleanup is not reset to false for subflows

</td><td>

The table cleaners need to be revised.

</td><td>

Open http://localhost:8080/ sys\_auto\_flush\_list.do? sysparm\_query=conditionsLIKEskip \_schedule\_cleanup &amp;sysparm\_view=.

 Observe that all the table cleaners use skip\_schedule\_cleanup. Skip\_schedule\_cleanup should be managed well.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 6](zurich-patch-6.md)
-   [Zurich Patch 5](zurich-patch-5.md)
-   [Zurich Patch 4](zurich-patch-4.md)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

