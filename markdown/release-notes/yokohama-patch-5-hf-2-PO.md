---
title: Yokohama Patch 5 Hotfix 2
description: The Yokohama Patch 5 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-15"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 5 Hotfix 2

The Yokohama Patch 5 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 07-10-2025\_1005

    Build tag: glide-yokohama-12-18-2024\_\_patch5-hotfix2-07-07-2025


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

Virtual Agent Web Client

 PRB1904063

</td><td>

Typing too fast in an NLU-based text choice picker for a lot of rows prevents upgrades

</td><td>

 

</td><td>

1.  Create a topic with a Dynamic choice picker in NLU.
2.  Ensure that the selected records have a lot of rows \(10K+\).
3.  Type fast in the text choice picker.

 Expected behavior: It should update the filtered items in the list.

 Actual behavior: The results never update due to 423 errors in the backend responses.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 5 Hotfix 1](yokohama-patch-5-hf-1-PO.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

