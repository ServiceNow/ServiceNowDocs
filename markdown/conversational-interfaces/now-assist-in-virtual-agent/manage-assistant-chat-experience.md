---
title: Manage an assistant chat experience
description: Manage the chat experience of your assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 6
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Manage an assistant chat experience

Manage the chat experience of your assistant.

## Before you begin

See [Enable additional chat features](additional-chat-features.md).

Role required: virtual\_agent\_admin or admin

## About this task

Define your greeting, closing messages and fallback options.

Depending on your configuration, different options may appear. Legacy messages \(chat messages\) and legacy fallbacks \(chat fallbacks\) are shown when at least one display experience has standard chat or enhanced chat. Premium messages and premium fallbacks are shown when at least one display experience has premium chat.

A standard chat preview pane is shown for the default greeting topic and the default closing topic. Selecting custom topics won't show a preview pane.

Fallbacks appear in the preview pane when you toggle individual or all fallbacks on.

**Note:** Fallbacks aren't supported for Now Assist - Developer assistant.

## Procedure

1.  Select the **Chat experience** page.

2.  In the **Legacy messages** or the **Premium messages** section, set up your messages.

    ![Greeting message screen.](../image/NAinVA-chat-experience-legacy-messages-0426.png "Set up Now Assist in Virtual Agent assistant legacy messages")

    ![Greeting message screen.](../image/NAinVA-chat-experience--nap-premium-messages-0426.png "Set up Now Assist panel - Platform assistant premium messages")

    Selecting a default topic shows its corresponding default message. You can also create your own topic from **All** &gt; **Assistant Designer** &gt; **Asset Library**, and use it as the greeting or closing topic. When selecting a custom topic, the message field isn’t shown in the preview pane.

    Closing message only appears if you have a display experience with standard chat.

    ![Closing topic and closing message for the standard chat experience.](../image/NAinVA-closing-message-122025.png "Standard chat closing message")

    **Note:** Configuration options differ between different assistant types and display experiences.

<table id="table_vx4_nhh_zfc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Now Assist in Virtual Agent assistant

</th><th>

Employee Slate assistant

</th><th>

Now Assist panel - Platform assistant

</th><th>

Now Assist panel - Developer assistant

</th></tr></thead><tbody><tr><td>

Greeting topic

</td><td>

Now Assist - Greeting is the default greeting topic for Now Assist in Virtual Agent assistants.Now Assist Panel - Greeting is the default greeting topic for Now Assist panel assistants.

Select a custom greeting if you want to replace the default greeting topic.

</td><td>

Yes

</td><td>

You can use the default greeting message or contact Support to create your own greeting source.

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Greeting message

</td><td>

If the default greeting topic is used, the default greeting message is shown.If a custom greeting topic is selected, the **Greeting message** field doesn't appear.

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Closing topic

</td><td>

The closing topic is only applicable for the standard chat experience.Now Assist - Closing is the default closing topic. To replace it, select a topic from the drop-down menu.

</td><td>

Yes \(only for standard chat\)

</td><td>

No

</td><td>

No

</td><td>

No

</td></tr><tr><td>

Closing message

</td><td>

**Closing message** field is shown and used if the default Now Assist - Closing topic is selected.If a custom topic is selected, the **Closing message** field isn't shown.

</td><td>

Yes \(only for standard chat\)

</td><td>

No

</td><td>

No

</td><td>

No

</td></tr><tr><td>

Error topic

</td><td>

Now Assist - Error is the default topic for Now Assist in Virtual Agent assistants.Now Assist Panel - Error is the default topic for Now Assist panel assistants.

To replace the default topic, select a custom topic from the drop-down menu.

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Error message

</td><td>

If the default Now Assist - Error topic is used, the default Error message is used.If a custom topic is used, the error message field isn't shown.

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Survey

</td><td>

