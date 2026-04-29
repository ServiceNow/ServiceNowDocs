---
title: Manage an assistant chat experience
description: Manage the chat experience of your assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Manage an assistant chat experience

Manage the chat experience of your assistant.

## Before you begin

See [Brand an assistant](brand-assistant.md).

Role required: virtual\_agent\_admin or admin

## About this task

Define your greeting, closing messages and fallback options. A standard chat preview pane is shown for the default greeting topic and the default closing topic. Selecting custom topics won't show a preview pane.

Fallbacks are shown in the preview pane when you toggle on each or all fallbacks.

**Note:** Fallbacks aren't supported for Now Assist - Developer assistant.

## Procedure

1.  Select the **Chat experience** page.

2.  In the **Messages** section, set up your greeting topic, closing topic, error topic, and survey.

    ![Greeting message screen.](../image/NAinVA-messages-122025.png "Set up the assistant messages")

    Selecting a default topic shows its corresponding default message. You can also create your own topic from **All** &gt; **Assistant Designer** &gt; **Asset Library**, and use it as the greeting or closing topic. When selecting a custom topic, the message field isn’t shown in the preview pane.

    Closing message only appears if you have a display experience with standard chat.

    ![Closing topic and closing message for the standard chat experience.](../image/NAinVA-closing-message-122025.png "Standard chat closing message")

    **Note:** Configuration options differ between different assistant types and display experiences.

<table id="table_vx4_nhh_zfc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Available in Now Assist in Virtual Agent assistants

</th><th>

Available in Now Assist panel - Platform assistant

</th><th>

Available in Now Assist panel - Developer assistant

</th></tr></thead><tbody><tr><td>

Greeting topic

</td><td>

Now Assist - Greeting is the default greeting topic for Now Assist in Virtual Agent assistants.Now Assist Panel - Greeting is the default greeting topic for Now Assist panel assistants.

Select a custom greeting if you want to replace the default greeting topic.

</td><td>

Yes

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

</td></tr><tr><td>

Error topic

</td><td>

Now Assist - Error is the default topic for Now Assist in Virtual Agent assistants.Now Assist Panel - Error is the default topic for Now Assist panel assistants.

To replace the default topic, select a custom topic from the drop-down menu.

</td><td>

Yes

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

</td></tr><tr><td>

Survey

</td><td>

You can optionally select a custom topic to use it as a survey topic. If you don't select any topic, the default survey experience is applied.

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td></tr></tbody>
</table>3.  In the **Fallback** section, activate one or more fallback options.

    ![Activate fallback options.](../image/NAinVA-fallback-122025.png "Activate fallback options")

    **Note:** For Now Assist panel - Platform assistant, web search, record producer, and custom fallback are available options. End this chat and survey are available for the standard chat experience.

    Examples for when you might want to select more than one fallback option:

    -   To transfer a user to a live agent while also creating an incident record.
    -   To end a conversation while creating an incident report.
    -   To use a custom topic while having the live agent transfer option.
    1.  Route the user to an available agent by turning on **Live agent**. Selecting the **Live agent topic** field displays a drop-down for topics, and the text input is used for the fallback button in the assistant. The default **Live agent topic** is **Now Assist Live Agent**.The default button label is **Request a live chat**.

        **Note:** If your instance doesn't have Live Agent configured, the **Live Agent** fallback option is unavailable. To configure Live agent, select the **Configure** link and navigate to **CI Admin console** &gt; **Settings** &gt; **Agent chat** tab. Use the default Now Assist Live Agent topic or select a topic.

    2.  Provide the user with web search results by turning on **Web search**. The web search option is useful when the synthesized response can't generate answers. The **Web search** check box displays a text input that is used for the name of the fallback button in the assistant. The default button label is **Search the web**. The default web search provider is Google Gemini.

        **Warning:** Certain API features that process data via third-party providers may route traffic to a datacenter outside of your region or location for these API features. See [KB2596322](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2596322) for a list of third-party APIs. Please consider your organization's data policies before using this feature.

        If the instance is self-hosted or regulated, the warning message won't be shown.

    3.  Direct the user to a record producer catalog item to create an incident or a case by turning on **Record producer**.

        A **Record producer catalog item** field check box displays a drop-down where you can select a catalog item. The default record producer catalog item is **Create a generic ticket**. The button label default is **Create a generic ticket**.

    4.  End the chat between the user and the assistant by turning on **End this chat**. End this chat is a fallback option for the standard chat experience. For the enhanced chat experience, conversations don't end. The text input is used for the fallback button in the assistant, and the default text input is **End this chat**. The button label default is **End this chat**.
    5.  Select a topic from the **Custom fallback topic** field by turning on **Custom fallback**. There isn't a default topic. The text input is used for the fallback button in the assistant. The default text input is **Custom fallback button**.
    For more information about fallback options, see [Enhanced chat](../concept/nava-enhanced-chat.md).

4.  Select **Save and continue**.


## What to do next

See [Enable additional chat features](additional-chat-features.md).

