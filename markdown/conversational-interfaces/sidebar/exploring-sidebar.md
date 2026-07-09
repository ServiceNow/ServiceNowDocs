---
title: Exploring Sidebar
description: Using Sidebar, agents can have real-time collaboration with others as a standalone conversation or based around a Workspace record. These Sidebar discussions facilitate the exchange of information and knowledge to help resolve issues faster and with higher-quality outcomes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/sidebar/exploring-sidebar.html
release: zurich
product: Sidebar
classification: sidebar
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
keywords: [Virtual Agent, sidebar, workspace, discussion panel, activity stream]
breadcrumb: [Sidebar, Conversational Interfaces]
---

# Exploring Sidebar

Using Sidebar, agents can have real-time collaboration with others as a standalone conversation or based around a Workspace record. These Sidebar discussions facilitate the exchange of information and knowledge to help resolve issues faster and with higher-quality outcomes.

## Sidebar overview

An agent can initiate a Sidebar discussion as a standalone conversation or from a Workspace record. Agents enter preliminary information and context and adding subject matter experts. For Sidebar discussions created from a Workspace record, the agent can create multiple discussions for a record.

## Sidebar workspaces

Sidebar is supported in these workspaces:

-   Customer Service Management \(CSM\) Configurable Workspace.
-   CSM Manager Workspace
-   Human Resources \(HR\) Agent Workspace
-   IT Service Management \(ITSM\) Manager Workspace
-   Security Incident Response Workspace
-   Vendor Management Workspace

For information on adding the **Discuss** button to a supported workspace, see [Adding the Discuss button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/add-sidebar-button.md).

