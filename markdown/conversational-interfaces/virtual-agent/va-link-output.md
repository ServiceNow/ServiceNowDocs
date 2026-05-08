---
title: Link bot response control
description: Use the Link bot response control in a Virtual Agent topic to present a bot response. The response contains a header prompt with either a single URL link to an item or multiple URL links for up to three items.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Assistant Designer bot responses, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Link bot response control

Use the Link bot response control in a Virtual Agent topic to present a bot response. The response contains a header prompt with either a single URL link to an item or multiple URL links for up to three items.

**Note:** If you are using the link bot response control for Virtual Agent conversations on Now mobile apps, web links open in the mobile browser. If you want links to open in a native mobile screen within the mobile app, create deep links for items in your conversation topics. For details about deep linking in mobile apps, see the MobileDeepLinkGenerator - Global API.

## Link bot response control properties

<table id="table_il2_n2r_sdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this Link bot response control node in the topic flow.

</td></tr><tr><td>

Link list

</td><td>

Type of links returned in the output result.-   Select **Single Link** to return one item in the output results.
-   Select **Multiple Links** to return up to three items in the output results.

</td></tr><tr><td class="sub-head" colspan="2">

Single link properties

</td></tr><tr><td>

Header

</td><td>

Message displayed above the URL link. The message can be a string with variables or a script.

</td></tr><tr><td>

Label

</td><td>

Text that identifies a single link in the bot bubble. The text can be a string with variables or a script.

</td></tr><tr><td>

Link

</td><td>

Link to a single item, such as a website page or a particular record. The link can be a string with variables or a script that returns a valid URL as a string. For example, you can enter the complete URL, such as `https://servicenow.com`.

</td></tr><tr><td class="sub-head" colspan="2">

Multiple links properties

</td></tr><tr><td>

Header Message

</td><td>

Text prompt that is displayed above the list of links. The prompt can be a string with variables or a script.

</td></tr><tr><td>

Link List Value Expression

</td><td>

Script that creates a list of links to display. The script includes the following parameters: link URL, link display label, link description, and link context.

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

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Supported|None|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Supported|The web link appears as a [URL button](https://developers.facebook.com/docs/messenger-platform/send-messages/buttons#url) in the conversation.|
|SMS Twilio|Supported|None|
|LINE|Supported|None|
|WhatsApp|Supported|None|
|Apple Messages for Business|Supported|Any URLs must be added to the allowed domain list \[sys\_cs\_hostname\_allow\_list\] table.|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For nonscreen devices, the user receives a message: `We found a link`. For details, see [Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](../concept/va-settings-for-alexa.md).|

## Example single-link bot response control

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Single link bot response properties

</th><th>

Link bot response output

</th></tr></thead><tbody><tr><td>

![Basic properties include node name, link list - single or multiple, header, label, and URL link.](../images/va-link-output-properties.png "Single Link bot response control basic properties")

</td><td>

![In this simple example, the header reads, "Here is a link," followed by a hyperlink that reads, "Click Here."](../images/va-link-output-web.png "Web UI Link bot response output")

</td></tr></tbody>
</table>## Example multiple-link bot response control properties

<table id="table_frm_vxp_3kb"><thead><tr><th>

Multi-link bot response properties

</th><th>

Link bot response output

</th></tr></thead><tbody><tr><td>

![Basic properties with the Multiple links option selected. The link list is defined by a script.](../images/va-multi-link-output-properties.png "Multi-link bot response control basic properties")

</td><td>

![Example output that reads, "I found some information that might help you," followed by 3 links with titles and short descriptions.](../images/va-multilink-web-output.png "Web UI Link bot response output - multiple URL links")

 **Note:** Multi-link bot output is also supported in Microsoft Teams, Slack, Workplace, and Facebook Messenger.

</td></tr></tbody>
</table>**Parent Topic:**[Assistant Designer bot responses](va-bot-responses.md)

