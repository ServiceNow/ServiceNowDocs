---
title: Zurich Patch 10 Hotfix 4
description: The Zurich Patch 10 Hotfix 4 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-10-hf-4-PO.html
release: zurich
topic_type: reference
last_updated: "2026-07-10"
reading_time_minutes: 3
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 10 Hotfix 4

The Zurich Patch 10 Hotfix 4 release contains fixes to these problems.

-   **Build information:**

    Build date: 07-08-2026\_2020

    Build tag: glide-zurich-07-01-2025\_\_patch10-hotfix4-07-06-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

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

 PRB2050363

</td><td>

Incorrect and inconsistent heading hierarchy in ServiceNow flow

</td><td>

Users who rely on screen readers to navigate via headings are unable to get an overview of the 'Inbox' section. The lack of a clear hierarchy makes the content feel disconnected from the rest of the page, leading to confusion and increased cognitive load when trying to locate specific information.

</td><td>

1.  Open the SOW home page.
2.  Navigate to the 'Inbox' section using the tab key.
3.  Enable VoiceOver on macOS and use the rotor or heading shortcut to navigate.

Observe that it only identifies H4 and H5.

4.  Enable ChromeVox on ChromeOS and try to navigate by heading using the 'H' key.

 Observe that ChromeVox fails to identify any headings in this section.

</td></tr><tr><td>

Now Assist in Virtual Agent

 PRB2033795

</td><td>

Granular feedback options aren't getting translated

</td><td>

 

</td><td>

1.  Switch to a different language.
2.  Try to add granular feedback.

 Observe that translation doesn't work.

</td></tr><tr><td>

Virtual Agent

 PRB2041409

</td><td>

The vaContext object isn't available in the **Applicability** field of the Virtual Agent topic

</td><td>

An error occurs in the logs and the topic is not present, even though it should be conditionally available for the table.

</td><td>

1.  Log in to the instance.
2.  Open a record from the table 'x\_snc\_pm\_product\_feature'.
3.  Create a new chat in Now Assist for Request \(NASS\).
4.  Confirm that the topic 'Generate epics from capability', which should be conditionally available for this table, is not present.

 Notice the error in the logs, 'Script evaluation error at \[topic\_Generate epics from capability\_applicability\] ReferenceError: 'vaContext' is not defined. \(sys\_cs\_topic. 6db146b993f6f610 b2f9f60f2603d678; line 9\)'.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2022914

</td><td>

A model is not displayed to the guest user informing them of the timeout or 403 failure

</td><td>

The logs display 'sync' calls failing with a 403, but a 'Session expire' message or any other timeout message is not displayed to the user. This results in Virtual Agent getting stuck.

</td><td>

1.  Open a Zurich instance.
2.  Attempt to access Virtual Agent web client as guest user.
3.  Leave the chat open.

 Notice that after some time of inactivity, the logs display 'sync' calls failing with a 403, but a 'Session expire' message or any other timeout message is not displayed to the user. This results in Virtual Agent getting stuck.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2032099

</td><td>

New chat contains messages from the old chat

</td><td>

If the user is on a chat and selects the **+** button, it starts a new chat and shows the content of the previous chat as well.

</td><td>

1.  Start a new chat from NAVA.
2.  Transfer to a live agent.
3.  When the chat ends, immediately select the **+** button.

 Observe that the new chat shows messages from the previous closed chat.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 10 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3135835)
-   [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)

