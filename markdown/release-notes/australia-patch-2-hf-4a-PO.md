---
title: Australia Patch 2 Hotfix 4a
description: The Australia Patch 2 Hotfix 4a release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/australia-patch-2-hf-4a-PO.html
release: australia
topic_type: reference
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 2 Hotfix 4a

The Australia Patch 2 Hotfix 4a release contains fixes to these problems.

-   **Build information:**

    Build date: 07-09-2026\_1946

    Build tag: glide-australia-02-11-2026\_\_patch2-hotfix4a-07-07-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

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

 PRB2030144

</td><td>

When a work item is in the queue but not yet accepted, the user can't update string fields on the open record

</td><td>

In the workspace, when a work item is in the queue but not yet accepted, the user is unable to update string fields on the open record. With these two circumstances satisfied, a focus-stealing issue occurs, where the blinking cursor is removed after a moment.

</td><td>

1.  Open a base instance.
2.  Impersonate an agent.
3.  Navigate to Service Operations Workspace.
4.  Open any editable record from one of the Lists \(for example, RITM, INC, etc.\).
5.  Select **Inbox**.
6.  Set the agent to Available.
7.  Route a chat to this agent from an incognito window.
8.  While the new chat is in the inbox and the form is visible, attempt to type something in any string field on the form.

 Observe that the blinking cursor disappears.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-security-notables.md)
-   [All other Australia fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/available-versions.md)

