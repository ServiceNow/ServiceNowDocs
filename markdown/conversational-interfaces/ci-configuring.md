---
title: Configuring Conversational Interfaces
description: You can use the Conversational Interfaces console and the Chat Settings option in the Home page to explore and configure general chat functionality and set up Virtual Agent and Agent Chat features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/ci-configuring.html
release: zurich
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 9
keywords: [Configuring, Conversational Interfaces, Chat Settings, Virtual Agent, Agent Chat, Now Assist]
breadcrumb: [Conversational Interfaces Console, Conversational Interfaces]
---

# Configuring Conversational Interfaces

You can use the Conversational Interfaces console and the **Chat Settings** option in the **Home** page to explore and configure general chat functionality and set up Virtual Agent and Agent Chat features.

## Configuring Conversational Interfaces

Use the cards on the Conversational Interfaces console to set up features for Virtual Agent and Agent Chat. The cards automatically sort each time you visit and unaddressed features appear first.

For more information, select the question mark at the top right. This opens a contextual help panel.

<table id="table_spz_ngh_gbc"><thead><tr><th>

Card

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create a Virtual Agent with Now Assist, using an LLM model and generative AI skills.\[Omitted image "create-va-with-llm-card.png"\] Alt text: Card with Create a virtual agent with LLM.

</td><td>

To create a virtual agent using Now Assist, select **Get started** to display the Assistants screen. For more information, see [Manage LLM virtual agents on the Assistants screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/manage-llm-va.md).

</td></tr><tr><td>

Create a Virtual Agent with NLU, which contains default settings and setup topics.\[Omitted image "create-va-with-nlu-card.png"\] Alt text: Card with Create a virtual agent with NLU.

</td><td>

To create a virtual agent using an NLU model:1.  Select **Get started** to open a new window with the plugin screen where you can install the com.glide.cs.chatbot plugin. For more information, see [Activate Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/activate-virtual-agent.md).
2.  After the plugin is installed, return to the previous window and refresh it using your browser's refresh button.
3.  Select **Settings** to display the CI Admin Experience settings page.
4.  In the left-hand panel, select **Virtual Agent** to configure your settings and NLU models. For more information, see [Configuring Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-virtual-agent.md).

</td></tr><tr><td>

Monitor your Now Assist in Virtual Agent\[Omitted image "monitor-na-in-va.png"\] Alt text: Card with Monitor your Now Assist in virtual agent.

</td><td>

To view Virtual Agent analytics for existing LLM virtual agents, select **View performance**. For more information, see .

 To manage existing LLM virtual agents, select **Manage assistants** to display the Assistants screen. For more information, see [Manage LLM virtual agents on the Assistants screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/manage-llm-va.md).

