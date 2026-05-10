---
title: Virtual Agent features supported in Slack conversations
description: Virtual Agent features, such as AI Search results, Virtual Agent notifications, and Virtual Agent Designer controls for creating Virtual Agent conversations are supported in Slack bot conversations.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent features supported in Slack conversations

Virtual Agent features, such as AI Search results, Virtual Agent notifications, and Virtual Agent Designer controls for creating Virtual Agent conversations are supported in Slack bot conversations.

**Note:** Conversational Integration for Slack is not supported for on-prem instances.

This section highlights key Virtual Agent features that are supported in the Conversational Integration with Slack app.

## AI Search results

Virtual Agent can generate AI Search results that are displayed as Genius result cards and multi-link outputs in conversations. For details on how Virtual Agent generates AI Search results, see [Improving the user experience with AI Search](va-ai-search.md). The default AI Search configuration for Virtual Agent enables search results for Q&amp;A \(knowledge base\) and catalog items.

## URL navigation for chat links

In Virtual Agent and Live Agent conversations on the Slack app, links to ServiceNow records open automatically in base system portals—including links displayed in output cards, Virtual Agent notifications, and AI Search results. If needed, admins can change the portals in which these links are opened. For configuration details, see [Configure URL navigation for chat links](../../conversational-interfaces/task/ac-configure-url-navigation.md).

## Trusted Domains

In custom chat integrations, the values specified in the Trusted media domains field of the Provider Channel Identities table \[sys\_cs\_provider\_application\] takes precedence over the Connections table \[sys\_cs\_provider\] and therefore overrides.

## Chat Localization into Conversation Language

Starting from version 5.0.1, chat gets localized into the customer specified conversation language set in the Slack UI, though the session language is different.

Translation of responses to the conversation language is done using the function `gs::getMessageLang(str, lang)`, where the language retrieved from Slack is passed through this function as a parameter. The translation process works with the following three use cases, when:

-   The requested language plugin is available in the ServiceNow instance.

    When the requested language plugin is available in the ServiceNow instance then the Session language honors the Conversation language set by the user.

-   The requested language plugin is absent, but fallback is set and enabled​.

    When the requested language plugin is absent, then the fallback language specified in the \[sys\_language\] table is used for the translation process. However, for the fallback mechanism to work, you must enable the **glide\_i18n.language\_fallback\_enabled** system property. By default, the value of the property is **false**. Set it to **true** to enable the fallback mechanism. For more information, see [Set a fallback language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/set-fallback-language.md).

-   The requested language plugin is absent, but fallback is not set/enabled.

    When the requested language plugin is absent and fallback is also not set/enabled, the default translation language will be English.


-   **[Virtual Agent Designer user input and bot response controls in Slack](va-designer-bot-controls-slack.md)**  
The Virtual Agent Designer user input controls and bot responses for creating conversation topics are supported in Slack conversations, including the table bot response and the card control that can display images.
-   **[Virtual Agent notifications supported in Slack](va-notif-slack.md)**  
Slack app supports Virtual Agent notifications during conversations.
-   **[Unsupported Virtual Agent features in Slack](../reference/limited-slack-features.md)**  
Refer to the unsupported features of Virtual Agent in Conversational Integration with Slack.

**Parent Topic:**[Conversational Integration with Slack](../task/mssg-slack.md)

