---
title: Yokohama Patch 2 Hotfix 2
description: The Yokohama Patch 2 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-21"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 2 Hotfix 2

The Yokohama Patch 2 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 04-16-2025\_1603

    Build tag: glide-yokohama-12-18-2024\_\_patch2-hotfix2-04-15-2025


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

Flow Engine

 PRB1874873

 [KB2042735](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2042735)

</td><td>

Deserialization issue occur to flows when upgrading from Washington DC to Yokohama

</td><td>

Flows containing the **Make a decision** logic don't resume and error out after upgrading to Yokohama. This is caused by a deserialization issue in Flow Engine V2, which prevents the flow from progressing.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1880998

</td><td>

Unable to deserialize **Make a decision** instruction after upgrading to Yokohama

</td><td>

When the flow is in a 'Waiting' state in the Washington DC release with Engine\_V2, the event opening the flow execution fails after upgrading to the Yokohama release.

</td><td>

1.  Create a flow with a **Make a decision** flow logic.
2.  Ensure the flow has a waiting scenario so that flow\_context goes to a 'Waiting' state.
3.  Execute the flow.
4.  Ensure the flow is in a 'Waiting' state in the Washington DC release with Engine\_V2.
5.  Upgrade the instance to Yokohama.
6.  Notice that the event opening the flow execution in **Operation view** fails, and resuming the flow by satisfying the waiting condition fails.

 Expected behavior: The flow should resume on Yokohama without any errors.

 Actual behavior: The flow errors out in Yokohama.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 2 Hotfix 1](yokohama-patch-2-hf-1-PO.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

