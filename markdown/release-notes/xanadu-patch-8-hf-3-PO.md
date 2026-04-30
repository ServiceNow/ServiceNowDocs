---
title: Xanadu Patch 8 Hotfix 3
description: The Xanadu Patch 8 Hotfix 3 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-05-08"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 8 Hotfix 3

The Xanadu Patch 8 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 05-05-2025\_2003

    Build tag: glide-xanadu-07-02-2024\_\_patch8-hotfix3-05-02-2025


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

 PRB1823459

</td><td>

AI Search indexing Topic Path Translation doesn't work for non system user preference language

</td><td>

Session users assigned as 'guest' with the sys\_user\_preference file 'name=user.language' and 'value=&lt;some\_non\_user \_session\_language&gt;' will have topic paths indexed in this language. The set language is not effective, which is the cause of incorrect translations.

</td><td>

1.  Ensure sys\_language has two active languages, **en** for English and **de** for Deutsch.
2.  Create an entry in the sys\_user\_preference table with the following values:
    -   system = true
    -   user = empty with language as 'de'
3.  Create the catalog item with translations for topic and topic path.

 Expected behavior: AI Search should index, and be able to search with the 'en' topic value.

 Actual behavior: AI Search indexes content with Deutsch translations for documents with both English and Deutsch languages, and the search for English will fail.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 8 Hotfix 2](xanadu-patch-8-hf-2-PO.md)
-   [Xanadu Patch 7](xanadu-patch-7.md)
-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