For information on adding the **Discuss** button to any workspace not listed \(such as the Service Operation Workspace\), see [KB article KB1213249](https://support.servicenow.com/kb_view.do?sysparm_article=KB1213249).

## Sidebar components

-   **Sidebar discussion panel**

    When you select the Sidebar discussion icon \[Omitted image "sidebar-chat-icon.png"\] Alt text: Sidebar discussion icon., the Sidebar discussion panel appears:

    \[Omitted image "sidebar-dialog-2.png"\] Alt text: Sidebar discussion panel.

    The Sidebar discussion panel includes:

<table id="table_z1h_4wq_d5b"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - \[Omitted image "sidebar-chat-icon.png"\] Alt text: Search icon, shown as a magnifying glass.

</td><td>

This is the magnifying glass. Display Sidebar discussions dialog. If a number in a blue square appears, the number indicates the number of Sidebar discussions that are currently active.

</td></tr><tr><td>

2- \[Omitted image "sidebar-search-icon.png"\] Alt text: Search icon, shown as a magnifying glass.

</td><td>

Search within the Sidebar discussions. When you select the Search icon, the **Search** field appears and you can enter the text you want to locate. The search results display below the search field and are grouped by user message then file name. Select **Cancel** to clear the search field and return to the Sidebar discussion. You can filter the search results by discussions, messages, and attachments and sort by most relevant or date.

 To use the Search KB quick action, enable AI Search. For more information, see AI Search and [AI Search Availability \[KB0867751\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867751).

</td></tr><tr><td>

3 - \[Omitted image "sidebar-pushpin-icon.png"\] Alt text: Pushpin icon

</td><td>

Permanently pin the menu to the side of the screen.

</td></tr><tr><td>

4 - \[Omitted image "sidebar-all-unread-heading.png"\] Alt text: Additional options screenshot.

</td><td>

Select what types of discussions that you want to view:-   All - all discussions.
-   Unread - all unread discussions.
-   This record - all discussions related to the record that's currently open in the background. The most recent information displays and is updated when a new message is received, there’s an unread message, or a new discussion is created for the record. You can also create discussions for the record by selecting **New discussion**.
-   Mentions - discussions that mention you with @yourusername.
-   Favorites - discussions that you marked as favorites.


</td></tr><tr><td>

5 - \[Omitted image "sidebar-star-icon.png"\] Alt text: Star icon.

</td><td>

Marks the Sidebar discussion as a favorite. Discussions that have been marked as favorites display under the **Favorites** tab. You can undo a discussion as a favorite by selecting the star icon again.

</td></tr><tr><td>

6 - \[Omitted image "more-options-icon.png"\] Alt text: More options icon, shown as three vertical dots.

</td><td>

Displays options for the discussion:-   Dismiss discussion - close the discussion dialog \(but don't exit the discussion\).
-   Leave discussion - exit the discussion.


</td></tr></tbody>
</table>-   **Docked chat windows**

    You can access multiple Sidebar discussions at the same time using the docked windows feature. Docked chat windows include these features:

    \[Omitted image "sidebar-docked-window.png"\] Alt text: Sidebar docked window, with header, avatar and presence, more actions icon, and text input box highlighted.

<table id="table_s2s_zgs_d5b"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - \[Omitted image "sidebar-star-icon.png"\] Alt text: Star icon.

</td><td>

Marks the Sidebar discussion as a favorite. Discussions that have been marked as favorites display under the **Favorites** tab. You can undo a discussion as a favorite by selecting the star icon again.

</td></tr><tr><td>

2 - \[Omitted image "sidebar-i-icon.png"\] Alt text: Information icon, displayed as a circled lowercase i.\[Omitted image "sidebar-participant-submenu.png"\] Alt text: Participants submenu on the Discussion info.

</td><td>

Opens the Discussion info panel that includes the About submenu, Participants submenu, and **Leave discussion** button. On the About submenu, you can view information about the discussion. On the Participants submenu, you can add and remove participants. If you want to exist the discussion, select **Leave discussion**. For a standalone discussion, select the drop-down arrow next to the About submenu and select the **Link to record** to link the discussion to a record.

</td></tr><tr><td>

3 - \[Omitted image "sidebar-double-arrow-icon.png"\] Alt text: Collapse icon, displayed as two arrows facing each other points-first.

</td><td>

Collapses the discussion so it displays only as a tab at the bottom of the screen.

</td></tr><tr><td>

4 - \[Omitted image "sidebar-x-icon.png"\] Alt text: Close dialog icon, displayed as a capital X

</td><td>

Closes the window.

</td></tr></tbody>
</table><table id="table_q11_jjm_g5b"><thead><tr><th>

User avatar and presence

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "sidebar-user-presence-example.png"\] Alt text: user icon

</td><td>

Displays the user's avatar and presence \(online status\). The dot indicates the user's presence depending on whether they’re logged in to the platform: -   Green dot - user is logged in.
-   No dot - user isn’t logged in.
-   Orange dot - user recently logged out.
If Sidebar and Microsoft Teams are integrated, Microsoft Teams users are differentiated from Sidebar users with a Microsoft Teams \[Omitted image "teams-icon.png"\] Alt text: Microsoft Teams icon icon. If Sidebar and Slack are integrated, Slack users are differentiated from Sidebar users with a Slack icon \( \[Omitted image "slack-icon.png"\] Alt text: Slack icon.\).

</td></tr></tbody>
</table><table id="table_i3d_hzq_1yb"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "more-actions-icon.png"\] Alt text: More actions icon, displayed as three vertical dots.

</td><td>

Display additional actions for this message including:

-   Post to activity stream
-   Remove from activity stream
-   Edit message
-   Delete message


</td></tr></tbody>
</table><table id="table_dyb_drc_f5b"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

A - \[Omitted image "sidebar-lightning-bolt-icon.png"\] Alt text: Quick actions icon, displayed as a lightning bolt.

</td><td>

Access base system or custom quick actions.

 The agent can start a KB article search by selecting the quick actions icon and then entering `search-kb`. The agent is prompted to search for the relevant KB article. Based on the search and the term that the agent enters, the agent is able to view the KB articles that match the search term. The agent can then select the KB article and include it in the discussion. The KB article is displayed as a record card in the Sidebar discussion. The KB article search is available with the base system.

 You can summarize a discussion by entering the `/summarize` quick action.

</td></tr><tr><td>

B - \[Omitted image "sidebar-smiley-face-icon.png"\] Alt text: Smiley face icon signaling ability to add an emoji.

</td><td>

Display the emoji menu so you can add emojis to the discussion.

</td></tr><tr><td>

C - \[Omitted image "sidebar-paper-clip-icon.png"\] Alt text: Attachment icon, displayed as a paperclip.

</td><td>

Add attachments to the current discussion so they can be shared with others in the discussion. You can drag files and select the send arrow icon or you can use the attachment icon.

</td></tr><tr><td>

D - \[Omitted image "sidebar-send-arrow-icon.png"\] Alt text: Side arrowhead icon used to send the message.

</td><td>

Send the message.

</td></tr></tbody>
</table>    If you minimize a docked window, it appears as a tab in the overflow menu at the bottom of the screen. Hovering over a minimized docked window shows the record number and chat title to help identify the content. You can select any tab to access that discussion again. The overflow menu can hold up to 25 docked windows and this limit is configurable. If there are more docked windows than can be displayed as tabs in the overflow menu, a tab with a number indicates how many extra docked windows aren't displayed.


## Threaded replies

Use threaded replies to keep related messages grouped within Sidebar discussions. When you respond using a threaded reply, your message is added to the specific message you're replying to, rather than the main discussion.

To start a threaded reply to a message:

1.  Select reply arrow \(\[Omitted image "threaded-reply-arrow.png"\] Alt text: Reply arrow icon.\) next to the message you want to reply to:

    \[Omitted image "sidebar-threaded-1.png"\] Alt text: Start of a threaded reply in a Sidebar discussion.

2.  The panel displays "Thread" followed by the discussion subject. Type your message in the text input box:

    \[Omitted image "sidebar-threaded-2.png"\] Alt text: Typing the text of a threaded reply.

3.  Select the send arrow \(\[Omitted image "threaded-send-arrow.png"\] Alt text: Send arrow icon.\).
4.  Your messages appear under the parent message:

    \[Omitted image "sidebar-threaded-3.png"\] Alt text: Typing the text of a threaded reply.

5.  If threaded reply has multiple messages, you can expand them to view all of the messages or you can collapse them and the number of messages displays instead.

    \[Omitted image "sidebar-threaded-4.png"\] Alt text: Multiple messages collapsed in a threaded reply.


**Note:** If you delete a message with threaded replies, a warning appears letting you know that all its threaded replies will also be deleted.

## Activity stream and Sidebar

To enable agents to post Sidebar discussions to the activity stream, you must integrate Sidebar with the activity stream. For instructions on integrating Sidebar with the activity stream, see [Integrating Sidebar and activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/integrate-sidebar-activity-stream.md). For information on using Sidebar with the activity stream, see [Activity stream in Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/activity-stream-sidebar.md).

## Installing and configuring Sidebar

The Sidebar configuration settings are available via the Sidebar tab under **Conversational Interfaces** &gt; **Settings**. For instructions, see [Installing Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/install-sidebar.md). After Sidebar is installed, see [Configuring Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/configure-sidebar.md) for instructions on configuring the admin settings.

## Using Sidebar

For information on how to use Sidebar, see [Using Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/using-sidebar.md) for more information.

Key Sidebar features include:

-   Custom discussion buttons
-   Core UI forms with Sidebar
-   Sidebar unread conversation badge count
-   Docked chat window
-   Favorite discussions
-   Discussion information panel
-   Discussion participant suggestions
-   Quick actions
-   Integration with activity stream
-   Integration with AI search
-   Drag-and-drop file sharing
-   Emojis
-   Mentioning a user with @

## Using Sidebar and Microsoft Teams

After Sidebar and Microsoft Teams are integrated, users of both applications can collaborate with each other. For more information on integrating Sidebar with Microsoft Teams, see [Sidebar and Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/sidebar-teams-overview.md).

## Core UI

You can create Sidebar discussions on interaction records from Next Experience Core UI.

## Domain Separation

For information about domain separation in Sidebar, see [Domain separation and Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/sidebar-domain-separation.md).

## More information

To learn more, see the [Now learning course on Sidebar.](https://learning.servicenow.com/lxp?course_id=f1a907258736919cd3be437e0ebb3523&id=learning_course_prev)

