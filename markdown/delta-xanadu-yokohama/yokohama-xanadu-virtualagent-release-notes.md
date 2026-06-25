---
title: Combined Virtual Agent release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Virtual Agent from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-virtualagent-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Virtual Agent release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Virtual Agent from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Virtual Agent release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Virtual Agent to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[AI agents in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&family=xanadu&ft:locale=en-US)**

View AI agents created in AI Agent Studio in Virtual Agent Designer.


-   **Quick start tests for [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=xanadu&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Virtual Agent works as expected. If you customized Virtual Agent, copy the quick start tests and configure them for your customizations.

-   **Rich text for Static and Dynamic Choice controls: [Static Choice user input control](https://www.servicenow.com/docs/access?context=va-static-choicelist&family=xanadu&ft:locale=en-US) and [Dynamic Choice user input control](https://www.servicenow.com/docs/access?context=va-reference-choicelist&family=xanadu&ft:locale=en-US)**

Use rich text options when creating Static and Dynamic Choice nodes in ServiceNow® Virtual Agent Designer.

-   **Virtual Agent Web Client branding: [Set up your Virtual Agent bot's branding](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&family=xanadu&ft:locale=en-US)**

Customize colors in the New Messages Above and New Messages Below banners in the chat window.

-   **LLM topic type association: [Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&family=xanadu&ft:locale=en-US)**

Associate LLM Assistants to Setup topics, Topic blocks, and Custom controls.

-   **[LLM topic testing](https://www.servicenow.com/docs/access?context=test-llm-topics&family=xanadu&ft:locale=en-US)**

Define an assistant on the Virtual Agent \(VA\) testing panel, when selecting Test All Active Topics with selecting an assistant.

-   **[LLM Text bot response control](https://www.servicenow.com/docs/access?context=va-ai-response&family=xanadu&ft:locale=en-US)**

Use the LLM Text bot response control to generate messages in conversations using LLM topic discovery.

-   **[Conversational Analytics dashboard in Platform Analytics experience](https://www.servicenow.com/docs/access?context=VA-dashboard-landing-page-pae&family=xanadu&ft:locale=en-US)**

The Conversational Analytics dashboard in the ServiceNow® Platform Analytics experience meets the compliance requirements of data regulated market environments, for example, Government Community Cloud \(GCC\). The dashboard contains indicators and breakdowns for rich visualizations and detailed analysis. You can access the dashboard by navigating to **All** &gt; **Conversational Interfaces** &gt; **Analytics**.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=xanadu&ft:locale=en-US)**

Determine whether actions for Virtual Agent notifications and Proactive Triggers are created after completing the full topic migration workflow via the **com.glide.cs.notification.create\_llm\_actions\_after\_topic\_migration** and **com.glide.cs.proactive\_trigger.create\_llm\_actions\_after\_topic\_migration** system properties.

-   **[NLU to LLM topic migration enhancements](https://www.servicenow.com/docs/access?context=llm-topic-migration&family=xanadu&ft:locale=en-US)**
    -   Migrate Virtual Agent notifications and Proactive Triggers actions on the Review connections step after publishing the newly migrated LLM topics in the NLU to LLM topic migration workflow.
    -   Review, edit, and test LLM topic descriptions against existing NLU utterances, if available, in the Review descriptions step. The Review descriptions step occurs after migration but before publication in the NLU to LLM topic migration workflow.
    -   Migrate NLU vocabulary sources automatically into either Dynamic Choice or Static Choice nodes, depending on the vocabulary sources setup in NLU.
-   **[Max wait time queue allows LLM topic selection](https://www.servicenow.com/docs/access?context=awa-create-queue-triggers&family=xanadu&ft:locale=en-US)**

Select LLM topics to be chosen after the max wait time is met during a Now Assist in Virtual Agent conversation. ServiceNow® Advanced Work Assignment queue triggers support LLM topics whenever the **Trigger Type** field's value is **Max Wait** and you’re prompted to select a Virtual Agent topic.

-   **[Catalogs for Virtual Agent](https://www.servicenow.com/docs/access?context=va-catalogs&family=xanadu&ft:locale=en-US)**

Search for and order services or products from catalog macroponents in Virtual Agent chat by using plain language. Customize the appearance of your catalogs to match your business’ branding.

-   **[Integrating Now Assist in Virtual Agent with Microsoft Copilot](https://www.servicenow.com/docs/access?context=ms-copilot-na-va&family=xanadu&ft:locale=en-US)**

Use your Self-configured bot to connect with Microsoft Copilot. The process of integrating the Self-configured bot with Microsoft Copilot is similar to that of integrating the Self-configured bot with Microsoft Teams.

You can @-mention the bot name to initiate a chat within Copilot and Copilot provides you the response based on your utterance.

Microsoft Copilot, when integrated with Now Assist in Virtual Agent, understands the ServiceNow context and routes users to Now Assist to conduct ServiceNow -related questions and tasks within Microsoft Teams.

Use your Now Virtual Agent bot to connect with Microsoft Copilot by @-mentioning the bot name.

Support for using declarative agents with Self-configured bots and transferring to live agents is available.

Support for the default Now Virtual Agent bot plugin is available on the Microsoft Teams Store.

-   **[Integrating Virtual Agent with enterprise messaging apps](https://www.servicenow.com/docs/access?context=integ-va-enterprise-apps&family=xanadu&ft:locale=en-US)**

Now LLM Service support for channels enables LLM-based conversations with Now Assist in Conversational Integration with Microsoft Teams and Conversational Integration with Slack.

The Now LLM Service support also provides new ServiceNow AI Search experience in channels with the following features:

    -   Legal disclaimers
    -   Pagination
    -   Search
    -   Generative AI Q&amp;A card
-   **[Configure rate limiting for providers](https://www.servicenow.com/docs/access?context=configure-rate-limit&family=xanadu&ft:locale=en-US)**

Configure rate limiting at the provider level to control the request flow for requests made within a stipulated time.


-   **[Primary and secondary assistants are honored in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=llm-assistants&family=xanadu&ft:locale=en-US)**

View which conversational assets are applicable to primary or secondary assistants.

-   **[Language detection for LLM conversations](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation&family=xanadu&ft:locale=en-US)**

For Now Assist in Virtual Agent users, use language detection for your LLM conversations to improve your user's experience.

-   **[Synthesized response](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&family=xanadu&ft:locale=en-US)**

For Now Assist in Virtual Agent users, a synthesized response can appear. A synthesized response includes a brief summary of the requested information and search results along with Genius Results. Mid-topic switching can occur during a conversation with synthesized response. Users can continue with their original request or switch the conversation's focus.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=xanadu&ft:locale=en-US)**

The following system property was added to increase flexibility of the search results and response:

    -   **sn\_nowassist\_va.synthesized\_autostart\_items**: When synthesized response only returns a singular action, configure whether to directly launch into that action. By default, whenever synthesized response returns a single Virtual Agent topic, that action is auto-launched. The following actions can be configured to auto-launch:
        -   Synthesized response returns a single conversational catalog item.
        -   Synthesized response returns a single Virtual Agent topic, along with Knowledge Base information.
        -   Synthesized response returns a single conversational catalog item, along with Knowledge Base information.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&family=yokohama&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings](https://www.servicenow.com/docs/access?context=asset-lib-conv-settings&family=yokohama&ft:locale=en-US)Conversational settings**

Manage the settings for an asset directly from the Asset library page.


-   **[Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&family=yokohama&ft:locale=en-US)**

Start the create flow for all supported conversational LLM assets directly from Virtual Agent Designer.

-   **[Assistants in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&family=yokohama&ft:locale=en-US)**

The Now Assist Panel - Platform \(default\) assistant is now available in Virtual Agent Designer.

-   **[AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&family=yokohama&ft:locale=en-US)**

Select AI agents to handle tasks in the AI Connector utility. For more information on AI agents in Virtual Agent Designer, see [Managing AI agents](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&family=yokohama&ft:locale=en-US) and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&family=yokohama&ft:locale=en-US).

-   **Virtual Agent Designer [Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&family=yokohama&ft:locale=en-US)**

Slide the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.

-   **Virtual Agent server**
    -   In chatHandshake, set **dynamic\_step\_loader\_enabled** to `true` to send stacked Agentic AI messages to server. Set **dynamic\_step\_loader\_enabled** to `false` to avoid sending messages.
    -   Pre-chat and post-chat surveys are now available for Anthropic Claude on AWS and Google Gemini LLMs. For more information on surveys, see [Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&family=yokohama&ft:locale=en-US).

-   **[AI Connector Utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&family=yokohama&ft:locale=en-US)**

Link custom skills to generative AI to add their functionality to LLM conversations.

-   **[AI agents and agentic workflows in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&family=yokohama&ft:locale=en-US)**

View AI agents and agentic workflows created in AI Agent Studio in Virtual Agent Designer.

-   **[Shorten responses option for bot text response](https://www.servicenow.com/docs/access?context=va-text-response&family=yokohama&ft:locale=en-US)**

For bot text responses, use the **Shorten responses** toggle in Virtual Agent Designer to turn on the **Show more** option in the chat on the user side.


-   **[Application scope for topics](https://www.servicenow.com/docs/access?context=vad-topic-creation-form&family=yokohama&ft:locale=en-US)**

Select the application scope for topics in Virtual Agent Designer.


-   **[Synthesized response in Slack conversations](https://www.servicenow.com/docs/access?context=slack-synthesized-response&family=yokohama&ft:locale=en-US)**

Generate synthesized responses in Slack conversations with Now Assist.

-   **[Virtual Agent feature support in Microsoft Teams conversations](https://www.servicenow.com/docs/access?context=va-teams-other-features&family=yokohama&ft:locale=en-US)**

Generate synthesized responses in Slack conversations with Now Assist.

-   **[Custom skills in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-custom-skills&family=yokohama&ft:locale=en-US)**

View skills created in Now Assist Skill Kit in Virtual Agent Designer.

-   **[Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&family=yokohama&ft:locale=en-US)**

Create chat surveys compatible with LLM-enabled user inputs, aside from the Carousel user input.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Virtual Agent features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Test assistant options](https://www.servicenow.com/docs/access?context=test-llm-topics&family=yokohama&ft:locale=en-US)**

The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


-   **[Dynamic Translation calls](https://www.servicenow.com/docs/access?context=translation-for-now-assist&family=yokohama&ft:locale=en-US)**

For Now Assist, if native translation is enabled, a Dynamic Translation call is only made if an unsupported language for native translation is used.

-   **[Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&family=yokohama&ft:locale=en-US)**

Use the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Virtual Agent features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Virtual Agent features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Starting with the Xanadu release, the Conversational Analytics dashboard is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Yokohama

</td><td>

Support for Now Assist in Conversational IVR was removed.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Virtual Agent is a ServiceNow AI Platform feature that is available with activation of the Glide Virtual Agent plugin \(com.glide.cs.chatbot\), which requires a separate subscription. For details, see [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&family=xanadu&ft:locale=en-US).

**Note:** The Glide Virtual Agent plugin initially installs the Topic Recommendations and Conversational Analytics apps. Subsequent updates to these apps must be installed from the ServiceNow Store.

 ServiceNow® Virtual Agent Lite is a subset of the Virtual Agent platform that is available to ServiceNow® IT Service Management \(ITSM\) customers. It doesn't require activation and works with ITSM Virtual Agent Lite conversations, which are also available to ITSM customers.

</td></tr><tr><td>

Yokohama

</td><td>

Virtual Agent is a ServiceNow AI Platform feature that is available with activation of the Glide Virtual Agent plugin \(com.glide.cs.chatbot\), which requires a separate subscription. For details, see [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&family=yokohama&ft:locale=en-US).

**Note:** The Glide Virtual Agent plugin initially installs the Topic Recommendations and Conversational Analytics applications. Subsequent updates to these apps must be installed from the ServiceNow Store.

 ServiceNow® Virtual Agent Lite is a subset of the Virtual Agent platform that is available to ServiceNow® IT Service Management \(ITSM\) customers. It doesn't require activation and works with ITSM Virtual Agent Lite conversations, which are also available to ITSM customers.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Virtual Agent, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The ServiceNow® Localization Framework is integrated in Virtual Agent.

</td></tr><tr><td>

Yokohama

</td><td>

The ServiceNow® Localization Framework is integrated in Virtual Agent.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Xanadu Patch 9](https://www.servicenow.com/docs/access?context=xanadu-patch-9&family=xanadu&ft:locale=en-US)

-   View people information in the synthesized response along with people citation when you search a person in Microsoft Teams chat.
-   AI agent support for Virtual Agent.
-   View AI agents in Virtual Agent Designer.

 -   Integrate ServiceNow® Now Assist for Virtual Agent with Microsoft Copilot to enable making IT-related calls and resolve tasks without having to leave the Microsoft Teams tenant.
-   Enable Now LLM Service support for Virtual Agent conversations in Conversational Integration with Microsoft Teams and Conversational Integration with Slack.
-   Review and test large language model \(LLM\) topic descriptions against existing Natural Language Understanding \(NLU\) utterances, migrate Virtual Agent notifications and Proactive Triggers, and migrate NLU vocabulary sources in the NLU to LLM topic migration workflow.
-   Configure One Extend Rate Limit for incoming requests for providers.
-   Now Assist conversational experience using Now Virtual Agent bot and Self-configured bots within Microsoft Copilot.

 Xanadu Patch 3

-   Use an updated Virtual Agent Designer list-based home page that includes conversational subflows and actions.
-   Work with conversations associated to primary and secondary assistants in Virtual Agent Designer.
-   Use language detection and engage in small talk within LLM conversations.
-   Receive a synthesized response for Now Assist in Virtual Agent users.

 See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=xanadu&ft:locale=en-US) for more information.

**Note:** Performance and the user experience are improved by tracking aggregate in-app activity, including interaction with the app. This tracking is focused on aggregated technical information rather than personal information.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 7](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.

 [Yokohama Patch 6](https://www.servicenow.com/docs/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Start the create flow for all supported conversational assets directly from Virtual Agent Designer.
-   Enhance the user experience with Slack response message streaming capability.

 [Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   View people information in the synthesized response along with people citation when you search a person in Microsoft Teams chat.
-   AI agent support for Virtual Agent.
-   View AI agents and agentic workflows in Virtual Agent Designer.
-   Select AI agents to handle tasks in the AI Connector utility. See [AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&family=yokohama&ft:locale=en-US), [Managing AI agents](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&family=yokohama&ft:locale=en-US), and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&family=yokohama&ft:locale=en-US) for more information.

 [Yokohama Patch 1](https://www.servicenow.com/docs/access?context=yokohama-patch-1&family=yokohama&ft:locale=en-US)

-   Enhance the user experience with Microsoft Teams response message streaming capability.

 [Yokohama Early Availability](https://www.servicenow.com/docs/access?context=yokohama-security-notables&family=yokohama&ft:locale=en-US)

-   Enhance the overall voice-based chat experience in Conversational IVR with Now Assist.
-   Generate synthesized responses in Slack conversations with Now Assist.
-   Generate synthesized responses in Microsoft Teams conversations with Now Assist.
-   View custom skills in Virtual Agent Designer.

 See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

