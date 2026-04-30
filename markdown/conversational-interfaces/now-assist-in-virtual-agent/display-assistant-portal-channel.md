---
title: Display your assistant on a portal or channel
description: Select at least one portal or integrate with your preferred messaging channels to display your assistant.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-04-22"
reading_time_minutes: 6
breadcrumb: [Configuring Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Display your assistant on a portal or channel

Select at least one portal or integrate with your preferred messaging channels to display your assistant.

## Before you begin

[Assign Now Assist skills to an assistant](assign-na-skills-assistant.md)

Role required: virtual\_agent\_admin or admin

## Procedure

1.  On the **Portals** tab, select one or more portals from the **Add Portal** drop-down list or integrate with your preferred messaging channels to display Virtual Agent.

    **Note:** For Now Assist panel assistants \(Platform and Developer\), there aren't any **Portals**, **Channels**, or **Mobile** tabs.

    -   For Now Assist panel assistant \(Platform\), select the **Unified Navigation app shell** link to test Now Assist panel assistant \(Platform\).
    -   For Now Assist panel assistant \(Developer\), select the **Studio** link to test Now Assist panel assistant \(Developer\).
    ![Display experience page shows where Virtual Agent is displayed, such as portals, channels, and mobile.](../image/NAinVA-portal-display-052025.png "Options for where Virtual Agent appears")

    One portal can only include one assistant. Any portal in the list that is already used is unavailable for selection.

    Natural Language Understanding \(NLU\)-based Virtual Agent doesn't coexist with Now Assist in Virtual Agent. They can coexist in the same instance, but not within the same portal.

    1.  Choose between the standard or enhanced chat experience, and then select **Add**. For more information, see [Standard chat](../concept/nava-standard-chat.md) and [Enhanced chat](../concept/nava-enhanced-chat.md).

        **Note:** If you're a new customer and haven't set up an assistant with a display experience, only the enhanced chat option is available.

        ![Select between standard chat or enhanced chat for your portal.](../image/NAinVA-standard-enhanced-052025.png "Standard or enhanced chat experience for your portal")

        If your portal has AI Search activated, enhanced chat includes the option to turn on the enhanced chat experience. Select **Allow the search bar to open into a full-page chat experience**. For more information about whether your portal meets the requirements to have users chat from search results, see [Portal prerequisites for enhanced chat](../concept/prerequisites-enhanced-chat.md).

        **Note:** When you activate enhanced chat in a portal, that portal uses the VA Search Profile instead of the search profile specified in the portal's search application configuration. To learn more about search profiles and how they affect search behavior, see [Search profiles in AI Search](https://www.servicenow.com/docs/access?context=defining-search-profiles-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

        For information about the enhanced chat experience option, see [Using Now Assist in Virtual Agent](../concept/using-now-assist-in-va.md).

        **Note:** Customer Service Management \(CSM\) portals don't have the full-page experience option.

        If the Now Assist Q&amp;A skill isn't enabled for the assistant, the enhanced chat experience is unavailable.

        If the portal has an NLU assistant enabled, the LLM assistant replaces it.

    2.  Select the ellipsis to remove a portal or edit settings to toggle between enhanced chat and standard chat.

        ![Ellipsis shows edit portal settings or remove a portal.](../image/NAinVA-edit-experience-052025.png "Edit experience or remove a portal")

    3.  Select the **Allow public access for this assistant** check box to enable Virtual Agent on public pages for all selected portals.

        Selecting the check box only makes the assistant response publicly available to guest users. In addition to selecting the check box, make sure that the UI page and standard chat are also public. For more information, see [Make UI pages public or private](https://www.servicenow.com/docs/access?context=t_MakeAPagePublic&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), [Configure page security by role](https://www.servicenow.com/docs/access?context=configure-page-security&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US), and [Configure widget security](https://www.servicenow.com/docs/access?context=configure-widget-security&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

        For public access across the entire instance, see **Conversational** &gt; **Interfaces** &gt; **Settings**.

    On the **Channels** tab, Now Assist in Virtual Agent integrates with these channels: Slack, Microsoft Teams, SMS with Twilio, WhatsApp, and Amazon Connect. If the plugins are already installed, the available channel cards aren't displayed. For more information on integrating Virtual Agent with messaging apps, see [Virtual Agent integration with messaging apps](../../virtual-agent/concept/va-integration-messaging-apps.md).

    ![List of channels to integrate with Virtual Agent.](../image/NAinVA-display-channels.png "Channels that integrate with Virtual Agent")

    Getting the plugin redirects you to the ServiceNow Store. After the plugins are installed and configured, you can then select the ones that you want the assistant to integrate with.

    In the **Mobile** tab, if no mobile app is selected to display standard chat or enhanced chat, users see the traditional NLU Virtual Agent in the mobile app. There are three different mobile app components that admins can integrate with an assistant: mobile search widget, chat launcher, and a custom app \(mobile SDK\).

    1.  To use Now Assist in Virtual Agent on your mobile app, download the Now Mobile App or Agent App and use Mobile App Builder to configure Virtual Agent in the app.

        If the application for mobile in the Now Assist Admin console is turned on, Now Assist large language model \(LLM\) is enabled in Virtual Agent for application on mobile.

        For information about mobile prerequisites, see [Mobile app prerequisites for enhanced chat](../concept/mobile-prereqs-enhanced-chat.md).

        Select a mobile search widget from the **Add search widget** drop-down list. The assistant must have the enhanced chat experience enabled.

        ![Drop-down list of mobile applications.](../image/NAinVA-mobile-builder-052025.png "Integrate your assistant with a mobile application")

        The **Add chat experience** pop-up window appears. Select a mobile search configuration, and then select **Add**.

        ![List of mobile search configurations for the assistant.](../image/NAinVA-mobile-search-widget-052025.png "Select a mobile search configuration for the assistant")

        The search widget configuration is added to the Search widget name list.

        In the **Chat launcher functions** drop-down list, select a function to open the assistant. Optionally, you can also select a mobile search configuration.

        ![List of optional mobile search configurations for the assistant.](../image/NAinVA-chat-launcher-052025.png "Select an optional mobile search configuration for the assistant")

        **Note:** Any prior Virtual Agent configurations that applied to the NOW mobile or Agent apps are migrated to apply to the chat launcher functions.

        The Add chat launcher function pop-up window appears. Select standard chat or enhanced chat, and then select **Add**.

        The **Custom apps section** is displayed when a mobile SDK plugin is installed. Select a custom mobile app integrated with the mobile SDK that launches this assistant.

        The Add custom app pop-up window appears. Select standard chat or enhanced chat, and then select **Add**.

    2.  Select the ellipsis to remove a mobile app or edit settings to toggle between the enhanced chat and standard chat experience, if standard chat is available to you.
2.  Select **Save and continue**.


## What to do next

[Add information sources to an assistant](add-info-sources-assistant.md).

