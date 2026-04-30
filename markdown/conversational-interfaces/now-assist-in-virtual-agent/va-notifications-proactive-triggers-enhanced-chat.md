---
title: Proactive triggers and Virtual Agent notifications in enhanced chat
description: Proactive triggers and Virtual Agent notifications can be selected and completed in a Virtual Agent conversation.
locale: en-US
release: yokohama
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2025-04-01"
reading_time_minutes: 2
keywords: [Using, Now Assist, Virtual Agent, AI Search, Proactive triggers, Notifications, genius results, generative AI]
breadcrumb: [Enhanced chat, Using Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Proactive triggers and Virtual Agent notifications in enhanced chat

Proactive triggers and Virtual Agent notifications can be selected and completed in a Virtual Agent conversation.

Proactive triggers and simple Virtual Agent notifications are displayed the same way on the portal as a pop-up rectangle box.

![A pop-up rectangle box appears near the Now Assist in Virtual Agent enhanced chat button.](../image/pt-va-notification-nass-only.png "Example of proactive trigger or notification in enhanced chat")

Proactive triggers and Virtual Agent notifications only display on the portal pages with the chat button and are unavailable in the full-page experience view. Selecting a proactive trigger redirects you to a new chat. If you switch to a new chat while another active chat is ongoing, a pop-up message on the chats icon ![Chats icon.](../image/nass-chats-icon.png) appears: `Your previous chat was saved. You can revisit all of your past chats and continue ones that are still active.`For more information on Proactive Triggers, see [Exploring Proactive Triggers](https://www.servicenow.com/docs/access?context=proactive-triggers&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Virtual Agent notifications display as an unread message and after you select the notification, the notification displays in the chat conversation. For Virtual Agent notifications, the **sn\_nowassist\_va.nass\_notification\_enabled** system property defaults to `true` in System Properties \(sys\_properties.list\). When **sn\_nowassist\_va.nass\_notification\_enabled** is set to `true`, Virtual Agent notifications appear on your portal home page. Selecting a notification redirects you to the conversation in a chat. Simple \(nonactionable\) notifications are displayed in the navigation area's **Chats** &gt; **Updates** section. Actionable notifications are displayed in the navigation area's **Chats** &gt; **Active** section. These actionable notifications create a chat with the notification title as the chat title. Selecting an actionable notification loads the conversation with the notification and associated actions. If you don't act and initiate a search, after viewing the search results, you can switch back to the notification that triggered the conversation by entering `Show notifications`. Entering `Show notifications` in a non-notification conversation results in a message indicating that there are no actionable notifications to view. To view your actionable notifications, it’s best to select the chats icon \(![Chats icon.](../image/nass-chats-icon.png)\). When you select a notification, the unread badge count on the chats icon \(![Chats icon.](../image/nass-chats-icon.png)\) goes down. After you have worked with the actionable notification, the notification moves to the **Chats** &gt; **Closed** section. For more information on configuring Notifications, see [Configuring Virtual Agent notifications](../../virtual-agent/concept/configuring-va-notifications.md) and [Configure a delivery channel for Virtual Agent notification](../../virtual-agent/task/configure-delivery-channel.md).

