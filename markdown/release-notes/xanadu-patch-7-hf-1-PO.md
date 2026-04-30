---
title: Xanadu Patch 7 Hotfix 1
description: The Xanadu Patch 7 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-04-04"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 7 Hotfix 1

The Xanadu Patch 7 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 04-02-2025\_1342

    Build tag: glide-xanadu-07-02-2024\_\_patch7-hotfix1-04-01-2025


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

MID Server

 PRB1870465

 [KB2022624](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2022624)

</td><td>

ECCSender does not use the correct character set when reading XML queue files

</td><td>

ECCSender is using the default file encoding/character set when reading XML queue files from disk. This results in incorrect characters in the response for some special characters. ECCSender should use UTF-8 when reading these files, as XML queue files on disk are always UTF-8.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Integration Hub Remote Process Sync

 PRB1874002

</td><td>

Remote Process Sync \(RPS\) is triggered by changes from non-captured fields

</td><td>

RPS captures changes to a record when any changes are made to the fields selected by the user as part of the CDC Definition \(change data capture\). Even though changes are being made to fields that are not part of the CDC Definition, RPS still captures these changes.

</td><td>

1.  Set up RPS.
2.  Create a record that syncs.
3.  Modify a field on that record that isn't part of the CDC Definition

 Observe that this creates an update record on cdc\_queue\_ih, which should not be created.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 7](xanadu-patch-7.md)
-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

