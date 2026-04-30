---
title: Xanadu Patch 4b Hotfix 2
description: The Xanadu Patch 4b Hotfix 2 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 4b Hotfix 2

The Xanadu Patch 4b Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 03-04-2025\_0721

    Build tag: glide-xanadu-07-02-2024\_\_patch4b-hotfix2-02-27-2025


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

AI Search

 PRB1836358

 [KB1790348](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1790348)

</td><td>

A race condition causes an incorrect deleteMultiple\(\) query to be generated on the v\_search\_genius\_result and sys\_variable\_value tables

</td><td>

When the AI Search Genius Result is requested and processed in a multi-threaded, high-concurrency environment, such as when multiple users simultaneously perform search functions on a portal or Virtual Agent \(VA\), a thread safety issue arises. This issue may cause an incorrect deleteMultiple\(\) query to be generated, potentially leading to the deletion of excessive records from the sys\_variable\_value table. This may result in unexpected outcomes for various components including the Integration Hub, Service Catalog items, and workflows due to the absence of these critical records.

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 4b Hotfix 1](xanadu-patch-4b-hf-1-PO.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

