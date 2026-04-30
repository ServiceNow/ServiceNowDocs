---
title: Conversations tab
description: Use the Conversations tab to view the list of Virtual Agent conversations and details of each conversation that occurred during the selected date range.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Conversations tab

Use the **Conversations** tab to view the list of Virtual Agent conversations and details of each conversation that occurred during the selected date range.

All conversations from the Conversation table \[sys\_cs\_conversation\], that run on the Virtual Agent Designer are listed on the Conversations page, except for notifications, open \(ongoing\) conversations, and previews.

To tag a conversation as a favorite, select the star icon on the side panel. You can list all conversations that are marked as favorite using the Filter Editor.

Virtual Agent conversations and analytics data is retained for a period of two years.

To access the **Conversations** tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

![Virtual Agent Analytics conversations page set to all conversations, with first conversation in list highlighted.](../images/conversations-1-pae.png "Conversations page")

## Conversations tab benefits

The **Conversations** tab enables you to do the following:

-   Filter the list of conversations based on specific conditions using the filter editor. For more information, see [Use filters in the Conversation tab](conversation-tab-filtering-pae.md)
-   Learn more about each conversation by viewing conversation details. For more information, see [Get conversation details](conversation-tab-pae.md#section_i4l_jlt_j4b).
-   Export the list of conversations to a file. For more information, see [Export the conversations list](conversation-tab-pae.md#section_y5z_md2_tpb).
-   Download the conversation transcript to troubleshoot individual conversations. For more information, see [Download the conversation transcript](conversation-tab-pae.md#section_mdz_4f3_stb).

## Get conversation details

To get more information about a conversation, select one of the conversations in the list. The information appears on the side panel.

![Virtual Agent conversation details panel.](../images/vaa-next-conversation-details-pae.png "Conversation details")

To view and download the conversation transcript, select the **Transcript** tab.

![Virtual Agent Conversation transcript tab showing record of conversation.](../images/chat-transcript-download-pae.png "Conversation transcript")

## Export the conversations list

To export the conversations list on the Conversations page to a file, select **Export**. In the Export pop-up window, specify the format for the file such as Excel, CSV, JSON, or PDF, and the delivery type such as email or download.

**Note:** You can export up to 1000 records only from the list on the page. This limit is not configurable.

## Conversation information

The following table describes details of conversations listed in the **Conversations** tab.

<table id="table_amh_4yj_b4b"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date of the conversation.

</td></tr><tr><td>

Duration

</td><td>

Duration of the conversation.

</td></tr><tr><td>

User ID

</td><td>

Unique identifier that the system creates and permanently assigns to a Virtual Agent user. The Id becomes a part of conversation records.This is not the same as the system user ID.

</td></tr><tr><td>

Device Type

</td><td>

Conversational channel used for the chat.

</td></tr><tr><td>

Language

</td><td>

Language used for the conversation.

</td></tr><tr><td>

End state

</td><td>

How the conversation ended. For more information on various conversation end states, see [Virtual Agent interaction records](va-interactions.md).

</td></tr><tr><td>

Type

</td><td>

Type of conversation, for example, VA Only \(conversation initiated and completed in VA\).

</td></tr><tr><td>

Conversation

</td><td>

Sys Id of the conversation.

</td></tr></tbody>
</table>## Download the conversation transcript

To download the conversation transcript, select a conversation from the conversations list and click **Download**.

The conversation transcript .txt file includes various data elements such as user input, Virtual Agent response, Flow Designer Integration Hub, flow action, custom controls, and topic block information for the selected conversation. This information helps Virtual Agent administrators to troubleshoot conversations, for example, conversations where there were errors or transfers to a live agent. For more information on the .txt file, see [Conversation transcript template](../reference/chat-transcript-template-pae.md).

-   **[Conversation transcript template](../reference/chat-transcript-template-pae.md)**  
The conversation transcript .txt file contains information used to troubleshoot individual conversations.
-   **[Use filters in the Conversation tab](conversation-tab-filtering-pae.md)**  
You can filter out conversation for a deeper understanding.

**Parent Topic:**[Using the Conversational Analytics Dashboard](use-the-dashboard-overview-pae.md)

