---
title: Display your chat assistant on a portal, channel, or mobile app
description: Select a display experience for your chat assistant. Display experiences are the different places where a user can find and interact with an assistant. Select from a list of portals, messaging channels, and mobile app. To activate an assistant, at least one display experience must be configured.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-05-14"
reading_time_minutes: 11
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Display your chat assistant on a portal, channel, or mobile app

Select a display experience for your chat assistant. Display experiences are the different places where a user can find and interact with an assistant. Select from a list of portals, messaging channels, and mobile app. To activate an assistant, at least one display experience must be configured.

## Before you begin

See [Add assets to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-assets.md).

If you're using a display experience for a Now Assist panel assistant \(Platform or Developer\), see [Display your assistant on Platform or ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/display-nap-assistant.md).

Role required: virtual\_agent\_admin or admin

## About this task

The chat experience configuration defines how users interact with an assistant during a conversation, including message behavior, response generation, and fallback handling.

-   Standard chat is a condensed conversational support experience in a chat widget.
-   Enhanced chat is a conversational experience that includes a dynamic, movable, and resizable chat window, plus access to multiple active conversations.
-   Premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they’re doing.

If your instance is eligible, you can opt into the premium chat experience. ServiceNow performs a set of readiness checks to see if your instance is eligible for premium chat. The default chat experience is enhanced chat. However, if you also previously had standard chat enabled, you still have that as an option.

An alert is shown when:

-   The instance is eligible for premium chat.
-   There is a possible delay for premium chat to appear as an option on your instance.

**Note:** Remember to refresh your browser to view the option to opt in to the premium chat experience.

If your instance doesn’t meet the requirements for premium chat, you can continue using your existing standard or enhanced chat experience.

Premium chat is not available for instances in regulated markets \(Government Cloud Community\), instances that use domain separation, or regional data routing.

In premium chat, catalog items have improved fluidity, but some will no longer be conversational. They’ll open in a catalog form instead. For more information, see .

## Procedure

