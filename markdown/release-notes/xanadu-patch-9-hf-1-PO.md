---
title: Xanadu Patch 9 Hotfix 1
description: The Xanadu Patch 9 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-06-18"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 9 Hotfix 1

The Xanadu Patch 9 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 06-13-2025\_1945

    Build tag: glide-xanadu-07-02-2024\_\_patch9-hotfix1-06-13-2025


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

Agent Chat

 PRB1900981

</td><td>

Inbox audio is delayed when the 'Workspace' tab is inactive or out of focus before receiving the first work item

</td><td>

 

</td><td>

1.  Log in as an agent.
2.  Navigate to Workspace.
3.  Mark an agent as online.
4.  Navigate to another browser tab \(inactive tab\) or anywhere else on the machine except the workspace tab.
5.  Log in as requestor.
6.  Start a chat.
7.  Wait for some time.
8.  Switch back to Agent Workspace.

 Expected behavior: Audio should be heard as soon as the work item is assigned.

 Actual behavior: When the work item assigned, audio isn't heard. Audio is heard only after switching back to the workspace.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 9](xanadu-patch-9.md)
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

