---
title: Configuring Conversational Interfaces
description: You can use the Conversational Interfaces console and the Chat Settings option in the Home page to explore and configure general chat functionality and set up Virtual Agent and Agent Chat features.
locale: en-US
release: xanadu
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2024-11-07"
reading_time_minutes: 9
keywords: [Configuring, Conversational Interfaces, Chat Settings, Virtual Agent, Agent Chat, Now Assist]
breadcrumb: [Conversational Interfaces Console, Conversational Interfaces]
---

# Configuring Conversational Interfaces

You can use the Conversational Interfaces console and the **Chat Settings** option in the **Home** page to explore and configure general chat functionality and set up Virtual Agent and Agent Chat features.

## Configuring Conversational Interfaces

Use the cards on the Conversational Interfaces console to set up features for Virtual Agent and Agent Chat. The cards automatically sort each time you visit and unaddressed features appear first.

For more information, select the question mark at the top right. This opens a contextual help panel.

![Contextual help panel for more information.](../image/CI-contextual-help.png)

<table id="table_spz_ngh_gbc"><thead><tr><th>

Card

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create a Virtual Agent with Now Assist, using an LLM model and generative AI skills.![Card with Create a virtual agent with LLM.](../image/create-va-with-llm-card.png)

</td><td>

To create a virtual agent using Now Assist, select **Get started** to display the Assistants screen. For more information, see [Manage LLM virtual agents on the Assistants screen](../../virtual-agent/task/manage-llm-va.md).

</td></tr><tr><td>

Create a Virtual Agent with NLU, which contains default settings and setup topics.![Card with Create a virtual agent with NLU.](../image/create-va-with-nlu-card.png)

</td><td>

To create a virtual agent using an NLU model:1.  Select **Get started** to open a new window with the plugin screen where you can install the com.glide.cs.chatbot plugin. For more information, see [Activate Virtual Agent](../../virtual-agent/task/activate-virtual-agent.md).
2.  After the plugin is installed, return to the previous window and refresh it using your browser's refresh button.
3.  Select **Settings** to display the CI Admin Experience settings page.
4.  In the left-hand panel, select **Virtual Agent** to configure your settings and NLU models. For more information, see [Configuring Virtual Agent](../../virtual-agent/concept/configure-virtual-agent.md).

</td></tr><tr><td>

Monitor your Now Assist in Virtual Agent![Card with Monitor your Now Assist in virtual agent.](../image/monitor-na-in-va.png)

</td><td>

To view Virtual Agent analytics for existing LLM virtual agents, select **View performance**. For more information, see [Analyzing Now Assist in Virtual Agent](../../now-assist-in-va/concept/now_assist_in_virtual_agent_analytics_dashboard.md).

 To manage existing LLM virtual agents, select **Manage assistants** to display the Assistants screen. For more information, see [Manage LLM virtual agents on the Assistants screen](../../virtual-agent/task/manage-llm-va.md).

