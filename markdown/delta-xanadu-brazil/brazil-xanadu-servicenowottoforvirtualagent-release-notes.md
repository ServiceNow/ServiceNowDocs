---
title: Combined ServiceNow Otto for Virtual Agent release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for ServiceNow Otto for Virtual Agent from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-servicenowottoforvirtualagent-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for Virtual Agent release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for ServiceNow Otto for Virtual Agent from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for Virtual Agent release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for Virtual Agent to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

You can upgrade ServiceNow Otto for Virtual Agent from the ServiceNow Store.


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for ServiceNow Otto for Virtual Agent.

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

</td></tr><tr><td>

Zurich

</td><td>

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&family=zurich&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings](https://www.servicenow.com/docs/access?context=asset-lib-conv-settings&family=zurich&ft:locale=en-US)Conversational settings**

Manage the settings for an asset directly from the Asset library page.


</td></tr><tr><td>

Australia

</td><td>

-   **[Assign search sources](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&family=australia&ft:locale=en-US)**

For premium chat, catalog items have improved fluidity; however, some of them are no longer conversational. They’ll open in a catalog form instead. This applies to Now Assist in Virtual Agent assistants and Now Assist panel – Platform assistant.

-   **[Select a display experience](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&family=australia&ft:locale=en-US)**
    -   If your instance is eligible, you can opt into the premium chat experience. ServiceNow performs a set of readiness checks to see if your instance is eligible for premium chat. Premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they're doing.
    -   An alert is shown when the instance is eligible for premium chat or when there is a possible delay for premium chat to appear as an option on your instance.
    -   When editing the display experience of an existing portal or mobile widget, chat experience options depend on the existing configuration.
    -   For channels, select channels from the **Add channels** drop-down list that integrate with the assistant.
    -   For Microsoft Teams, edit the channel to toggle between standard and premium chat.
-   **[Display assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&family=australia&ft:locale=en-US)**

An alert is shown when the instance is eligible for premium chat or when there is a possible delay for premium chat to appear as an option on your instance.

-   **[Brand and personalize an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&family=australia&ft:locale=en-US)**

Customize an assistant’s tone, response length, and persona in the **Personalization** section when branding your assistant. By default, personalization is hidden.To enable personalization, set the appropriate values in the **sn\_nowassist\_va.assistant\_personalization** system property. For more information, see [ServiceNow Otto for Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=australia&ft:locale=en-US).

-   **[Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&family=australia&ft:locale=en-US)**

For Now Assist in Virtual Agent assistants, voice input is available for premium chat.For Now Assist panel – Platform assistant, voice input is available for standard, enhanced, and premium chat.

-   **[Manage chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=australia&ft:locale=en-US)**

For premium chat, you can select a topic for fallback options.For premium messages, select the default greeting message, static greeting message, or select a custom topic. The static greeting message allows you to customize message.For premium chat, your premium messages and premium fallbacks are pre-filled with your legacy messages and legacy fallbacks.

-   **[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&family=australia&ft:locale=en-US)**

View **All assets** to see the assets that are assigned to an assistant.There is no limit to the number of assets that can be promoted.If an active asset is promoted, and later is set to inactive, the asset is not shown in the **Discoverable**, **Visible**, and **Promoted** lists.

-   **[ServiceNow Otto for Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=australia&ft:locale=en-US)**

Use the **sn\_nowassist\_va.assistant\_personalization** system property to show or hide chat personalization when branding an assistant. Personalization determines the tone of the assistant, response length, and persona.

-   **[Post-chat surveys](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

Collect user feedback in premium chats through post-chat surveys that trigger on agent task completion instead of waiting for a chat-end event. When an agent completes a task in an agentic flow, the survey can surface based on a configured probability, enabling you to gather insights that were previously unavailable.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Display assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&family=brazil&ft:locale=en-US)**

For eligible new customers, premium chat is the default and the only available chat experience. If the assistant uses the Now LLM Service provider, the premium chat option isn't available.

-   **[Embed on third-party sites for enhanced chat](https://www.servicenow.com/docs/access?context=add-portable-va-client-website&family=brazil&ft:locale=en-US)**

Embed the chat widget for enhanced chat on third-party websites.

-   **[View all topics on the premium chat greeting screen](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=brazil&ft:locale=en-US)**

Select **View all topics** on the chat’s greeting screen to show all promoted topics in premium chat.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ServiceNow Otto for Virtual Agent features.

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

-   **Changes to Virtual Agent Designer list view**
    -   Tabs have replaced pills in the Virtual Agent Designer list view.
    -   Hover over the tooltip icon \(\[Omitted image "image.i-tooltip"\] Alt text:\) to see information about the assistant you have selected from the drop-down menu.
    -   Use the new **AI agents** and **Agentic workflows** tabs to select from the types of topics on the home page, along with **Topics**, **Subflows**, **Actions**, and **Custom skills**.
    -   When a promoted asset has a conditional property that determines the context in which appears for an assistant, it's marked as **Condition applied** under **Show more**.

 -   **[Test assistant options](https://www.servicenow.com/docs/access?context=test-llm-topics&family=yokohama&ft:locale=en-US)**

The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Preferences](https://www.servicenow.com/docs/access?context=set-up-preferences-next-experience&family=zurich&ft:locale=en-US)**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Assistant Designer Asset library](https://www.servicenow.com/docs/access?context=vad-topics-page&family=zurich&ft:locale=en-US)**
    -   Tabs have replaced pills in the Virtual Agent Designer list view.
    -   Hover over the tooltip icon \(\[Omitted image "image.i-tooltip"\] Alt text:\) to see information about the assistant you have selected from the drop-down menu.
    -   Use the new **AI agents** and **Agentic workflows** tabs to select from the types of topics on the home page, along with **Topics**, **Subflows**, **Actions**, and **Custom skills**.
-   **Virtual Agent Designer [Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&family=zurich&ft:locale=en-US)**

Slide the new Show links for each record toggle switch to activate links for each record in the output in your Virtual Agent conversation.


 -   **[Test assistant options](https://www.servicenow.com/docs/access?context=test-llm-topics&family=zurich&ft:locale=en-US)**

The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


</td></tr><tr><td>

Australia

</td><td>

-   **[Updated Otto processing animation](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

View an updated Otto processing animation.

-   **[Assign Model Context Protocol \(MCP\) servers to an assistant](https://www.servicenow.com/docs/access?context=assign-mcp-servers&family=australia&ft:locale=en-US)**

Role-based configuration is no longer stored or managed within Assistant Designer.


 -   **[Upload files improvements](https://www.servicenow.com/docs/access?context=upload-documents-na-va&family=australia&ft:locale=en-US)**

Upload up to 10 files or 50 MB for the following file types: PDF native, PDF OCR, Word, PPTX, Excel, CSV, TXT, JPEG, PNG for premium chat in ServiceNow Otto for Virtual Agent and Otto panel.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Assign Model Context Protocol \(MCP\) servers to an assistant](https://www.servicenow.com/docs/access?context=assign-mcp-servers&family=brazil&ft:locale=en-US)**

Role-based configuration is no longer stored or managed within Assistant Designer.

-   **[Upload files improvements](https://www.servicenow.com/docs/access?context=upload-documents-na-va&family=brazil&ft:locale=en-US)**

Upload up to 10 files or 50 MB for the following file types: PDF native, PDF OCR, Word, PPTX, Excel, CSV, TXT, JPEG, PNG for premium chat in ServiceNow Otto for Virtual Agent and Otto panel.

-   **[Updated ServiceNow Otto processing animation](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=brazil&ft:locale=en-US)**

View an updated ServiceNow Otto processing animation.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some ServiceNow Otto for Virtual Agent features or functionality were removed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some ServiceNow Otto for Virtual Agent features or functionality were deprecated.

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

Support for Now Assist in Conversational IVR was removed.

</td></tr><tr><td>

Zurich

</td><td>

-   Starting with the Zurich release, [Sensitive Data Handler](https://www.servicenow.com/docs/access?context=ac-sensitive-data-overview&family=zurich&ft:locale=en-US) and Sensitive Data Masking capability are being prepared for future deprecation. They will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&family=zurich&ft:locale=en-US).

-   Starting with the Zurich release, Microsoft LUIS is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.


</td></tr><tr><td>

Australia

</td><td>

-   Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Brazil

</td><td>

-   **[Deprecation of Virtual Agent for NLU and keywords](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page-nlu&family=brazil&ft:locale=en-US)**

Starting with the Brazil release, Virtual Agent for NLU and Virtual Agent Lite are being prepared for future deprecation. They will eventually be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   **[Deprecation of Virtual Agent channel integrations applications](https://www.servicenow.com/docs/access?context=integrate-virtual-agent-nlu&family=brazil&ft:locale=en-US)**

Starting with the Brazil release, the following Virtual Agent channel integration applications are being prepared for future deprecation:

    -   [Conversational Integration with Alexa](https://www.servicenow.com/docs/access?context=conv-integ-alexa&family=brazil&ft:locale=en-US)
    -   [Conversational IVR with Amazon Connect](https://www.servicenow.com/docs/access?context=va-ivr-voice&family=brazil&ft:locale=en-US)
    -   [IBM Watson Assistant conversations](https://www.servicenow.com/docs/access?context=va-ibm-watson-assistant-config&family=brazil&ft:locale=en-US)
They will eventually be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   **[Now LLM Service deprecation notice](https://www.servicenow.com/docs/access?context=now-llm-model-updates&family=brazil&ft:locale=en-US)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Otto for Virtual Agent.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Virtual Agent is available with activation of the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) if you have the admin role. For details, see [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&family=brazil&ft:locale=en-US). Once activated, you can install ServiceNow Otto for Virtual Agent by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for Virtual Agent we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Additional requirements**

ServiceNow Otto for Virtual Agent requires at least one ServiceNow Otto product or the Requestor Agents - Foundation plugin.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto for Virtual Agent we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Browser requirements**

Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Otto for Virtual Agent, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto for Virtual Agent we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Localization information**

Dynamic Translation is supported for non-streaming ServiceNow Otto for Virtual Agent conversations. For more information, see [Translate conversations](https://www.servicenow.com/docs/access?context=dynamic-translation-va&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Otto for Virtual Agent we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   Use a conversation designer to build and test conversations without scripting or advanced skills.
-   Empower users to self-serve with AI agents, enhanced or premium chat with AI Search, conversational catalog skills, and more.
-   Seamlessly transfer the entire conversation history and context to the right human agent so they can quickly address any escalations and resolve user issues.

 See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

