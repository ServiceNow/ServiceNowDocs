---
title: HTML bot response control
description: Use the HTML bot response control to display static HTML text in the Virtual Agent bot response.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Virtual Agent, designer, HTML, bot, response, control]
breadcrumb: [Virtual Agent Designer bot responses, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# HTML bot response control

Use the HTML bot response control to display static HTML text in the Virtual Agent bot response.

**Note:** If you created conversations in earlier releases that use this bot response control to generate card layouts, consider updating your conversations to use the [Card bot response control](va-card-output.md). The Card displays information from a record in your instance and contains a link to that related record.

## Security considerations for HTML markup

For security reasons, an HTML sanitizer script runs automatically and checks all HTML markup used in the instance, including Virtual Agent conversations. The sanitizer script removes elements or attributes that might enable cross-site scripting attacks. You can edit the HTML sanitizer script to change the list of markup items to be preserved or removed. For details, see [HTML sanitizer](https://www.servicenow.com/docs/access?context=c_HTMLSanitizer&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US). For examples of adding markup items to the exclusion or inclusion lists, see [Configure HTML sanitizer](https://www.servicenow.com/docs/access?context=t_ConfigureHTMLSanitizer&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

To disable the HTML sanitizer script only for Virtual Agent conversations, add the **com.glide.cs.html.sanitizer.enabled** system property and set the value to false. For details about creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

## HTML bot response control properties

<table id="table_il2_n2r_sdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this HTML bot response control node in the topic flow.

</td></tr><tr><td>

HTML message

</td><td>

HTML output to be displayed. Select the Script icon ![Script icon.](../images/icon-script.png) to open the HTML editor and enter the HTML text.

</td></tr><tr><td>

Height \(Pixel\)

</td><td>

Maximum height of the area for displaying HTML output in third-party messaging applications.

</td></tr><tr><td>

Width \(Pixel\)

</td><td>

Maximum width of the bot bubble for displaying HTML output in third-party messaging applications.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Channel support

**Note:** As shown in the examples, HTML output can vary in third-party messaging applications. Determine an appropriate **Height** and **Width** area by setting initial height and width values, previewing the HTML output in the messaging applications you intend to use, and then adjusting the height and width values.

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Supported|None|
|Microsoft Teams|Supported|Since HTML is rendered as an image in Microsoft Teams, other controls are recommended. For example, use images or cards instead of HTML for Microsoft Teams.|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Not supported|Not applicable|
|SMS Twilio|Not supported|Not applicable|
|LINE|Not supported|Not applicable|
|WhatsApp|Not supported|Not applicable|
|Apple Messages for Business|Not supported|Not applicable|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For nonscreen devices, the user receives a message: `We found a link`. For details, see [Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](../concept/va-settings-for-alexa.md).|

## Example HTML bot response output

The HTML bot response shows a static HTML as a chat response. This example includes an image, headings, and paragraph text. The web UI presents this content as HTML. The Slack, Microsoft Teams, and Workplace user interfaces display the same content as a PNG image. URL links within the HTML are extracted and displayed below the image. The URL can be either an absolute or a relative link. If you use a relative link, it must be relative to the ServiceNow instance.

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

HTML bot response properties

</th><th>

HTML bot response output

</th></tr></thead><tbody><tr><td>

![Basic properties include the node name, HTML message, height, and width.](../images/va-html-properties.png "HTML bot response control basic properties")

</td><td>

![A chat window shows the company logo with a header, subheader, and body text.](../../notification/image/va-html-native.png "Web UI HTML output")

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer bot responses](va-bot-responses.md)

