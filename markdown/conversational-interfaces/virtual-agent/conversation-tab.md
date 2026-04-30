---
title: Legacy - Conversations tab
description: Use the Conversations tab to view the list of Virtual Agent conversations and details of each conversation that occurred during the selected date range.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Legacy, Virtual Agent, Designer, conversations, tab, sys\_cs\_conversation, chat\_analytics\_viewer, chat analytics viewer, filtering, transcript, details]
breadcrumb: [Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Conversations tab

Use the **Conversations** tab to view the list of Virtual Agent conversations and details of each conversation that occurred during the selected date range.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

All conversations from the Conversation table \[sys\_cs\_conversation\], that run on the Virtual Agent Designer are listed on the Conversations page, except for notifications, open \(ongoing\) conversations, and previews.

Virtual Agent conversations data is retained for a period of 90 days. The analytics data extracted from the conversations is retained for a period of two years.

To access the **Conversations** tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role. Conversation dates and times are in UTC.

![Virtual Agent Analytics conversations page set to all conversations, with first conversation in list highlighted.](../images/conversations-1.png "Conversations page")

## Conversations tab benefits

The **Conversations** tab enables you to do the following:

-   Filter the list of conversations easily by using pre-built filtering options. For more information, see [Filtering using list options](conversation-tab-filtering.md#section_xmk_mk3_spb).
-   Filter the list of conversations based on a specific condition and save conditions for filtering. For more information, see [Filtering using the Filter Editor](conversation-tab-filtering.md#section_izh_yrd_vpb).
-   Learn more about each conversation, view the conversation transcript, and mark a conversation as a favorite. For more information, see [Get conversation details](conversation-tab.md#section_i4l_jlt_j4b).
-   Export the list of conversations to a file. For more information, see [Export the conversations list](conversation-tab.md#section_y5z_md2_tpb).
-   Download the conversation transcript to troubleshoot individual conversations. For more information, see [Download the conversation transcript](conversation-tab.md#section_mdz_4f3_stb).

## Get conversation details

To get more information about a conversation, select one of the conversations in the list. The information appears on the side panel.

![Virtual Agent conversation details panel.](../images/chat-details-va-1.png "Conversation details")

To view and download the conversation transcript, select the **Transcript** tab.

![Virtual Agent Conversation transcript tab showing record of conversation.](../images/chat-transcript-download.png "Conversation transcript")

To view the conversation timeline, select the **Timeline** tab.

![Virtual Agent conversation Timeline tab, showing timestamps for Greetings and Anything Else Topic nodes.](../images/timeline-1.png "Conversation timeline")

To tag a conversation as a favorite, you can select the star icon on the side panel. On the Conversations page, you can easily list the conversations that are marked as favorite using the Filter Editor.

## Export the conversations list

To export the conversations list on the Conversations page to a file, select **Export**. In the Export pop-up window, specify the format for the file such as Excel, CSV, JSON, or PDF, and the delivery type such as email or download.

**Note:** You can export up to 1000 records only from the list on the page. This limit is not configurable.

## Conversation information

The following table describes the summarized Virtual Agent conversation information on the **Conversations** tab.

<table id="table_amh_4yj_b4b"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date

</td><td>

Date of the conversation.

</td></tr><tr><td>

Duration

</td><td>

Duration of the conversation.

</td></tr><tr><td>

User index

</td><td>

Link to go to the User Details page. It's a unique number that the system creates and permanently assigns to a Virtual Agent user. This number becomes a part of conversation records.This number is not the same as the system user ID.

</td></tr><tr><td>

Channel

</td><td>

Client software that the user used to chat.

</td></tr><tr><td>

Language

</td><td>

Language used for the conversation.

</td></tr><tr><td>

End state

</td><td>

How the conversation ended. For more information on various conversation end states, see [Virtual Agent interaction records](va-interactions.md).

</td></tr><tr><td>

Topics

</td><td>

Virtual Agent topics that were invoked during the chat conversation.

</td></tr><tr><td>

Favorites

</td><td>

Indicates whether the user is tagged as favorite.

</td></tr></tbody>
</table>## Download the conversation transcript

To download the conversation transcript, select a conversation from the conversations list and select **Download**.

The conversation transcript .txt file includes various data elements such as user input, Virtual Agent response, Flow Designer Integration Hub, flow action, custom controls, and topic block information for the selected conversation. This information helps Virtual Agent administrators to troubleshoot conversations, for example, conversations where there were errors or transfers to a live agent. For more information on the .txt file, see [Legacy - Conversation transcript template](../reference/chat-transcript-template.md).

-   **[Legacy - Use filters in the Conversation tab](conversation-tab-filtering.md)**  
You can filter out conversation for a deeper understanding.
-   **[Legacy - Conversation transcript template](../reference/chat-transcript-template.md)**  
The conversation transcript .txt file contains information used to troubleshoot individual conversations.

**Parent Topic:**[Legacy - Using the Conversational Analytics Dashboard](use-the-dashboard-overview.md)

