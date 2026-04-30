---
title: Pre-chat surveys
description: Use pre-chat surveys to capture preliminary information from a customer. From the responses received, Advanced Work Assignment \(AWA\) routes chat conversations to appropriate queues and groups. Before entering into a chat conversation, the assigned agent can review the context of the issue.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the chat channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Pre-chat surveys

Use pre-chat surveys to capture preliminary information from a customer. From the responses received, Advanced Work Assignment \(AWA\) routes chat conversations to appropriate queues and groups. Before entering into a chat conversation, the assigned agent can review the context of the issue.

## Pre-chat features

Pre-chat surveys provide the following advantages that help agents efficiently handle chat conversations:

-   **Preconfigured pre-chat surveys**

    Pre-chat surveys determine the pre-chat questions presented to users. Preconfigured surveys are activated by default in the base system, but in order to avoid conflicts with previous configurations, customers who have upgraded have to manually activate them.​ These preconfigured surveys are:

    -   CSP Pre-Chat Survey - Collects preliminary information for logged-in customers.
    -   CSP Anonymous Pre-Chat Survey – Collects preliminary information for users who are not logged in.
    You can define a different survey or modify these predefined surveys. For more information, see [Create chat surveys](https://www.servicenow.com/docs/access?context=create-chat-surveys&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

-   **Routing chats to the correct queue**

    Advanced Work Assignment \(AWA\) leverages information captured through pre-chat surveys to route a chat to the right queue. For more information, see [Work item queues](https://www.servicenow.com/docs/access?context=awa-queues&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   **Identifying topics related to the chat issue**

    When customers enter a response to the standard pre-chat question "Please briefly describe your issue," Natural Language Understanding can help determine the appropriate Virtual Agent conversation topic. Relevant topics are automatically displayed to end users \(requesters\) rather than prompting them to choose from a list of conversation topics. For more information, see [Define context topic intent configurations](https://www.servicenow.com/docs/access?context=ac-configure-context-topic-intent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).


## Configuring Pre-chat if you have upgraded

Some settings need to be configured if you have upgraded your ServiceNow® instance. For more information, see [Configure Pre-chat after upgrading](../task/csm-configure-pre-chat-upgrade.md).

## Plugins

You must activate the Consumer Service Portal \(com.glide.service-portal.consumer-portal\) and Glide Conversation Server \(com.glide.cs\) plugins. To activate the plugins, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Related topics**  


[Pre-chat from the Consumer Service Portal](../task/csm-pre-chat.md)

