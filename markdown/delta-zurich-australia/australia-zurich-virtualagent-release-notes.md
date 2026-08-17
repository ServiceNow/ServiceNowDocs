---
title: Combined Virtual Agent release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Virtual Agent from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-virtualagent-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Virtual Agent release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Virtual Agent from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Virtual Agent release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Virtual Agent to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&family=zurich&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings](https://www.servicenow.com/docs/access?context=asset-lib-conv-settings&family=zurich&ft:locale=en-US)Conversational settings**

Manage the settings for an asset directly from the Asset library page.


-   **[Integrating with Google Workspace](https://www.servicenow.com/docs/access?context=integrate-with-gsuite&family=zurich&ft:locale=en-US)**

Integrate Google Workspace chat with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.

-   **[AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&family=zurich&ft:locale=en-US)**

Select AI agents to handle tasks in the AI Connector utility. For more information on AI agents in Virtual Agent Designer, see [Managing AI agents](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&family=zurich&ft:locale=en-US) and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&family=zurich&ft:locale=en-US).

-   **[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=zurich&ft:locale=en-US) server**
    -   In chatHandshake, set **dynamic\_step\_loader\_enabled** to `true` to send stacked agentic AI messages to the server. Set **dynamic\_step\_loader\_enabled** to `false` to avoid sending messages.
    -   Pre-chat and post-chat surveys are now available for Anthropic Claude on AWS and Google Gemini large language models \(LLMs\). For more information on surveys, see [Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&family=zurich&ft:locale=en-US).
-   **[Create a Virtual Agent asset](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&family=zurich&ft:locale=en-US)**

Start the create flow for all supported conversational LLM assets directly from Virtual Agent Designer.

-   **[Assistants in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&family=zurich&ft:locale=en-US)**

The Now Assist Panel - Platform \(default\) assistant is now available in Virtual Agent Designer.

-   **[Integrating ServiceNow Otto for Virtual Agent with Microsoft Copilot](https://www.servicenow.com/docs/access?context=ms-copilot-na-va&family=zurich&ft:locale=en-US)**

Custom Engine Agent \(CEA\) is replacing the legacy Microsoft bot framework, allowing Microsoft Copilot to discover Virtual Agent, Now Assist, and use multi-turn conversations.


</td></tr><tr><td>

Australia

</td><td>

-   **[View Live Agent status updates](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

Routing messages and section headers indicate when the live agent has entered and left the chat in premium chat conversations.


-   **[Switch between interactive views](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

In premium chat conversations, switch between multiple interactive views through the drop-down selector including Knowledge Base articles, catalog forms, org charts, and AI agent widgets.


-   **[Assign Model Context Protocol \(MCP\) servers to an assistant](https://www.servicenow.com/docs/access?context=assign-mcp-servers&family=australia&ft:locale=en-US)**

Admins can assign configured Model Context Protocol \(MCP\) servers to assistants. Role-based access can be configured for each assigned MCP server to control which users can access MCP-provided capabilities through the assistant.

-   **[Brand and personalize an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&family=australia&ft:locale=en-US)**

Enable estimated wait time for the next live agent. When enabled, users see the estimated wait time for the live agent in the chat menu item.

-   **[Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&family=australia&ft:locale=en-US)**

Premium chat now supports uploading documents directly into a conversation.

-   **[Review settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&family=australia&ft:locale=en-US)**

The MCP servers section shows which users can access Model Context Protocol \(MCP\)-provided capabilities through the assistant.

-   **[ServiceNow Otto for Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=australia&ft:locale=en-US)**

Personalization is now shown by default.


-   **[Assign search sources](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&family=australia&ft:locale=en-US)**

Premium chat prefills messages with legacy messages that were previously configured in your standard or enhanced chat experiences.

By default, portals and mobile apps that have enhanced chat with a dynamic, movable, and resizable window use the assistant search profile for both portal/mobile search and the assistant search. Admins can now turn off this behavior and continue to use the portal/mobile search profile independently.

The **Include AI Responses** column shows whether the search source is included in the synthesized response. Within Assistant Designer, the setting is read-only. However, it can be modified in AI Search Admin console.

-   **[Select a display experience](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&family=australia&ft:locale=en-US)**

Mobile custom apps support configuration of enhanced chat and premium chat display options, with availability dependent on the widget's current configuration.

-   **[Manage chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=australia&ft:locale=en-US)**

If you configured legacy messages and legacy fallbacks, your premium messages and premium fallbacks are prefilled with what you had in your legacy messages and legacy fallbacks. In this release, closing topics, closing messages, and survey topic are now prefilled.

Closing topic, closing message, and survey topic are available for standard, enhanced, and premium chat for Now Assist in Virtual Agent.

-   **[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&family=australia&ft:locale=en-US)**

When editing an assistant with premium chat, create, edit, or delete prompts from the prompt library. Prompts help users ask better questions and get more accurate answers. Use the prompt library to manage prompts that users see in premium chat. Create your own prompts or use the default prompts.

-   **[Prompt library](https://www.servicenow.com/docs/access?context=now-assist-prompt-library&family=australia&ft:locale=en-US)**

Browse and select from promoted prompt templates or save your own custom prompts, eliminating the need to retype frequently-used prompts within your chats. Access your reusable templates instantly from the omnibar for faster, more consistent conversations.

-   **[View uploaded documents in interactive view](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

When in premium chat conversations, you can upload a document and view it in the interactive view.


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

Customize an assistant’s tone, response length, and persona in the **Personalization** section when branding your assistant. By default, personalization is hidden.

To enable personalization, set the appropriate values in the **sn\_nowassist\_va.assistant\_personalization** system property. For more information, see [ServiceNow Otto for Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=australia&ft:locale=en-US).

-   **[Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&family=australia&ft:locale=en-US)**

For Now Assist in Virtual Agent assistants, voice input is available for premium chat.

For Now Assist panel – Platform assistant, voice input is available for standard, enhanced, and premium chat.

-   **[Manage chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=australia&ft:locale=en-US)**

For premium chat, you can select a topic for fallback options.

For premium messages, select the default greeting message, static greeting message, or select a custom topic. The static greeting message allows you to customize message.

For premium chat, your premium messages and premium fallbacks are pre-filled with your legacy messages and legacy fallbacks.

-   **[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&family=australia&ft:locale=en-US)**

View **All assets** to see the assets that are assigned to an assistant.

There is no limit to the number of assets that can be promoted.

If an active asset is promoted, and later is set to inactive, the asset is not shown in the **Discoverable**, **Visible**, and **Promoted** lists.

-   **[ServiceNow Otto for Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=australia&ft:locale=en-US)**

Use the **sn\_nowassist\_va.assistant\_personalization** system property to show or hide chat personalization when branding an assistant. Personalization determines the tone of the assistant, response length, and persona.

-   **[\[Placeholder link text to key bundle-convint.deployment-config-attributes\]](https://www.servicenow.com/docs/access?context=deployment-config-attributes&family=australia&ft:locale=en-US)**

Manage the behavior of suggestions that users see when typing in the input box.

-   **[Post-chat surveys](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

Collect user feedback in premium chats through post-chat surveys that trigger on agent task completion instead of waiting for a chat-end event. When an agent completes a task in an agentic flow, the survey can surface based on a configured probability, enabling you to gather insights that were previously unavailable.


-   **[View assistants](https://www.servicenow.com/docs/access?context=view-assistants&family=australia&ft:locale=en-US)**

If you have the **com.snc.ex\_ai\_portal** \(Employee Slate\) app installed, the default Employee Slate assistant is shown, and Employee Slate is mapped to it by default. The default Employee Slate assistant can be activated, deactivated, edited, and tested. It can’t be deleted.

-   **[Select a display experience](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&family=australia&ft:locale=en-US)**

The default Employee Slate assistant comes with premium chat. Premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they’re doing.

-   **[Brand and personalize an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&family=australia&ft:locale=en-US)**

For the default Employee Slate assistant, configure premium chat branding. Select and configure the chat header, chat logo, and chat menu items such as a phone number, email, and link.

A **Channels** section is shown for Now Assist in Virtual Agent assistants and the default Employee Slate assistant if a channel is configured in the display experience.

-   **[Manage chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=australia&ft:locale=en-US)**

Depending on your configuration, different greeting, closing, and fallback options may appear. Legacy messages \(chat messages\) and legacy fallbacks \(chat fallbacks\) are shown when at least one display experience has standard chat or enhanced chat. Premium messages and premium fallbacks are shown when at least one display experience has premium chat.

-   **[Test a chat assistant](https://www.servicenow.com/docs/access?context=test-assistant&family=australia&ft:locale=en-US)**

Test your chat assistant \(standard, enhanced, or premium chat\) to simulate an end-to-end conversation before moving your experience into a production environment.

-   **[Assistant Designer Asset library](https://www.servicenow.com/docs/access?context=vad-topics-page&family=australia&ft:locale=en-US)**

Use the **Test Assistant** button to test your LLM assistant in Standard, Enhanced, and Premium Chat, after adding chat experiences in Assistant Designer's **Assistants** tab.

-   **[Now Assist in Virtual Agent on mobile](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&family=australia&ft:locale=en-US)**

Use the modified version of Now Assist in Virtual Agent on your mobile device. This redesigned version adapts to smaller screens without losing functionality or clarity.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Premium chat experience for Now Assist Panel - Platform \(default\) assistant](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

The Now Assist Panel - Platform \(default\) assistant now has the premium chat experience configured by default.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Virtual Agent features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=zurich&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&family=zurich&ft:locale=en-US)**

Use the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.

-   **[Test assistant options](https://www.servicenow.com/docs/access?context=test-llm-topics&family=zurich&ft:locale=en-US)**

The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**




</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Virtual Agent features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Virtual Agent features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Starting with the Zurich release, [Sensitive Data Handler](https://www.servicenow.com/docs/access?context=ac-sensitive-data-overview&family=zurich&ft:locale=en-US) and Sensitive Data Masking capability are being prepared for future deprecation. They will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&family=zurich&ft:locale=en-US).

-   Starting with the Zurich release, Microsoft LUIS is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Virtual Agent is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Virtual Agent is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Virtual Agent, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Virtual Agent and ServiceNow Otto panel. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   [Assistant Designer Asset library](https://www.servicenow.com/docs/access?context=vad-topics-page&family=zurich&ft:locale=en-US):
    -   View an updated UI for Virtual Agent Designer topics in the new Assistant Designer Asset library page.
    -   Navigate between Assistants, Asset library, and Analytics tabs in the Assistant Designer UI.
    -   Disconnect an LLM Assistant from a given asset with the Actions on Row icon \[Omitted image "image.kebab-menu"\] Alt text:in the Asset library.
    -   See descriptions of each LLM asset type when selecting **Create asset** in the Asset library.
    -   Read a tooltip that appears when you edit an LLM assistant under the Assistans tab and try to promote more than 6 topics associated with an LLM assistant.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Google Workspace chat now works with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.
-   Start the create flow for all supported conversational assets directly from Virtual Agent Designer.

 See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Virtual Agent and ServiceNow Otto panel. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   Prompts help users ask better questions and get more accurate answers. Admins can turn prompt library on or off and further configure the default recommended prompts for users.

 See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