</td></tr></tbody>
</table>|Card|Feature|Description|
|----|-------|-----------|
|![Choose pre-built topic plugins to handle your user requests. Options include IT Service Management, Customer Service Management, and HR Service Delivery plugins.](../image/ci-home-plugins-crop.png)|[Get pre-built topics](../../virtual-agent/reference/prebuilt-topics-ITSM.md)|Teach your bot to handle additional requests using pre-built conversation topics.|
|![Select the Request AI Search tile to add AI-powered search to your bot.](../image/ci-home-request-ai-search.png)|Request [AI Search](../../virtual-agent/concept/va-ai-search.md)|Give your users the power to search for answers to their questions or solutions to their requests by adding AI Search to your Virtual Agent bot.|
|![Select the Brand your bot tile to customize the look and feel of the chat window.](../image/ci-home-brand-your-bot.png)|[Brand your bot](branding-chat-client.md)|Customize your bot by selecting the colors and icons, and add a logo that reflects your company’s portal.|
|![Select the Create your bot's greeting tile to customize the way your bot greets users in different contexts.](../image/ci-home-create-bots-greeting.png)|[Create your bot's greeting](../../virtual-agent/task/configure-default-chat-experience.md)|Customize your bot by choosing how it greets and interacts with your users.|
|![Select the Add your bot to a portal tile to make your bot available in your user portals.](../image/ci-home-add-bot-portal.png)|[Add your bot to a portal](../task/ac-configure-bot-portal.md)|Choose where you want your Virtual Agent bot to live by adding it to a portal.|
|![Select the Set up Topic Recommendations tile to get recommendations for topics that are based on your data.](../image/ci-home-set-up-tr.png)|[Set up Topic Recommendations](../../virtual-agent/concept/va-topic-recommendations.md)|Get recommended topics based on analyses of existing support requests.|
|![Select the Capture conversational metrics tile to set up Conversational Analytics.](../image/ci-home-capture-conv-metrics.png)|[Capture conversational metrics](../../virtual-agent/concept/VA-dashboard-landing-page.md)|Use the Conversational Analytics Dashboard to collect interaction metrics to evaluate your bot's performance.|
|![Select the Set up your NLU tile to enable and configure Natural Language Understanding topic discovery for your Virtual Agent conversations.](../image/ci-home-set-up-nlu.png)|[Set up Natural Language Understanding \(NLU\)](../../virtual-agent/task/configure-nlu-settings.md)|Help your bot better understand a user's intent. For details, see [Advantages of natural language models over keywords](../../virtual-agent/concept/advantages-nlu.md).|
|![Select the Manage your channels tile to configure and customize conversations in other channels.](../image/ci-home-manage-bots-channels.png)|[Virtual Agent integration with messaging apps](../../virtual-agent/concept/va-integration-messaging-apps.md)|Add your bot to other channels, such as a Conversational Integration with Slack or Microsoft Teams.|
|![Select the Set up Agent Chat tile to connect users with a live agent on your instance.](../image/ci-home-set-up-ac.png)|[Set up Agent Chat](../task/ac-configure-agent-chat.md)|Connect users to live chat support in the chat client they are using.|
|![Select the Boost agent productivity tile to install Sidebar and help agents resolve user issues more quickly.](../image/ci-home-sidebar.png)|[Setting up Sidebar](../task/set-up-sidebar.md)|Provide live agents with a way to collaborate with others while they work on a Workspace record.|
|![Select the Get Profanity Filter tile to install a plugin that prevents users and agents from using prohibited words and phrases.](../image/ci-home-profanity-filter.png)|[Install and configure the Profanity Filter plugin for Agent Chat](ci-profanity-filter.md)|Prevent live agents from sending messages with inappropriate or profane language to requesters.|
|![Select the Get Virtual Agent for IVR tile to install the Interactive Voice Response plugin for Virtual Agent.](../image/ci-home-get-ivr.png)|[Install Conversational IVR with Amazon Connect](../../virtual-agent/task/install-va-ivr.md)|Enable user conversations with a bot using the phone channel.|
|![Select the Set up Dynamic Translation for VA tile to enable language detection and dynamic translation for Virtual Agent conversations.](../image/ci-home-dynamic-trans.png)|[Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](../../virtual-agent/concept/dynamic-lang-detection-translation-enhanced-chat.md)|Enable a combination of language detection and machine translation for Virtual Agent to improve the chat experience for diverse users.|
|![Select the Set up Issue Auto Resolution tile to enable your bot to proactively reach out to users to help them resolve support requests.](../image/ci-home-set-up-iar.png)|[Set up Issue Auto Resolution](../../virtual-agent/concept/auto-resolution-va.md)|Provide users with immediate self-service by using machine learning to intelligently deliver Virtual Agent topics, Knowledge articles, and catalog items.|
|![Select the Get Omnichannel Callback tile to](../image/ci-home-omnichannel-cllbck.png)|[Install Omnichannel Callback](https://www.servicenow.com/docs/access?context=install-omnichannel-callback&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)|Enable other ServiceNow® apps to display or announce callback options to users.|

## Assistants

The Assistants screen appears when you select the **Assistants** tab on the Conversational Interfaces home screen.

## Chat settings

The **Chat Settings** tab opens with the **General** tab selected. This tab contains general settings that apply to all Conversational Interfaces applications. The currently installed plugins and available plugins that you can activate are listed as links. Select a link for more information or to start an activation process.

The **Virtual Agent**, **Agent Chat**, and **Sidebar** tabs in the left navigation pane open configuration settings pages for each application.

![Chat client display options in Conversational Interfaces general settings.](../image/ci-home-chat-client-display-options.png)

For more information about these settings, see the following topics:

-   [General settings](ci-configuring-chat-features.md)
-   [Virtual Agent settings](../../virtual-agent/concept/configure-virtual-agent.md)
-   [Agent Chat settings](../task/ac-configure-agent-chat.md)
-   [Sidebar settings](configure-sidebar.md)

