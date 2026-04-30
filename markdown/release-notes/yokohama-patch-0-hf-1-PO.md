---
title: Yokohama EA Hotfix 1
description: The Yokohama EA Hotfix 1 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-02-20"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama EA Hotfix 1

The Yokohama EA Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 02-17-2025\_2042

    Build tag: glide-yokohama-12-18-2024\_\_patch0-hotfix1-02-11-2025


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

AI Search

 PRB1847092

</td><td>

A part of the query on sys \_generative \_ai \_config has been ignored because of insufficient access for 'query\_match operation on sys\_generative \_ai\_config definition

</td><td>

Results in warning message pop-ups.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1854242

</td><td>

Turn off data snapshots on instances that are Raptor standard

</td><td>

From the 'pa\_indicators' list view and 'indicator' form view, users shouldn't see data snapshots. MLB related buttons shouldn't be visible to users. Users shouldn't be able to modify them via the MLB system property.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

