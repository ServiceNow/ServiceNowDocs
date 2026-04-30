---
title: Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience
description: Fine-tune your Virtual Agent settings and topics provided by the Virtual Agent Designer for the best voice chat experience with Alexa.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure Conversational Integration with Alexa, Integrating Virtual Agent with Alexa, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience

Fine-tune your Virtual Agent settings and topics provided by the Virtual Agent Designer for the best voice chat experience with Alexa.

-   Virtual Agent Designer is a diagram tool for creating and managing topics, which are blueprints for conversation between a Virtual Agent and a user. For more information, see [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).

    **Note:** Be sure that you specify Alexa as the applicable channel in the **Additional channel support** field if you want the topics that you designed using the Virtual Agent Designer to work on Alexa. For more information about the channel selection, see [Deploying Virtual Agent topics in other channels](va-integrations.md).

-   Bot messages help you to interact with Alexa. You can change the bot messages for interaction in a voice chat conversation. To access the bot messages, enter `sys_cs_provider_application.list` in the navigation filter and navigate to your Alexa application profile to find the bot messages.

    ![Provider Channel Identity settings window for Alexa, next to Alexa Provider Channel Identity window with Bot Messages highlighted.](../images/alexa-bot-messages.png "Bot messages for Alexa")

-   You can change the greeting message and other messages only for the voice channels using the Custom Greeting and Setup page. For example, you can create a custom topic, edit it, and assign it to be used if the end user is on a voice channel. For more information about accessing the Custom Chat and to change the greeting section of the message, see [Configure a Virtual Agent chat experience](../task/configure-default-chat-experience.md).

-   You can also change the system-generated messages by entering `sys_properties.list` in the navigation filter, and filter them by the criteria `com.glide.cs` to confirm that these messages work for voice channels. You can review the following key messages:

    -   com.glide.cs.topic\_picker\_msg
    -   com.glide.cs.no\_topic\_found\_message
    -   com.glide.cs.no\_topic\_sorry\_message
    -   com.glide.cs.link\_account\_msg
    -   com.glide.cs.topic\_choice\_list\_message
    -   com.glide.cs.topic\_confirmation\_message
    **Note:** Most of the messages unique to the voice channels are listed in the Bot Messages section of the Provider Channel Identity record.

    For more information, see [Change the Virtual Agent greeting messages in the Greeting setup topic](../task/va-welcome-topic-selection-msgs.md).

-   Most components work for screen-based and screen-less devices accessed in Alexa. However, some components are not compatible especially for the screen-less devices.

    **Note:** On the screen-based Alexa enabled devices, the presentation of cards and images has limitations as per the Alexa skill kit specification.

    The Conversational Integration with Alexa application supports the following user input controls in Virtual Agent Designer.

    **Note:** Conversational Integration with Alexa also supports touch input for screen-based devices.

<table id="table_kls_vnd_mqb"><thead><tr><th>

User input control

</th><th>

Description

</th><th>

Screen

</th><th>

No screen

</th></tr></thead><tbody><tr><td>

Text input/output

</td><td>

Text format that is validated when a user enters certain text items.

</td><td>

Yes.

</td><td>

Yes.

</td></tr><tr><td>

Static Choice

</td><td>

User selects an item from a predefined list.

</td><td>

Yes, touch scroll.

</td><td>

Yes, voice pagination.

</td></tr><tr><td>

Dynamic Choice

</td><td>

User selects a choice from the list of dynamically created choices.

</td><td>

Yes, no clicking links.

</td><td>

Yes, voice pagination.

</td></tr><tr><td>

Boolean

</td><td>

User enters a Boolean response to the bot. For example, the user can reply `Yes` or `No` in a chat conversation.

</td><td>

Yes.

</td><td>

Yes.

</td></tr><tr><td>

Date Time

</td><td>

User selects a calendar date, time \(hours and minutes\), or both.

</td><td>

Yes \(NLU recommended at the node\).

</td><td>

Yes \(NLU recommended at the node\).

</td></tr><tr><td>

File Picker

</td><td>

User sends a file to the bot.

</td><td>

No.

</td><td>

No.

</td></tr><tr><td>

Pause

</td><td>

Breaks the conversation with Alexa.

</td><td>

No.

</td><td>

No.

</td></tr><tr><td>

Carousel

</td><td>

User selects a single item from the carousel.

</td><td>

Yes, touch scroll.

</td><td>

Yes, reading labels.

</td></tr><tr><td>

Image/Link/HTML output

</td><td>

Bot sends an image, a link, or an HTML to the user.

</td><td>

Yes, no clicking links.

</td><td>

error\_msg

</td></tr><tr><td>

Video

</td><td>

User can choose a video card from the header card.

</td><td>

video\_screen\_device\_msg

</td><td>

video\_audio\_device\_msg

</td></tr><tr><td>

Card

</td><td>

Type of header card. Choose the contents:-   Large image with text
-   Small image with text
-   YouTube Video Card
The fields in the dialog box change based on your choice.

</td><td>

Yes, no clicking.

</td><td>

Yes, reading labels.

</td></tr><tr><td>

Table

</td><td>

If you selected Record as the **Reference Type**, select the table to be searched.

</td><td>

YesShows the table headers, followed by rows with column header: value pair, Speak \(Table header\). Please say Done to continue.

</td><td>

No, reading labels Unfortunately, I cannot show you the content on this device. Please say Done to continue.

</td></tr></tbody>
</table>    **Note:** To edit or change any of the following bot messages, enter sys\_cs\_provider\_application.list in the navigation filter of your ServiceNow instance, select **Alexa** &gt; **Bot Messages**, and click the name of the bot message that you want to edit.

    -   error\_msg
    -   video\_screen\_device\_msg
    -   video\_audio\_device\_msg
    -   table\_msg
    If you find the message name &lt;EMPTY&gt; and want to add a Boolean confirmation message to the end users, you can configure the bot message with the value \[0\] or \[1\].

-   Conversational Integration with Alexa supports contextual actions that serve an appropriate response from custom chat integrations when user input is mapped to them. For more information, see [Contextual actions for Alexa](../reference/alexa-contextual-actions.md).

