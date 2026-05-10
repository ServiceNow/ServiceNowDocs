---
title: Exploring Sidebar
description: Using Sidebar, agents can have real-time collaboration with others as a standalone conversation or based around a Workspace record. These Sidebar discussions facilitate the exchange of information and knowledge to help resolve issues faster and with higher-quality outcomes.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: concept
last_updated: "2026-03-12"
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

For information on adding the **Discuss** button to a supported workspace, see [Adding the Discuss button](../task/add-sidebar-button.md).

For information on adding the **Discuss** button to any workspace not listed \(such as the Service Operation Workspace\), see [KB article KB1213249](https://support.servicenow.com/kb_view.do?sysparm_article=KB1213249).

## Sidebar components

-   **Sidebar discussion panel**

    When you select the Sidebar discussion icon ![Sidebar discussion icon.](../image/sidebar-chat-icon.png), the Sidebar discussion panel appears:

    ![Sidebar discussion panel.](../image/sidebar-dialog-2.png)

    The Sidebar discussion panel includes:

<table id="table_z1h_4wq_d5b"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - ![Search icon, shown as a magnifying glass.](../image/sidebar-chat-icon.png)

</td><td>

This is the magnifying glass. Display Sidebar discussions dialog. If a number in a blue square appears, the number indicates the number of Sidebar discussions that are currently active.

</td></tr><tr><td>

2- ![Search icon, shown as a magnifying glass.](../image/sidebar-search-icon.png)

</td><td>

Search within the Sidebar discussions. When you select the Search icon, the **Search** field appears and you can enter the text you want to locate. The search results display below the search field and are grouped by user message then file name. Select **Cancel** to clear the search field and return to the Sidebar discussion. You can filter the search results by discussions, messages, and attachments and sort by most relevant or date.

 To use the Search KB quick action, enable AI Search. For more information, see [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/overview-ais.md) and [AI Search Availability \[KB0867751\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867751).

</td></tr><tr><td>

3 - ![Pushpin icon](../image/sidebar-pushpin-icon.png)

</td><td>

Permanently pin the menu to the side of the screen.

</td></tr><tr><td>

4 - ![Additional options screenshot.](../image/sidebar-all-unread-heading.png)

</td><td>

Select what types of discussions that you want to view:-   All - all discussions.
-   Unread - all unread discussions.
-   This record - all discussions related to the record that's currently open in the background. The most recent information displays and is updated when a new message is received, there’s an unread message, or a new discussion is created for the record. You can also create discussions for the record by selecting **New discussion**.
-   Mentions - discussions that mention you with @yourusername.
-   Favorites - discussions that you marked as favorites.


</td></tr><tr><td>

5 - ![Star icon.](../image/sidebar-star-icon.png)

</td><td>

Marks the Sidebar discussion as a favorite. Discussions that have been marked as favorites display under the **Favorites** tab. You can undo a discussion as a favorite by selecting the star icon again.

</td></tr><tr><td>

6 - ![More options icon, shown as three vertical dots.](../image/more-options-icon.png)

</td><td>

Displays options for the discussion:-   Dismiss discussion - close the discussion dialog \(but don't exit the discussion\).
-   Leave discussion - exit the discussion.


</td></tr></tbody>
</table>-   **Docked chat windows**

    You can access multiple Sidebar discussions at the same time using the docked windows feature. Docked chat windows include these features:

    ![Sidebar docked window, with header, avatar and presence, more actions icon, and text input box highlighted.](../image/sidebar-docked-window.png)

<table id="table_s2s_zgs_d5b"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - ![Star icon.](../image/sidebar-star-icon.png)

</td><td>

Marks the Sidebar discussion as a favorite. Discussions that have been marked as favorites display under the **Favorites** tab. You can undo a discussion as a favorite by selecting the star icon again.

</td></tr><tr><td>

2 - ![Information icon, displayed as a circled lowercase i.](../image/sidebar-i-icon.png)![Participants submenu on the Discussion info.](../image/sidebar-participant-submenu.png "Participants submenu")

</td><td>

Opens the Discussion info panel that includes the About submenu, Participants submenu, and **Leave discussion** button. On the About submenu, you can view information about the discussion. On the Participants submenu, you can add and remove participants. If you want to exist the discussion, select **Leave discussion**. For a standalone discussion, select the drop-down arrow next to the About submenu and select the **Link to record** to link the discussion to a record.

</td></tr><tr><td>

3 - ![Collapse icon, displayed as two arrows facing each other points-first.](../image/sidebar-double-arrow-icon.png)

</td><td>

Collapses the discussion so it displays only as a tab at the bottom of the screen.

</td></tr><tr><td>

4 - ![Close dialog icon, displayed as a capital X](../image/sidebar-x-icon.png)

</td><td>

Closes the window.

</td></tr></tbody>
</table><table id="table_q11_jjm_g5b"><thead><tr><th>

User avatar and presence

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![user icon](../image/sidebar-user-presence-example.png)

</td><td>

Displays the user's avatar and presence \(online status\). The dot indicates the user's presence depending on whether they’re logged in to the platform: -   Green dot - user is logged in.
-   No dot - user isn’t logged in.
-   Orange dot - user recently logged out.
If Sidebar and Microsoft Teams are integrated, Microsoft Teams users are differentiated from Sidebar users with a Microsoft Teams ![Microsoft Teams icon](../image/teams-icon.png) icon. If Sidebar and Slack are integrated, Slack users are differentiated from Sidebar users with a Slack icon \( ![Slack icon.](../image/slack-icon.png)\).

</td></tr></tbody>
</table><table id="table_i3d_hzq_1yb"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![More actions icon, displayed as three vertical dots.](../image/more-actions-icon.png)

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

A - ![Quick actions icon, displayed as a lightning bolt.](../image/sidebar-lightning-bolt-icon.png)

</td><td>

Access base system or custom quick actions.

 The agent can start a KB article search by selecting the quick actions icon and then entering `search-kb`. The agent is prompted to search for the relevant KB article. Based on the search and the term that the agent enters, the agent is able to view the KB articles that match the search term. The agent can then select the KB article and include it in the discussion. The KB article is displayed as a record card in the Sidebar discussion. The KB article search is available with the base system.

 You can summarize a discussion by entering the `/summarize` quick action.

</td></tr><tr><td>

B - ![Smiley face icon signaling ability to add an emoji.](../image/sidebar-smiley-face-icon.png)

</td><td>

Display the emoji menu so you can add emojis to the discussion.

</td></tr><tr><td>

C - ![Attachment icon, displayed as a paperclip.](../image/sidebar-paper-clip-icon.png)

</td><td>

Add attachments to the current discussion so they can be shared with others in the discussion. You can drag files and select the send arrow icon or you can use the attachment icon.

</td></tr><tr><td>

D - ![Side arrowhead icon used to send the message.](../image/sidebar-send-arrow-icon.png)

</td><td>

Send the message.

</td></tr></tbody>
</table>    If you minimize a docked window, it appears as a tab in the overflow menu at the bottom of the screen. Hovering over a minimized docked window shows the record number and chat title to help identify the content. You can select any tab to access that discussion again. The overflow menu can hold up to 25 docked windows and this limit is configurable. If there are more docked windows than can be displayed as tabs in the overflow menu, a tab with a number indicates how many extra docked windows aren't displayed.


## Threaded replies

Use threaded replies to keep related messages grouped within Sidebar discussions. When you respond using a threaded reply, your message is added to the specific message you're replying to, rather than the main discussion.

To start a threaded reply to a message:

1.  Select reply arrow \(![Reply arrow icon.](../image/threaded-reply-arrow.png)\) next to the message you want to reply to:

    ![Start of a threaded reply in a Sidebar discussion.](../image/sidebar-threaded-1.png)

2.  The panel displays "Thread" followed by the discussion subject. Type your message in the text input box:

    ![Typing the text of a threaded reply.](../image/sidebar-threaded-2.png)

3.  Select the send arrow \(![Send arrow icon.](../image/threaded-send-arrow.png)\).
4.  Your messages appear under the parent message:

    ![Typing the text of a threaded reply.](../image/sidebar-threaded-3.png)

5.  If threaded reply has multiple messages, you can expand them to view all of the messages or you can collapse them and the number of messages displays instead.

    ![Multiple messages collapsed in a threaded reply.](../image/sidebar-threaded-4.png)


**Note:** If you delete a message with threaded replies, a warning appears letting you know that all its threaded replies will also be deleted.

## Activity stream and Sidebar

To enable agents to post Sidebar discussions to the activity stream, you must integrate Sidebar with the activity stream. For instructions on integrating Sidebar with the activity stream, see [Integrating Sidebar and activity stream](../task/integrate-sidebar-activity-stream.md). For information on using Sidebar with the activity stream, see [Activity stream in Sidebar](activity-stream-sidebar.md).

## Installing and configuring Sidebar

The Sidebar configuration settings are available via the Sidebar tab under **Conversational Interfaces** &gt; **Settings**. For instructions, see [Installing Sidebar](../task/install-sidebar.md). After Sidebar is installed, see [Configuring Sidebar](configure-sidebar.md) for instructions on configuring the admin settings.

## Using Sidebar

For information on how to use Sidebar, see [Using Sidebar](using-sidebar.md) for more information.

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

After Sidebar and Microsoft Teams are integrated, users of both applications can collaborate with each other. For more information on integrating Sidebar with Microsoft Teams, see [Sidebar and Microsoft Teams](sidebar-teams-overview.md).

## Core UI

You can create Sidebar discussions on interaction records from Next Experience Core UI.

## Domain Separation

For information about domain separation in Sidebar, see [Domain separation and Sidebar](sidebar-domain-separation.md).

## More information

To learn more, see the [Now learning course on Sidebar.](https://learning.servicenow.com/lxp?course_id=f1a907258736919cd3be437e0ebb3523&id=learning_course_prev)

