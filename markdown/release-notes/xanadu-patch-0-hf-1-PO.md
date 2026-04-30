---
title: Xanadu EA Hotfix 1
description: The Xanadu EA Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-29"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu EA Hotfix 1

The Xanadu EA Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 08-27-2024\_1527

    Build tag: glide-xanadu-07-02-2024\_\_patch0-hotfix1-08-26-2024


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

 PRB1797451

</td><td>

The textAreaRef doesn't get instantiated correctly on hook-insert, so the 'Enter' key and **Send** button in the input area don't work

</td><td>

The issue is intermittent.

</td><td>

1.  Create a chat as a requester.
2.  As an agent, before the entire chat renders, select the input text area.
3.  Type something quickly and hit the 'Enter' key.

 Expected behavior: Hitting the 'Enter' key or selecting the **Send** button sends the messages.

 Actual behavior: Hitting the 'Enter' key creates new lines and selecting the **Send** button does nothing.

</td></tr><tr><td>

Agent Chat

 PRB1788201

</td><td>

Resolve copy-paste and debounce issues for chat input texta area in Agent Chat and sidebar

</td><td>

There are two issues. The **Send** button enables after a 250s delay. On sending a message which is typed extremely fast, the message is cut off.

</td><td>

1.  Initiate an agent chat.
2.  Type some text in the text area.

</td></tr><tr><td>

Horizon Component Library

 PRB1782771

</td><td>

Copy-paste isn't working as expected in the chat text area

</td><td>

This is reproducible both in Agent Chat and sidebar.

</td><td>

1.  Create a sidebar discussion or start a live agent conversation.
2.  Send a message: 'abcd'.
3.  Try to copy and paste an incident number into the chat text area.

 Expected behavior: Copied text should be pasted in the text area.

 Actual behavior: Pasted text is replaced by the last chat message.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

