---
title: Virtual Agent release notes
description: The ServiceNow Virtual Agent application provides user assistance through a conversational interface to help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-27"
reading_time_minutes: 9
---

# Virtual Agent release notes

The ServiceNow® Virtual Agent application provides user assistance through a conversational interface to help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Australia release.

## Virtual Agent highlights for the Australia release

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Virtual Agent and ServiceNow Otto panel. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)

-   Prompts help users ask better questions and get more accurate answers. Admins can turn prompt library on or off and further configure the default recommended prompts for users.

See [Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent-landing-page.md) for more information.

## New in the Australia release

-   **[View Live Agent status updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)**

    Routing messages and section headers indicate when the live agent has entered and left the chat in premium chat conversations.


-   **[Switch between interactive views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)**

    In premium chat conversations, switch between multiple interactive views through the drop-down selector including Knowledge Base articles, catalog forms, org charts, and AI agent widgets.


-   **[Assign Model Context Protocol \(MCP\) servers to an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/assign-mcp-servers.md)**

    Admins can assign configured Model Context Protocol \(MCP\) servers to assistants. Role-based access can be configured for each assigned MCP server to control which users can access MCP-provided capabilities through the assistant.

-   **[Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/brand-assistant.md)**

    Enable estimated wait time for the next live agent. When enabled, users see the estimated wait time for the live agent in the chat menu item.

-   **[Enable additional chat features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/additional-chat-features.md)**

    Premium chat now supports uploading documents directly into a conversation.

-   **[Review chat assistant settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/review-assistant-settings.md)**

    The MCP servers section shows which users can access Model Context Protocol \(MCP\)-provided capabilities through the assistant.

-   **[ServiceNow® Otto for Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-sys-props.md)**

    Personalization is now shown by default.


-   **[Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/add-info-sources-assistant.md)**

    Premium chat prefills messages with legacy messages that were previously configured in your standard or enhanced chat experiences.

    By default, portals and mobile apps that have enhanced chat with a dynamic, movable, and resizable window use the assistant search profile for both portal/mobile search and the assistant search. Admins can now turn off this behavior and continue to use the portal/mobile search profile independently.

    The **Include AI Responses** column shows whether the search source is included in the synthesized response. Within Assistant Designer, the setting is read-only. However, it can be modified in AI Search Admin console.

-   **[Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-assistant-portal-channel.md)**

    Mobile custom apps support configuration of enhanced chat and premium chat display options, with availability dependent on the widget's current configuration.

-   **[Manage an assistant chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/manage-assistant-chat-experience.md)**

    If you configured legacy messages and legacy fallbacks, your premium messages and premium fallbacks are prefilled with what you had in your legacy messages and legacy fallbacks. In this release, closing topics, closing messages, and survey topic are now prefilled.

    Closing topic, closing message, and survey topic are available for standard, enhanced, and premium chat for Now Assist in Virtual Agent.

-   **[Edit a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/edit-assistant.md)**

    When editing an assistant with premium chat, create, edit, or delete prompts from the prompt library. Prompts help users ask better questions and get more accurate answers. Use the prompt library to manage prompts that users see in premium chat. Create your own prompts or use the default prompts.

-   **[Prompt library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-prompt-library.md)**

    Browse and select from promoted prompt templates or save your own custom prompts, eliminating the need to retype frequently-used prompts within your chats. Access your reusable templates instantly from the omnibar for faster, more consistent conversations.

-   **[View uploaded documents in interactive view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)**

    When in premium chat conversations, you can upload a document and view it in the interactive view.


-   **[Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/add-info-sources-assistant.md)**

    For premium chat, catalog items have improved fluidity; however, some of them are no longer conversational. They’ll open in a catalog form instead. This applies to Now Assist in Virtual Agent assistants and Now Assist panel – Platform assistant.

-   **[Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-assistant-portal-channel.md)**
    -   If your instance is eligible, you can opt into the premium chat experience. ServiceNow performs a set of readiness checks to see if your instance is eligible for premium chat. Premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they're doing.
    -   An alert is shown when the instance is eligible for premium chat or when there is a possible delay for premium chat to appear as an option on your instance.
    -   When editing the display experience of an existing portal or mobile widget, chat experience options depend on the existing configuration.
    -   For channels, select channels from the **Add channels** drop-down list that integrate with the assistant.
    -   For Microsoft Teams, edit the channel to toggle between standard and premium chat.
-   **[Display your assistant on Platform or ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-nap-assistant.md)**

    An alert is shown when the instance is eligible for premium chat or when there is a possible delay for premium chat to appear as an option on your instance.