1.  In **Portals**, select one or more portals from the **Add Portal** drop-down list.

    **Note:** If you have access to the default Employee Slate assistant, Employee Slate is available from within the portal list. Selecting Employee Slate prompts you to add premium chat.

    -   Standard chat and enhanced chat are not options for Employee Slate.
    -   Employee Slate can be removed/unmapped from the default Employee Slate assistant and added to any Now Assist in Virtual Agent assistant.
    \[Omitted image "NAinVA-display-exp-052026.png"\] Alt text: Select a portal for where you want your assistant to appear.

    One portal can only include one assistant. Any portal in the list that is already used is unavailable for selection.

    Natural Language Understanding \(NLU\) and large language model \(LLM\) topic discovery cannot coexist in the same portal.

    1.  Choose between the standard/enhanced or premium chat experience, and then select **Add**. For more information, see [Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-standard-chat.md), [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md), or [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.md).

        \[Omitted image "NAinVA-display-premium-062026.png"\] Alt text: Opt into premium chat for your portal.

        When adding a new assistant into a portal, the chat experience options are:

        -   Enhanced chat with a dynamic, movable, and resizable chat window.
        -   Enhanced chat with the option to allow the search bar to open into a full-page chat experience.
        -   Premium chat opens the search bar into a full-page chat experience.
        If your portal has AI Search activated, enhanced chat includes the option to turn on the full-page chat experience. Select **Allow the search bar to open into a full-page chat experience**. Premium chat comes with the full-page chat experience.

        For more information about whether your portal meets the requirements to have users chat from search results, see [Portal prerequisites for enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/prerequisites-enhanced-chat.md).

        **Note:** When you activate enhanced chat in a portal or mobile app, that portal or mobile app uses the assistant search application configuration rather than the portal or mobile app's search application configuration. This ensures that the portal/mobile app's search results and assistant provide consistent responses. To learn more about search profiles and how they affect search behavior, see [Search profiles in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/defining-search-profiles-ais.md).

        Your display experience options depend on the configuration.

        -   If you’re using standard chat, your chat experience options are:
            -   Remain with standard chat.
            -   Enhanced chat with a dynamic, movable, and resizable chat window.
            -   Enhanced chat with the option to allow the search bar to open into a full-page chat experience.
            -   Premium chat that opens the search bar into a full-page chat experience.
        -   If you’re using enhanced chat with a dynamic, movable, and resizable chat window, your chat experience options are:
            -   Remain with enhanced chat with a dynamic, movable, and resizable chat window.
            -   Enhanced chat with the option to allow the search bar to open into a full-page chat experience.
            -   Premium chat that opens the search bar into a full-page chat experience.
        -   For portals that do not have AI search enabled, you can choose between standard chat and enhanced chat with a dynamic, movable, and resizable chat window.
        Enhanced chat \(full-page experience\) and premium chat \(full-page experience\) are supported for default Customer Service Management \(CSM\) portals such as Business Portal, CSM Portal, and Consumer Service Portal \(CSP\). CSM portals must have AI Search enabled. Enhanced chat is the default when an assistant is added to a default CSM portal.

        For premium chat, your premium messages and premium fallbacks are prefilled with what you had in your legacy messages and legacy fallbacks. Review the settings to ensure that everything was prefilled correctly.

        For information about the enhanced chat experience option, see [Using Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/using-now-assist-in-va.md).

    2.  Select the ellipsis to remove a portal or edit settings to toggle between chat experiences.

        \[Omitted image "NAinVA-remove-portal-122025.png"\] Alt text: Ellipsis shows edit portal settings or remove a portal.

    3.  Select the **Allow public access for this assistant** check box to enable the assistant on public pages for all selected portals.

        Selecting the check box only makes the assistant response available to guest users. In addition to selecting the check box, ensure that the UI page and chat client are also set to public. For more information, see [Make UI pages public or private](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_MakeAPagePublic.md), [Configure page security by role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-page-security.md), and [Configure widget security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-widget-security.md).

        For public access across the entire instance, see **Conversational** &gt; **Interfaces** &gt; **Settings**.

2.  In **Channels**, select your preferred messaging channels to display a chat assistant.

    Now Assist in Virtual Agent integrates with these channels: Slack, Microsoft Teams, Google Chat, SMS with Twilio, WhatsApp, and Amazon Connect. If the plugins are already installed, the available channel cards aren't displayed. For more information on integrating Virtual Agent with messaging apps, see [Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-integration-messaging-apps.md).

    Getting the plugin redirects you to the ServiceNow Store. After the plugins are installed and configured, you can then select the ones that you want the assistant to integrate with.

    -   After the plugins are installed and configured, choose the ones that you want the assistant to integrate with by selecting from the Add channel drop down menu.

        \[Omitted image "NAinVA-display-channels-062026.png"\] Alt text: List of channels to integrate with Virtual Agent.

    -   Select the ellipsis to remove a channel. The edit option is only available for Microsoft Teams. You can toggle between standard and premium chat.
        -   For standard chat, conversations in Microsoft Teams display responses using adaptive, in-context cards.
        -   For premium chat, conversations in Microsoft Teams display text-based responses for a faster, more conversational experience.
3.  In **Mobile**, select a mobile app display experience.

    In the **Mobile** tab, if no mobile app is selected to display standard chat or enhanced chat, users see the traditional NLU Virtual Agent in the mobile app. There are different mobile app components that admins can display with an assistant: mobile search widget, chat launcher, prominent action button override, and a custom app \(mobile SDK\).

    The table shows the chat experiences that are available when you edit the display experience of an existing mobile widget or if you're adding an assistant to a new mobile widget. When editing a display experience of an existing mobile widget, the chat experience options are dependent on the existing configuration.

<table id="table_bx3_bh3_njc"><thead><tr><th>

Mobile widget

</th><th>

Edit chat experience options

</th><th>

Add chat experience options

</th><th>

Mobile search configuration

</th></tr></thead><tbody><tr><td>