You can optionally select a custom topic to use it as a survey topic. If you don't select any topic, the default survey experience is applied.

 Feedback surveys are supported in both the standard and enhanced chat experiences. When enhanced chat is enabled, the survey is automatically triggered when the user indicates that they are finished chatting, based on the assistant's survey configuration.

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td><td>

No

</td></tr></tbody>
</table>3.  In the **Legacy fallbacks** or **Premium fallbacks** sections, activate one or more fallback options.

    **Note:** For premium fallbacks, web search fallback is dependent on your web search mode setting in [Enable additional chat features](additional-chat-features.md). If web search mode is turned off, web search fallback is unavailable \(grayed out\). If web search mode is turned on, web search fallback is available where you can turn it on or off.

    ![Activate fallback options.](../image/NAinVA-chat-experience-legacy-fallbacks-0426.png "Activate Now Assist in Virtual Agent legacy fallback options")

    ![Activate fallback options.](../image/NAinVA-chat-experience-nap-premium-fallbacks-0426.png "Activate Now Assist panel - Platform assistant premium fallback options")

    **Note:** For Now Assist panel - Platform assistant, web search, record producer, and custom fallback are available options. End this chat and survey are available for the standard chat experience.

    Live agent is not an available option.

    Examples for when you might want to select more than one fallback option:

    -   To transfer a user to a live agent while also creating an incident record.
    -   To end a conversation while creating an incident report.
    -   To use a custom topic while having the live agent transfer option.
    1.  Route the user to an available agent by turning on **Live agent**. Selecting the **Live agent topic** field displays a drop-down for topics, and the text input is used for the fallback button in the assistant. The default **Live agent topic** is **Now Assist Live Agent**.The default button label is **Request a live chat**.

        **Note:** To customize premium fallbacks for premium chat, contact Support.

        If your instance doesn't have Live Agent configured, the **Live Agent** fallback option is unavailable. To configure Live agent, select the **Configure** link and navigate to **CI Admin console** &gt; **Settings** &gt; **Agent chat** tab. Use the default Now Assist Live Agent topic or select a topic.

    2.  Provide the user with web search results by turning on **Web search**. The web search option is useful when the synthesized response can't generate answers. The **Web search** check box displays a text input that is used for the name of the fallback button in the assistant. The default button label is **Search the web**. The default web search provider is Google Gemini.

        **Warning:** Certain API features that process data via third-party providers may route traffic to a datacenter outside of your region or location for these API features. See [KB2596322](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2596322) for a list of third-party APIs. Please consider your organization's data policies before using this feature.

        If the instance is self-hosted or regulated, the warning message won't be shown.

        **Note:** For the premium chat experience, web search fallback requires web search mode to be turned on. To ensure that web search mode is turned on, see [Enable additional chat features](additional-chat-features.md).

    3.  Direct the user to a record producer catalog item to create an incident or a case by turning on **Record producer**.

        A **Record producer catalog item** field check box displays a drop-down where you can select a catalog item. The default record producer catalog item is **Create a generic ticket**. The button label default is **Create a generic ticket**.

        **Note:** By default, Create a generic ticket is enabled for record producer premium fallbacks. If you want to customize your own record producer fallback, select an agentic catalog item from the drop-down list.

    4.  End the chat between the user and the assistant by turning on **End this chat**. End this chat is a fallback option for the standard chat experience. For the enhanced chat experience, conversations don't end. The text input is used for the fallback button in the assistant, and the default text input is **End this chat**. The button label default is **End this chat**.
    5.  Select a topic from the **Custom fallback topic** field by turning on **Custom fallback**. There isn't a default topic. The text input is used for the fallback button in the assistant. The default text input is **Custom fallback button**.

        **Note:** There is no default custom premium fallbacks. To customize premium fallbacks, contact Support.

    For more information about fallback options, see [Enhanced chat](../concept/nava-enhanced-chat.md).

4.  Select **Save and continue**.


## What to do next

See [Review chat assistant settings](review-assistant-settings.md).

