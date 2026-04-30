---
title: Virtual Agent Lite
description: Virtual Agent Lite is a limited version of Virtual Agent that is available to ITSM standard customers.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Virtual Agent, Lite, ITSM, IT Service Management, pre-built, conversations, slack, Microsoft, teams, msteams, workplace, messenger]
breadcrumb: [Explore, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent Lite

Virtual Agent Lite is a limited version of Virtual Agent that is available to ITSM standard customers.

## About Virtual Agent Lite

Use Virtual Agent Lite, to implement a virtual agent that provides IT service assistance using several pre-built ITSM conversations. As with Virtual Agent, you can set up and configure the chat clients for your end users. Use Virtual Agent Designer to review, duplicate, and publish the pre-built conversation topics for your end users.

Virtual Agent Lite is preinstalled in your instance. To use it, you must install ITSM Virtual Agent Conversation Topics Lite, which provides several pre-built conversations for common IT support requests. These keyword-based conversations run in the web chat client and also in Virtual Agent messaging integrations for the following channels:

-   Slack
-   Microsoft Teams
-   Workplace by Facebook
-   Facebook Messenger

## Virtual Agent Lite features

For Zurich, the Virtual Agent Designer features available in Virtual Agent Lite include the following:

-   Localization Framework integration.

    The Localization Framework is used in multi-language topic authoring and translations. The Localization Framework is installed automatically with Virtual Agent. Activate the ServiceNow® plugin for each language you want to support. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    In Virtual Agent Lite, information in the **Languages** tab is read-only.

-   Control topic discovery and visibility.

    The **Active** option of the header includes two options \(toggle switches\). Admins and topic authors can use these options to do one or both of the following:

    -   Enable Virtual Agent to discover topics for use in chats.
    -   Include a topic in the **All Topics** menu. This menu lists all of the topics that are available for use.
    For more information about using these options, see [Control topic discovery and visibility](../task/manage-topics-task.md).


After using Virtual Agent Lite, you can upgrade to Virtual Agent to access all of the features. Contact your ServiceNow account representative for upgrade information.

## Virtual Agent Lite limitations

Virtual Agent Lite has the following limitations:

-   Virtual Agent Designer limitations: Virtual Agent Lite only supports conversation topics in the ITSM self-service category \(including related topic blocks\) and the platform setup topics. This means you can't do the following:

    -   Create new topics, topic blocks, or custom controls.
    -   Specify the conditions that control how or when the topics are used.
    -   Specify the Live Agent \(chat\) variables that provide context for conversations.
    -   Enable the **Available for Agent Autopilot** toggle switch.
    **Note:** A lock icon displays next to the Virtual Agent Designer fields that are not available in Virtual Agent Lite.

-   Keyword-based conversations: Virtual Agent Lite only supports keyword-based conversations. Natural Language Understanding \(NLU\) models and NLU-enabled topics aren't supported. This means that related NLU features, such as topic switching and multi-language NLU models, are also not supported. Language support is available for conversations through ServiceNow AI Platform [language internationalization](https://www.servicenow.com/docs/access?context=c_LangInternationalizationSupport&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   Virtual Agent tables: Virtual Agent tables are read only for admins and Virtual Agent admins.
-   Localized content: Translated content is read-only. You can't add new translations or localize content. The **Languages** tab displays a banner asking users to contact their Account Executive for more information about upgrading to the latest release.
-   Custom channels: You can't run Virtual Agent Lite topics in any custom chat channels \(created through custom chat integrations\), except for the supported Virtual Agent integrations for Slack, Microsoft Teams, Workplace by Facebook, and Facebook Messenger applications.
-   Virtual Agent notifications: You can receive only simple and non-actionable notifications. Actionable notifications are not supported with Virtual Agent Lite.
-   Virtual Agent Analytics Dashboard: This feature is not available in Virtual Agent Lite.

## What to do

Set up and configure Virtual Agent Lite. For details, see [Quick start for Virtual Agent Lite](../task/quick-start-va-lite.md).

