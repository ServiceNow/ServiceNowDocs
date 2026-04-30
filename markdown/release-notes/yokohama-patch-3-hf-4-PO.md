---
title: Yokohama Patch 3 Hotfix 4
description: The Yokohama Patch 3 Hotfix 4 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-01"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 3 Hotfix 4

The Yokohama Patch 3 Hotfix 4 release contains fixes to these problems.

-   **Build information:**

    Build date: 2025\_06-26-2025\_2019

    Build tag: glide-yokohama-12-18-2024\_\_patch3-hotfix4-06-25


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

 PRB1881938

</td><td>

Boolean choice pickers aren't translated to the user's language in Dynamic Window

</td><td>

 

</td><td>

1.  Install a language.
2.  Switch the profile language to that language.
3.  Ensure that Dynamic Translation and Native Translation are turned on in Now Assist.
4.  Create a topic with the user input using the input selector.
5.  Navigate to Dynamic Window.
6.  Run the topic from step 4 until completion.

 Expected behavior: Boolean topic choice pickers are translated to the user's selected language \(Yes/No input\).

 Actual behavior: Boolean topic choice pickers are still in English \(Yes/No input\).

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 3 Hotfix 3](yokohama-patch-3-hf-3-PO.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

