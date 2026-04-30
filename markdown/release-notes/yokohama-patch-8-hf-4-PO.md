---
title: Yokohama Patch 8 Hotfix 4
description: The Yokohama Patch 8 Hotfix 4 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-01-29"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 8 Hotfix 4

The Yokohama Patch 8 Hotfix 4 release contains fixes to these problems.

-   **Build information:**

    Build date: 01-25-2026\_1918

    Build tag: glide-yokohama-12-18-2024\_\_patch8-hotfix4-01-23-2026


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

Advanced Work Assignment

 PRB1982818

</td><td>

After removing a service channel, the current universal capacity of the agent isn't decreased

</td><td>

After removing a service channel from the 'Available' presence state, the universal capacity for the existing documents related to that channel shouldn't be considered.

</td><td>

1.  Create a service channel \('Chat-test'\).
2.  Add it to the 'Available' presence state in awa\_presence\_state.
3.  Create related queues and assignment eligibility pools.
4.  Create a universal capacity record for the agent \('Beth Anglin'\).
5.  Make the agent 'Available'.
6.  Create documents for that and let those be assigned to the agent.
7.  Observe that the current universal capacity of the agent is increased.
8.  Remove the service channel from the 'Available" presence state in awa\_presence\_state.

 Observe that the current universal capacity of the agent stays the same. In Xanadu and Zurich, the current universal capacity gets decreased.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 8 Hotfix 3](yokohama-patch-8-hf-3-PO.md)
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

