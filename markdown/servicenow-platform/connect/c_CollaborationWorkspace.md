---
title: Connect workspace
description: The Connect workspace is a full-screen view of all your Connect Chat and Connect Support conversations in one place. It contains the conversation pane, which displays the conversation header and an expanded version of the mini window, and the conversation tools area.The conversation pane of the Connect workspace displays the conversation header and an expanded version of the mini window.The conversation tools area in the Connect workspace contains several tabs, each represented by an icon.
locale: en-US
release: yokohama
product: Connect
classification: connect
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Connect interface, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Connect workspace

The Connect workspace is a full-screen view of all your Connect Chat and Connect Support conversations in one place. It contains the conversation pane, which displays the conversation header and an expanded version of the mini window, and the conversation tools area.

To open the Connect workspace, navigate to **Collaborate** &gt; **Connect Chat** or click the new window icon \(![New window icon](../image/IconNewWindow.png)\) in a Connect mini window. If you do not have any recent conversations, a screen appears with helpful information about Connect.

The Connect workspace is composed of the following elements.

|Element|Description|
|-------|-----------|
|Sidebar|Provides access to conversations. The Connect sidebar behaves the same way in the workspace as it does in the Connect overlay. The only difference is that the sidebar appears on the left edge of the Connect workspace. For more information about using the sidebar, see [Connect sidebar](c_CollaborationOverlay.md#).|
|Conversation pane|Displays the currently selected conversation.|
|Conversation tools|Provides quick access to key information, conversation members, attachments, and notification preferences for the currently selected conversation. Some of the conversation tools vary depending on the type of conversation.|

![The Connect workspace contains the Connect sidebar, a conversation pane, and conversation tools](../image/ConnectWorkspace.png "Connect workspace")

## Conversation pane

The conversation pane of the Connect workspace displays the conversation header and an expanded version of the mini window.

The header displays basic conversation details like the avatar and name. You can [edit these details](../task/t_EditBasicConversationDetails.md) for group or record conversations.

Below the header, messages appear in chronological order. You can enter messages in the text entry field at the bottom of the window.

## Connect conversation tools

The conversation tools area in the Connect workspace contains several tabs, each represented by an icon.

Click an icon to open the tab. Click the same icon again to hide the tab. The tabs you see for each conversation depend on the conversation type and other conditions.

<table id="table_ptn_nlj_br"><thead><tr><th>

Tab icon

</th><th>

Tab name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Info tab icon](../image/IconInfoTab.png)

</td><td>

Info

</td><td>

Contains the following sections, each of which appears only if it contains information.-   **Record**: Lists details about the record the current conversation follows, such as record number, state, assignee, and short description. The fields displayed in this section vary by the type of record. This section is available only for record conversations.
-   **Related Records**: Lists Visual Task Boards and task records that have been referenced in the conversation, such as incidents, problems, or changes. When you send a record number as a message or drag a record in a conversation, it appears as a link. The list displays the short description for each task. Click a task to open the record in a new browser tab. Only conversation members who have rights to view the tasks can access them.
-   **Links**: Lists URLs that have been referenced in the conversation. Click a link to open the destination page in a new browser tab.

 This tab is not available for support conversations.

</td></tr><tr><td>

![Record tab icon](../image/IconRecordTab.png)

</td><td>

Record

</td><td>

Displays a compact form view of a record created from the current conversation, such as an incident. If more than one record has been created from the conversation, there is a separate record tab for each one. These tabs are available only for support conversations.

</td></tr><tr><td>

![Knowledge base tab icon](../image/IconKnowledgeBaseTab.png)

</td><td>

Knowledge Base

</td><td>

Displays a compact view of the knowledge homepage. For more information, see [Share knowledge in a Connect Support conversation](../task/t_ShareKnowledgeInConnectSupport.md).

</td></tr><tr><td>

![Members tab icon](../image/IconMembersTab.png)

</td><td>

Members

</td><td>

Lists all members of the current conversation. You can add or remove conversation members for group and record conversations.

</td></tr><tr><td>

![Attachments tab icon](../image/IconAttach.png)

</td><td>

Attachments

</td><td>

Lists all attachments in the conversation. Click an attachment to open it. Click **Add Attachment** to upload an attachment.

</td></tr><tr><td>

![Notification preferences tab icon](../image/IconNotificationPreferences.png)

</td><td>

Notification preferences

</td><td>

Contains settings to control which notifications you receive for the current conversation. For more information, see [Edit which notifications you receive for a conversation](../task/t_EditNotifRecAConv.md).

</td></tr></tbody>
</table>