---
title: Yokohama Patch 12 Hotfix 2
description: The Yokohama Patch 12 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-02-25"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 12 Hotfix 2

The Yokohama Patch 12 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 02-22-2026\_2045

    Build tag: glide-yokohama-12-18-2024\_\_patch12-hotfix2-02-13-2026


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

AI Search \(Glide\)

 PRB1971388

</td><td>

IngestableDocument. getObjectSize isn't counting fEmbeddedDocuments

</td><td>

Indexing the document/table causes out of memory errors.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1990134

</td><td>

If all KBBs from one doc are removed from KB late binding, the post process stops and all following docs are returned

</td><td>

If ACL filtering removes all the embedded documents from a knowledge base article \(and there's no embedded match\), the code stops processing all subsequent documents.

</td><td>

1.  Ensure the KB is using ACL instead of UC 'glide.knowman.search .apply\_acls'=true.
2.  Create two KB articles:
    -   For KB1, the user has ACL access, but cannot access any of the KBB.
    -   For KB2, the user has no ACL access.
3.  As the user, search a query that matches KB1. \(Or use result improvement rule to boost KB1.\)

 Expected behavior: KB2 is not shown because the user has no ACL access.

 Actual behavior: KB2 is shown.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 12 Hotfix 1](yokohama-patch-12-hf-1.md)
-   [Yokohama Patch 11](yokohama-patch-11.md)
-   [Yokohama Patch 10](yokohama-patch-10.md)
-   [Yokohama Patch 9](yokohama-patch-9.md)
-   [Yokohama Patch 8](yokohama-patch-8.md)
-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