</td></tr></tbody>
</table>|Card|Feature|Description|
|----|-------|-----------|
|\[Omitted image "ci-home-plugins-crop.png"\] Alt text: Choose pre-built topic plugins to handle your user requests. Options include IT Service Management, Customer Service Management, and HR Service Delivery plugins.|[Get pre-built topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/prebuilt-topics-ITSM.md)|Teach your bot to handle additional requests using pre-built conversation topics.|
|\[Omitted image "ci-home-request-ai-search.png"\] Alt text: Select the Set up AI Search tile to add AI-powered search to your bot.|Set up [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-ai-search.md)|Give your users the power to search for answers to their questions or solutions to their requests by adding AI Search to your Virtual Agent bot.|
|\[Omitted image "ci-home-brand-your-bot.png"\] Alt text: Select the Brand your Virtual Agent tile to customize the look and feel of the chat window.|[Brand your Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/branding-chat-client.md)|Customize your Virtual Agent bot by selecting the colors and icons, and add a logo that reflects your company’s portal.|
|\[Omitted image "ci-home-create-bots-greeting.png"\] Alt text: Select the Create your VA's greeting tile to customize the way your bot greets users in different contexts.|[Create your VA's greeting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-default-chat-experience.md)|Customize your Virtual Agent bot by choosing how it greets and interacts with your users.|
|\[Omitted image "ci-home-add-bot-portal.png"\] Alt text: Select the Add your bot to a portal tile to make your bot available in your user portals.|[Add your bot to a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/ac-configure-bot-portal.md)|Choose where you want your Virtual Agent bot to live by adding it to a portal.|
|\[Omitted image "ci-home-set-up-tr.png"\] Alt text: Select the Set up Topic Recommendations tile to get recommendations for topics that are based on your data.|[Set up Topic Recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-topic-recommendations.md)|Get recommended topics based on analyses of existing support requests.|
|\[Omitted image "ci-home-capture-conv-metrics.png"\] Alt text: Select the Capture conversational metrics tile to set up Conversational Analytics.|Capture conversational metrics|Use the Conversational Analytics Dashboard to collect interaction metrics to evaluate your bot's performance.|
|\[Omitted image "ci-home-set-up-nlu.png"\] Alt text: Select the Review your NLU settings tile to enable and configure Natural Language Understanding topic discovery for your Virtual Agent conversations.|[Configure Natural Language Understanding in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-nlu-settings.md)|Help your bot better understand a user's intent. For details, see [Advantages of natural language models over keywords](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/advantages-nlu.md).|
|\[Omitted image "ci-home-manage-bots-channels.png"\] Alt text: Select the Add your VA to other channels tile to configure and customize conversations in other channels.|[Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-integration-messaging-apps.md)|Add your Virtual Agent bot to other channels, such as a Conversational Integration with Slack or Microsoft Teams.|
|\[Omitted image "ci-home-set-up-ac.png"\] Alt text: Select the Set up Agent Chat tile to connect users with a live agent on your instance.|[Set up Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/agent-chat/ac-configure-agent-chat.md)|Connect users to live chat support in the chat client they are using.|
|\[Omitted image "ci-home-sidebar.png"\] Alt text: Select the Boost agent productivity with Sidebar tile to install Sidebar and help agents resolve user issues more quickly.|[Setting up Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/set-up-sidebar.md)|Provide live agents with a way to collaborate with others while they work on a Workspace record.|
|\[Omitted image "ci-home-profanity-filter.png"\] Alt text: Select the Get Profanity Filter tile to install a plugin that prevents users and agents from using prohibited words and phrases.|[Install and configure the Profanity Filter plugin for Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/agent-chat/ci-profanity-filter.md)|Prevent live agents from sending messages with inappropriate or profane language to requesters.|
|\[Omitted image "ci-home-get-ivr.png"\] Alt text: Select the Set up Virtual Agent for IVR tile to install the Interactive Voice Response plugin for Virtual Agent.|[Install Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/install-va-ivr.md)|Enable user conversations with a bot using the phone channel.|
|\[Omitted image "ci-home-dynamic-trans.png"\] Alt text: Select the Set up Dynamic Translation for VA tile to enable language detection and dynamic translation for Virtual Agent conversations.|[Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/dynamic-lang-detection-translation-enhanced-chat.md)|Enable a combination of language detection and machine translation for Virtual Agent to improve the chat experience for diverse users.|
|\[Omitted image "ci-home-set-up-iar.png"\] Alt text: Select the Set up Issue Auto Resolution tile to enable your bot to proactively reach out to users to help them resolve support requests.|[Set up Issue Auto Resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/auto-resolution-va.md)|Provide users with immediate self-service by using machine learning to intelligently deliver Virtual Agent topics, Knowledge articles, and catalog items.|
|\[Omitted image "ci-home-omnichannel-cllbck.png"\] Alt text: Select the Get Omnichannel Callback tile to give your customers a callback option.|[Install Omnichannel Callback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/omnichannel-callback/install-omnichannel-callback.md)|Enable other ServiceNow® apps to display or announce callback options to users.|

## Assistants

The Assistants screen appears when you select the **Assistants** tab on the Conversational Interfaces home screen.

## Chat settings

The **Chat Settings** tab opens with the **General** tab selected. This tab contains general settings that apply to all Conversational Interfaces applications. The currently installed plugins and available plugins that you can activate are listed as links. Select a link for more information or to start an activation process.

The **Virtual Agent**, **Agent Chat**, and **Sidebar** tabs in the left navigation pane open configuration settings pages for each application.

\[Omitted image "ci-home-chat-client-display-options.png"\] Alt text: Chat client display options in Conversational Interfaces general settings.

For more information about these settings, see the following topics:

-   [General settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/ci-configuring-chat-features.md)
-   [Virtual Agent settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-virtual-agent.md)
-   [Agent Chat settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/agent-chat/ac-configure-agent-chat.md)
-   [Sidebar settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/configure-sidebar.md)

