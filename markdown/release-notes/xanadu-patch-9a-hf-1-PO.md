---
title: Xanadu Patch 9a Hotfix 1
description: The Xanadu Patch 9a Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-08-05"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 9a Hotfix 1

The Xanadu Patch 9a Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 08-03-2025\_1126

    Build tag: glide-xanadu-07-02-2024\_\_patch9a-hotfix1-07-27-2025


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

Activity Stream

 PRB1743672

</td><td>

Worknotes using Carriage Return aren't displaying in HR Agent Workspace when using edge encryption

</td><td>

 

</td><td>

1.  Enable Edge Encryption in the HR Workspace.
2.  Open the HR Workspace using an encrypted URL.
3.  Post a Worknote on a HR Case that uses a Carriage Return.

 Notice that the Worknote isn't visible in the Activity Log.

</td></tr><tr><td>

Declarative Actions

 PRB1839321

</td><td>

**Customize flow** on the 'Order' line item loads a blank screen for Order Agent/Order Admin users

</td><td>

When selecting the **Customize flow** action on a newly created 'Order' line item for a given Order, the page fails to load.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1908169

 [KB2252998](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2252998)

</td><td>

An exact match for an experience with an invalid routeConfigId doesn't navigate

</td><td>

A new issue was found which results in Zing search results aren't opening properly within a workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Assist Panel

 PRB1909094

</td><td>

The **Show more** button isn't visible on Now Assist for Request \(NASS\) for Safari browsers

</td><td>

When using the Now Assist Panel \(NAP\), Now Assist for Virtual Agent \(NAVA\), or Now Assist for Request \(NASS\) on Safari, the **Show more** button isn't visible after truncation, so the user is unable to see the full message. This prevents users from accessing the complete content of responses.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1849654

 [KB1940828](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1940828)

</td><td>

Synthesized output is not captured in an interaction transcript

</td><td>

In Virtual Agent, the transcripts captured on the interaction don't log the synthesized output.

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 9a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2290356)
-   [Xanadu Patch 8](xanadu-patch-8.md)
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

