---
title: Yokohama Patch 8 Hotfix 3
description: The Yokohama Patch 8 Hotfix 3 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-12-08"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 8 Hotfix 3

The Yokohama Patch 8 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 12-04-2025\_1501

    Build tag: glide-yokohama-12-18-2024\_\_patch8-hotfix3-12-02-2025


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

Virtual Agent

 PRB1960129

</td><td>

Conversation abruptly ends after a cold start conversation with pre-chat survey enabled

</td><td>

Conversation abruptly ends after a cold start conversation with pre-chat survey enabled

</td><td>

1.  Enable pre-chat survey.
2.  Navigate to Teams.
3.  Type 'what is spam'.
4.  Complete the pre-chat survey.

 Expected behavior: The user should get a response related to the query from step 3.

 Actual behavior: The conversation ends after the survey is complete.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1963494

</td><td>

The synthesized response is not displayed completely

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to **/esc portal**.
3.  Perform multiple searches.

 Notice that the final response is displayed incompletely on VA web client.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 8 Hotfix 2](yokohama-patch-8-hf-2-PO.md)
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

