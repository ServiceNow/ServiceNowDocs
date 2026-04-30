---
title: Yokohama Patch 2 Hotfix 3
description: The Yokohama Patch 2 Hotfix 3 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-06-05"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 2 Hotfix 3

The Yokohama Patch 2 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 06-02-2025\_1015

    Build tag: glide-yokohama-12-18-2024\_\_patch2-hotfix3-05-29-2025


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

Activity Stream Compose Component

 PRB1897434

</td><td>

The 'Email' tab in the Activity Stream in the CSM Configurable Workspace doesn't resize when the text is larger than the vertical limit

</td><td>

This issue is found in Yokohama, but works as expected in Xanadu.

</td><td>

1.  Hop into a Yokohama instance as an admin user.
2.  Navigate to the **Activity Stream** &gt; **More** &gt; **Email**.
3.  Select **Return past vertical limit**.

 Expected behavior: The email text box auto-resizes vertically.

 Actual behavior: The email text box doesn't auto-resize.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 2 Hotfix 2](yokohama-patch-2-hf-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

