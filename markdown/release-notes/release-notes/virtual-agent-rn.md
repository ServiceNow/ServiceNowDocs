---
title: Virtual Agent release notes
description: The ServiceNow Virtual Agent application provides user assistance through a conversational interface to help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-27"
reading_time_minutes: 4
---

# Virtual Agent release notes

The ServiceNow® Virtual Agent application provides user assistance through a conversational interface to help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Australia release.

## New in the Australia release

-   ****
-   **[Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/add-info-sources-assistant.md)**

    For premium chat, catalog items have improved fluidity; however, some of them are no longer conversational. They’ll open in a catalog form instead. This applies to Now Assist in Virtual Agent assistants and Now Assist panel – Platform assistant.

-   **[Display your chat assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-assistant-portal-channel.md)**
    -   If your instance is eligible, you can opt into the premium chat experience. ServiceNow performs a set of readiness checks to see if your instance is eligible for premium chat. Premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they're doing.
    -   An alert is shown when the instance is eligible for premium chat or when there is a possible delay for premium chat to appear as an option on your instance.
    -   When editing the display experience of an existing portal or mobile widget, chat experience options depend on the existing configuration.
    -   For channels, select channels from the **Add channels** drop-down list that integrate with the assistant.
    -   For Microsoft Teams, edit the channel to toggle between standard and premium chat.
-   **[Display your assistant on Platform or ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-nap-assistant.md)**

    An alert is shown when the instance is eligible for premium chat or when there is a possible delay for premium chat to appear as an option on your instance.

-   **[Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/brand-assistant.md)**

    Customize an assistant’s tone, response length, and persona in the **Personalization** section when branding your assistant. By default, personalization is hidden.

    To enable personalization, set the appropriate values in the **sn\_nowassist\_va.assistant\_personalization** system property. For more information, see [Now Assist in Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-sys-props.md).

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

-   **[Now Assist in Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-sys-props.md)**

    Use the **sn\_nowassist\_va.assistant\_personalization** system property to show or hide chat personalization when branding an assistant. Personalization determines the tone of the assistant, response length, and persona.

-   **[Now Assist deployment configuration properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/deployment-config-attributes.md)**

    Manage the behavior of suggestions that users see when typing in the input box.


-   **[View assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/view-assistants.md)**

    If you have the **com.snc.ex\_ai\_portal** \(Employee Slate\) app installed, the default Employee Slate assistant is shown, and Employee Slate is mapped to it by default. The default Employee Slate assistant can be activated, deactivated, edited, and tested. It can’t be deleted.

-   **[Display your chat assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-assistant-portal-channel.md)**

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

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Premium chat experience for Now Assist Panel - Platform \(default\) assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)**

    The Now Assist Panel - Platform \(default\) assistant now has the premium chat experience configured by default.


## Activation information

Virtual Agent is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[Conversational Interfaces release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/conversational-interfaces-rn-landing.md)