Mobile search widgets

</td><td>

Currently on enhanced chat with a dynamic, movable, and resizable window or full-page experience, your option is premium full-page experience.

</td><td>

-   Enhanced chat with a dynamic, movable, and resizable window.
-   Enhanced chat with full-page experience.
-   Premium chat with full-page experience.


</td><td>

Required

</td></tr><tr><td>

Chat launcher functions

</td><td>

Currently on standard chat, your options are enhanced chat full-page experience or premium chat full-page experience. Currently on enhanced chat, your option is premium chat full-page experience.

</td><td>

-   Enhanced chat with full-page experience.
-   Premium chat with full-page experience.


</td><td>

Optional

</td></tr><tr><td>

Prominent action button override

</td><td>

Currently on standard chat, your options are enhanced chat full-page experience or premium chat full-page experience. Currently on enhanced chat, your option is premium chat full-page experience.

</td><td>

-   Enhanced chat with full-page experience.
-   Premium chat with full-page experience.


</td><td>

Optional

</td></tr><tr><td>

Custom apps

</td><td>

Currently on standard chat, your options are enhanced chat full-page experience or premium chat full-page experience. Currently on enhanced chat, your option is premium chat full-page experience.

</td><td>

-   Enhanced chat with full-page experience.
-   Premium chat option is not available.


</td><td>

Not applicable

</td></tr></tbody>
</table>    1.  To use Now Assist in Virtual Agent on your mobile app, download the Now Mobile App or Agent App and use Mobile App Builder to configure Virtual Agent in the app. For information about mobile prerequisites, see [Mobile app prerequisites for enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/mobile-prereqs-enhanced-chat.md).
    2.  Select a mobile search widget from the **Add search widget** drop-down list. The assistant must have the enhanced chat or the premium chat experience enabled.

        \[Omitted image "NAinVA-mobile-search-widget-122025.png"\] Alt text: Drop-down list of mobile applications.

        The **Add chat experience** pop-up window appears.

        \[Omitted image "NAinVA-display-mobile-premium-062026.png"\] Alt text: Choose a chat experience. \[Omitted image ""\] Alt text: Select a chat experience and mobile search configuration.

        Select a chat experience and a mobile search configuration. Select**Add**.

        The search widget configuration is added to the search widget name list.

    3.  In **Chat launcher functions**, select the drop-down menu to add a chat launcher function to open the assistant.

        The **Add chat experience** pop-up window appears where you can optionally select a mobile search configuration if you have enhanced chat or premium chat.

        **Note:** Any prior Virtual Agent configurations that applied to the NOW mobile or Agent apps are migrated to apply to the chat launcher functions.

    4.  In **Prominent action button override**, select from the **Add tab override** drop-down menu to allow a prominent action button to launch the assistant when it's opened from the selected mobile navigation tab. This overrides what’s been defined in the chat launcher function from any other assistant record.

        The default setting for the chat launcher function associated with a prominent action button should still be configured in the chat launcher functions. If there is no record in the chat launcher function, the override won’t work.

        The same chat experience must be used to override the same prominent action button. For example, if the chat launcher section is configured to be enhanced chat, only an override record for enhanced chat would work.

        \[Omitted image "NAinVA-prominent-action-override-122025.png"\] Alt text: Prominent action button override.

        The **Add chat experience** pop-up window appears where you can optionally select a mobile search configuration. For more information, see [Using the prominent action button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/using-prominent-action-button.md) and [Configuring a prominent action button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/configuring-prominent-action-button.md).

    5.  The **Custom apps section** is displayed when a mobile SDK plugin is installed. Select a custom mobile app integrated with the mobile SDK that launches this assistant.

        The **Add custom app** pop-up window appears. Select standard chat or enhanced chat.

4.  Select the ellipsis to remove a mobile app or edit settings to toggle between the enhanced chat and standard chat experience, if standard chat is available to you.

5.  Select **Save and continue**.


## What to do next

See [Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/brand-assistant.md).

