---
title: Video bot response control
description: Use the Video bot response control in a Virtual Agent topic to include a video in the conversation.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Virtual Agent, Video, bot response, control, node]
breadcrumb: [Virtual Agent Designer bot responses, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Video bot response control

Use the Video bot response control in a Virtual Agent topic to include a video in the conversation.

The Video bot response control includes a navigation button, which gives users time to watch the video. If you want the user to the watch the video before continuing with the conversation, use this navigation button.

When users have finished watching the video, they can select the navigation button to continue with the conversation.

**Note:** Topic authors can also use the [Card bot response control](va-card-output.md) to include a video in conversations. However, the Card bot response control doesn't include the navigation button, which gives users time to watch the video.

## Video bot response control properties

<table id="table_nff_y1b_3db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this video bot response control node in the topic flow.

</td></tr><tr><td>

Card type

</td><td>

Type of card. Select **YouTube Video Card**.**Note:** In the Yokohama release, only YouTube video cards are supported.

</td></tr><tr><td>

Template

</td><td>

A visual representation of the layout of the video included in the card.

</td></tr><tr><td>

Map data to fields on the card

</td><td>

Fields that correspond to the numbers shown on the template. These fields are the following:-   **Title**: Title of the card.
-   **Title Link**: URL to any relevant content.
-   **Description**: Description the card, such as the topic the video addresses.
-   **YouTube Video ID**: Unique identifier for the video used in the card. This identifier is the string following the equal sign \(=\) at the end of the video's URL path.

For example, in the path shown below, the video identifier is `FVgtjdEOa5M`.

![In the URL www.youtube.com/watch?v=FVgtjdEOa5M, the video identifier is FVgtjdEOa5M.](../images/va-video-unique-id.png)

![In this URL, the video identifier is the video ID in curly brackets.](../images/va-video-unique-id-2.png)


</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td>

Navigation button label

</td><td>

Navigation button used to continue with the conversation. By default, the button is labeled **Got it**, but you can change it. For example, you change the label to **Continue**.

 Users select this navigation button in the chat window to continue with the conversation.

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr><tr><td>

Node Conditions

</td><td>

Expression logic to specify a condition for presenting this topic to users. The condition must evaluate to true. You can set this field using either the condition builder or a script.

-   **Condition**: Use the condition builder to add or edit conditions.
-   **Script**: Use the script editor to create or edit a script that contains a condition statement.

</td></tr></tbody>
</table>## Channel support

**Note:** The way the Video bot response displays videos may vary across channels. For example, the video display you see in Slack messages may be different from what you see on Microsoft Teams or Workplace from Facebook. Also, if an embedded player is supported on that channel, the player is included in the display. For more information about channels, see the documentation for the channel you're using.

<table id="table_ttn_s5w_tsb"><thead><tr><th>

Channel

</th><th>

Support

</th><th>

Constraints

</th></tr></thead><tbody><tr><td>

Web UI

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Mobile UI

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Now Assist panel

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

Microsoft Teams

</td><td>

Supported

</td><td>

The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

</td></tr><tr><td>

Slack

</td><td>

Supported

</td><td>

Conversational Integration with Slack version 2.0.0 and later.The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

</td></tr><tr><td>

Workplace

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Facebook Messenger

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

SMS Twilio

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

LINE

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

WhatsApp

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

Apple Messages for Business

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

Alexa \(Voice\)

</td><td>

Not supported

</td><td>

Not applicable

</td></tr></tbody>
</table>## Example Video bot response control

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="id_irz_szc_54b"><thead><tr><th>

Response properties

</th><th>

Card output

</th></tr></thead><tbody><tr><td rowspan="2">

![Basic properties include the node name, card type, template, title, title link, description, and YouTube video ID.](../images/va-card-video-properties-2.png "Video bot response control basic properties")

</td><td>

![Video card with the header "Returning to work using Safe Workplace Suite," a description, and a "Continue" navigation button.](../images/va-video-with-nav-button-2.png "Video bot response output on the chat widget with the navigation button")

</td></tr><tr><td>

![Video card with the header, "Returning to work using Safe Workplace Suite" and a description.](../images/va-video-without-nav-button-2.png "Video bot response output on the chat widget without the navigation button")

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer bot responses](va-bot-responses.md)

