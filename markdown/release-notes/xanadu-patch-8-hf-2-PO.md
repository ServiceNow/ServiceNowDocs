---
title: Xanadu Patch 8 Hotfix 2
description: The Xanadu Patch 8 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-04-30"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 8 Hotfix 2

The Xanadu Patch 8 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 04-23-2025\_2116

    Build tag: glide-xanadu-07-02-2024\_\_patch8-hotfix2-04-23-2025


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

Mobile Platform

 PRB1883251

</td><td>

Block Mobile Attachment Sharing property for Mobile doesn't support exemption based on user roles

</td><td>

Changing the property glide.sg.block\_mobile\_attachment\_sharing from 'false' to 'true' should exempt some users based on their roles for the security property.

</td><td>

1.  Navigate to **sys\_properties.list**.
2.  Change the property glide.sg.block\_mobile\_attachment\_sharing from 'false' to 'true'.

 Notice that this applies to all users, when only some users require the ability to download or view attachments on Mobile based on their role.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 8 Hotfix 1](xanadu-patch-8-hf-1-PO.md)
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

