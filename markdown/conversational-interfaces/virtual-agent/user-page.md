---
title: Legacy - User Details page
description: Use the User Details page to see the history of a user's conversations.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Virtual Agent, User, Details, Page]
breadcrumb: [Legacy - Users tab, Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - User Details page

Use the User Details page to see the history of a user's conversations.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

The User Details page lists all chats that a user had with the Virtual Agent. It also displays the summary such as the language used in the chats, the first and last chats, and the channels.

![Virtual Agent Analytics User details page.](../images/user-details-page-va1.png "User details page")

You can select the star icon on the User Details page to tag the user as a favorite. In the Users page, you can easily list the users that are marked as favorite using the Filter Editor.

## Benefits

The User Details page enables you to do the following:

-   View detailed information about each chat, and mark chats as favorite. For more information, see [Get information about each chat](user-page.md#section_zj2_nmh_5pb).
-   View details about each user. For more information, see [Get information about each user](user-page.md#section_rpm_q5c_xpb).

## Get information about each chat

You can get more information about a chat that a user had with the Virtual Agent. To get detailed information about one of the chats listed on the User Details page, select a date in the list of conversations. The information appears on the side panel.

![Virtual Agent chat details tab.](../images/chat-details-va-1.png "Chat details")

To view the chat transcript for a user's conversation, select the **Transcript** tab.

![Virtual Agent conversation transcript tab.](../images/conversation-transcript-1.png "Conversation transcript")

To view the chat timeline, select the **Timeline** tab.

![Virtual Agent chat timeline tab.](../images/timeline-1.png "Timeline")

The **Timeline** tab shows the topic flow in the chat. For example, the following image shows that the chat started in Virtual Agent and moved to a live agent.

![Virtual Agent chat log topic flow with arrow indicating Closing Conversation message.](../images/dashboard-conversation-details-log.png "Topic flow")

The timeline shows that the user chatted with Virtual Agent until 5:25. Then the user requested to talk to a live agent, who joined the chat at 5:32. The timeline shows events such as how many responses Virtual Agent made, and when the live agent closed the chat.

![Virtual Agent chat log with arrow indicating Closing Conversation message.](../images/dashboard-closing-chat.png "Timeline log")

To tag the chat as favorite, select the star icon on the side panel. On the Conversations page, you can easily list the chats that are marked as favorite using the Filter Editor. For more information, see [Legacy - Conversations tab](conversation-tab.md).

## Get information about each user

The following table explains the fields in the User Details page:

|Field|Description|
|-----|-----------|
|User ID|User ID of the logged in user. If users don't log in, they appear in the sessions as anonymous.|
|First conversation|How long ago the user first started the Virtual Agent chat.|
|Last conversation|How long ago the user last had a Virtual Agent chat.|
|Time in chat|Duration of the Virtual Agent chat.|
|Languages|Language the user used in the chats.|
|Channels|Software that the user used to chat.|

**Parent Topic:**[Legacy - Users tab](users-tab.md)