-   **[Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/brand-assistant.md)**

    Customize an assistant’s tone, response length, and persona in the **Personalization** section when branding your assistant. By default, personalization is hidden.

    To enable personalization, set the appropriate values in the **sn\_nowassist\_va.assistant\_personalization** system property. For more information, see [ServiceNow® Otto for Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-sys-props.md).

-   **[Enable additional chat features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/additional-chat-features.md)**

    For Now Assist in Virtual Agent assistants, voice input is available for premium chat.

    For Now Assist panel – Platform assistant, voice input is available for standard, enhanced, and premium chat.

-   **[Manage an assistant chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/manage-assistant-chat-experience.md)**

    For premium chat, you can select a topic for fallback options.

    For premium messages, select the default greeting message, static greeting message, or select a custom topic. The static greeting message allows you to customize message.

    For premium chat, your premium messages and premium fallbacks are pre-filled with your legacy messages and legacy fallbacks.

-   **[Edit a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/edit-assistant.md)**

    View **All assets** to see the assets that are assigned to an assistant.

    There is no limit to the number of assets that can be promoted.

    If an active asset is promoted, and later is set to inactive, the asset is not shown in the **Discoverable**, **Visible**, and **Promoted** lists.

-   **[ServiceNow® Otto for Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-sys-props.md)**

    Use the **sn\_nowassist\_va.assistant\_personalization** system property to show or hide chat personalization when branding an assistant. Personalization determines the tone of the assistant, response length, and persona.

-   ****

    Manage the behavior of suggestions that users see when typing in the input box.

-   **[Post-chat surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)**

    Collect user feedback in premium chats through post-chat surveys that trigger on agent task completion instead of waiting for a chat-end event. When an agent completes a task in an agentic flow, the survey can surface based on a configured probability, enabling you to gather insights that were previously unavailable.


-   **[View assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/view-assistants.md)**

    If you have the **com.snc.ex\_ai\_portal** \(Employee Slate\) app installed, the default Employee Slate assistant is shown, and Employee Slate is mapped to it by default. The default Employee Slate assistant can be activated, deactivated, edited, and tested. It can’t be deleted.

-   **[Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-assistant-portal-channel.md)**

    The default Employee Slate assistant comes with premium chat. Premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they’re doing.

-   **[Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/brand-assistant.md)**

    For the default Employee Slate assistant, configure premium chat branding. Select and configure the chat header, chat logo, and chat menu items such as a phone number, email, and link.

    A **Channels** section is shown for Now Assist in Virtual Agent assistants and the default Employee Slate assistant if a channel is configured in the display experience.

-   **[Manage an assistant chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/manage-assistant-chat-experience.md)**

    Depending on your configuration, different greeting, closing, and fallback options may appear. Legacy messages \(chat messages\) and legacy fallbacks \(chat fallbacks\) are shown when at least one display experience has standard chat or enhanced chat. Premium messages and premium fallbacks are shown when at least one display experience has premium chat.

-   **[Test a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/test-assistant.md)**

    Test your chat assistant \(standard, enhanced, or premium chat\) to simulate an end-to-end conversation before moving your experience into a production environment.

-   **[Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/vad-topics-page.md)**

    Use the **Test Assistant** button to test your LLM assistant in Standard, Enhanced, and Premium Chat, after adding chat experiences in Assistant Designer's **Assistants** tab.

-   **[Now Assist in Virtual Agent on mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/now-assist-mobile-va.md)**

    Use the modified version of Now Assist in Virtual Agent on your mobile device. This redesigned version adapts to smaller screens without losing functionality or clarity.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Premium chat experience for Now Assist Panel - Platform \(default\) assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)**

    The Now Assist Panel - Platform \(default\) assistant now has the premium chat experience configured by default.


## UI changes

-   **[Refresh to the organization chart user interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)**

    The org chart's user interface was updated for premium chat in ServiceNow Otto for Virtual Agent and ServiceNow Otto panel.

-   **[Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/brand-assistant.md)**

    In **Assistant Designer** &gt; **Assistants** &gt; **Branding**, the standard chat and enhanced chat sections are condensed into one section.


-   **[Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/vad-topics-page.md): actions for this row icon**

    The tooltip for the **Discoverable** and **Visible** options now explains that Setup topics can't be discoverable or visible, as they aren't editable by users. The Live Agent topic is excepted.


## Changed in this release

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


## Activation information

Virtual Agent is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[Conversational Interfaces release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/conversational-interfaces-rn-landing.md)

