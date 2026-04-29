---
title: Display your chat assistant on a portal, channel, or mobile app
description: Select at least one portal, or integrate with your preferred messaging channels, to display your assistant. Display experiences are the different places where a user can find and interact with an assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Display your chat assistant on a portal, channel, or mobile app

Select at least one portal, or integrate with your preferred messaging channels, to display your assistant. Display experiences are the different places where a user can find and interact with an assistant.

## Before you begin

See [Add assets to a chat assistant](add-assets.md).

If you're using a display experience for a Now Assist panel assistant \(Platform or Developer\), see [Display your assistant on Platform or ServiceNow Studio](display-nap-assistant.md).

Role required: virtual\_agent\_admin or admin

## About this task

You must configure at least one display experience for an assistant before activation.

## Procedure

1.  In **Portals**, select one or more portals from the **Add Portal** drop-down list or integrate with your preferred messaging channels to display a chat assistant.

    ![Select a portal for where you want your assistant to appear.](../image/NAinVA-add-portal-122025.png "Options for where Virtual Agent appears")

    One portal can only include one assistant. Any portal in the list that is already used is unavailable for selection.

    Natural Language Understanding \(NLU\) and large language model \(LLM\) topic discovery cannot coexist in the same portal.

    1.  Choose between the standard or enhanced chat experience, and then select **Add**. For more information, see [Standard chat](../concept/nava-standard-chat.md) and [Enhanced chat](../concept/nava-enhanced-chat.md).

        **Note:** If you're a new customer and haven't set up an assistant with a display experience, only the enhanced chat option is available.

        ![Select between standard chat or enhanced chat for your portal.](../image/NAinVA-standard-enhanced-052025.png "Standard or enhanced chat experience for your portal")

        If your portal has AI Search activated, enhanced chat includes the option to turn on the full-page chat experience. Select **Allow the search bar to open into a full-page chat experience**. For more information about whether your portal meets the requirements to have users chat from search results, see [Portal prerequisites for enhanced chat](../concept/prerequisites-enhanced-chat.md).

        **Note:** When you activate enhanced chat in a portal or mobile app, that portal or mobile app uses the assistant search application configuration rather than the portal or mobile app's search application configuration. VA Search Profile instead of the search profile specified in the portal's search application configuration. To learn more about search profiles and how they affect search behavior, see [Search profiles in AI Search](https://www.servicenow.com/docs/access?context=defining-search-profiles-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

        For information about the enhanced chat experience option, see [Using Now Assist in Virtual Agent](../concept/using-now-assist-in-va.md).

        **Note:** Customer Service Management \(CSM\) portals don't have the enhanced chat option.

    2.  Select the ellipsis to remove a portal or edit settings to toggle between enhanced chat and standard chat.

        ![Ellipsis shows edit portal settings or remove a portal.](../image/NAinVA-remove-portal-122025.png "Edit experience or remove a portal")

    3.  Select the **Allow public access for this assistant** check box to enable the assistant on public pages for all selected portals.

        Selecting the check box only makes the assistant response available to guest users. In addition to selecting the check box, ensure that the UI page and chat client are also set to public. For more information, see [Make UI pages public or private](https://www.servicenow.com/docs/access?context=t_MakeAPagePublic&version=australia&pubname=australia-platform-security&ft:locale=en-US), [Configure page security by role](https://www.servicenow.com/docs/access?context=configure-page-security&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US), and [Configure widget security](https://www.servicenow.com/docs/access?context=configure-widget-security&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

        For public access across the entire instance, see **Conversational** &gt; **Interfaces** &gt; **Settings**.

2.  In **Channels**, select your preferred channels.

    Now Assist in Virtual Agent integrates with these channels: Slack, Microsoft Teams, Google chat, SMS with Twilio, WhatsApp, and Amazon Connect. If the plugins are already installed, the available channel cards aren't displayed. For more information on integrating Virtual Agent with messaging apps, see [Integrating Virtual Agent with messaging apps](../../virtual-agent/concept/va-integration-messaging-apps.md).

    ![List of channels to integrate with Virtual Agent.](../image/NAinVA-channels-122025.png "Channels that integrate with Virtual Agent")

    Getting the plugin redirects you to the ServiceNow Store. After the plugins are installed and configured, you can then select the ones that you want the assistant to integrate with.

3.  In **Mobile**, select a mobile app display experience.

    In the **Mobile** tab, if no mobile app is selected to display standard chat or enhanced chat, users see the traditional NLU Virtual Agent in the mobile app. There are different mobile app components that admins can display with an assistant: mobile search widget, chat launcher, prominent action button override, and a custom app \(mobile SDK\).

    1.  To use Now Assist in Virtual Agent on your mobile app, download the Now Mobile App or Agent App and use Mobile App Builder to configure Virtual Agent in the app. For information about mobile prerequisites, see [Mobile app prerequisites for enhanced chat](../concept/mobile-prereqs-enhanced-chat.md).
    2.  Select a mobile search widget from the **Add search widget** drop-down list. The assistant must have the enhanced chat experience enabled.

        ![Drop-down list of mobile applications.](../image/NAinVA-mobile-search-widget-122025.png "Integrate your assistant with a mobile application")

        The **Add chat experience** pop-up window appears.

        Select a mobile search configuration and select **Allow the search bar to open into a chat experience** if you want enhanced chat to launch directly from the mobile search bar. If you don't select the check box, synthesized responses on the standard search results page are shown. Select **Add**.

        ![List of mobile search configurations for the assistant.](../image/NAinVA-mobile-search-widget072025.png "Select a mobile search configuration for the assistant")

        The search widget configuration is added to the search widget name list.

    3.  In **Chat launcher functions**, select the drop-down menu to add a chat launcher function to open the assistant.

        The **Add chat experience** pop-up window appears where you can optionally select a mobile search configuration if you have enhanced chat. All new customers only have enhanced chat enabled. Selecting a mobile search configuration is not available for standard chat.

        ![List of optional mobile search configurations for the assistant.](../image/NAinVA-chat-launcher-072025.png "Select an optional mobile search configuration for the assistant")

        **Note:** Any prior Virtual Agent configurations that applied to the NOW mobile or Agent apps are migrated to apply to the chat launcher functions.

    4.  In **Prominent action button override**, select from the **Add tab override** drop-down menu to allow a prominent action button to launch the assistant when it's opened from the selected mobile navigation tab. This overrides what’s been defined in the chat launcher function from any other assistant record.

        The default setting for the chat launcher function associated with a prominent action button should still be configured in the chat launcher functions. If there is no record in the chat launcher function, the override won’t work.

        The same chat experience must be used to override the same prominent action button. For example, if the chat launcher section is configured to be enhanced chat, only an override record for enhanced chat would work.

        ![Prominent action button override.](../image/NAinVA-prominent-action-override-122025.png "Prominent action button override")

        The **Add chat experience** pop-up window appears where you can optionally select a mobile search configuration. For more information, see  and .

    5.  The **Custom apps section** is displayed when a mobile SDK plugin is installed. Select a custom mobile app integrated with the mobile SDK that launches this assistant.

        The **Add custom app** pop-up window appears. Select standard chat or enhanced chat.

4.  Select the ellipsis to remove a mobile app or edit settings to toggle between the enhanced chat and standard chat experience, if standard chat is available to you.

5.  Select **Save and continue**.


## What to do next

See [Brand an assistant](brand-assistant.md).

