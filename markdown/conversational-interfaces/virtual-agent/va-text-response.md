---
title: Text bot response control
description: Use the Text bot response control in a Virtual Agent topic to display a bot response as text. You can format the Text bot responses using the text editor controls. For example, you can bold or italicize the text, as well as include links, bulleted lists, and emojis.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Virtual Agent, designer, Text response, bot response, control, node]
breadcrumb: [Virtual Agent Designer bot responses, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Text bot response control

Use the Text bot response control in a Virtual Agent topic to display a bot response as text. You can format the Text bot responses using the text editor controls. For example, you can bold or italicize the text, as well as include links, bulleted lists, and emojis.

## Text bot response properties

Use the Text response properties panel to design bot responses to the user.

![Bot text response properties.](../images/bot-text-response.png)

<table id="table_gzl_msz_hdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this Text bot response node in the topic flow.

</td></tr><tr><td>

Response message

</td><td>

The Text bot response to the user. The response can be one of the following:-   Rich text message.
-   Script, which can include Glide record variables or script variables.

**Note:** The script can also include a temporary password for the end user.


You can format the text messages using the text editor controls. For example, you can use the icons on the **Response Message** field to bold or italicize the text, as well as include links, bulleted lists, numbered lists, and emojis.

![Text bot response message options: Open an incident in the Support Portal, or call for immediate assistance.](../images/rich-text-response-message-options.png)

You can also include an input variable, such as a temporary password, in the response message.

![Temporary password text response message.](../images/temp-password-text-bot.png)

To include a link, do one of the following:

-   Select the link icon: ![Link icon.](../images/link-icon.png).
-   Add your response message. Select the text to use as a link, and then select the link icon.

Fill in the fields in the Confirmation window. Enter the text to use as the link, and then enter the URL in the Link field.

Enter the display label for the link and a static URL, or use the data pill picker to create a dynamic URL.

</td></tr><tr><td>

Add alternate message

</td><td>

Add one or more alternate response messages for the user. Virtual Agent randomly chooses one of your responses for each conversation.![Three defined alternate response messages: "User, sounds great," "Excellent choice," and "Let's proceed with Chosen Option, then."](../images/rich-text-response-multiple-message-options.png)

</td></tr></tbody>
</table><table id="table_vfq_y2s_z2c"><tbody><tr><td class="sub-head" colspan="2">

Shorten responses

</td></tr><tr><td>

Enable

</td><td>

When turned on, long bot responses are shortened. A **Show more** link is shown along with the truncated response. When the option is turned off, the entire response is used. By default, this option is turned on.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Make this response secure

</td></tr><tr><td>

Enable

</td><td>

When enabled, the bot response is displayed to the user, but thereafter securely masked and not viewable by others.

</td></tr><tr><td class="sub-head" colspan="2">

Request feedback

</td></tr><tr><td>

Enable

</td><td>

When turned on, thumbs up and down icons are displayed next to bot responses for feedback.

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

A no-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

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
|Facebook Messenger|Supported|Plain text string only|
|SMS Twilio|Supported|None|
|LINE|Supported|None|
|WhatsApp|Supported|None|
|Apple Messages for Business|Supported|None|
|Alexa \(Voice\)|Supported|For screen devices, full support. For nonscreen devices, the header is read.|

## Example Text bot response script

In this example, the script returns a string that greets the user. The **gs.getUser\(\).getFirstName\(\)** property is used to append the first name of the current user.

```
(function execute() {
    return 'Hello ' + gs.getUser().getFirstName();
})()
```

In this example, the script returns links to three instances in the response. Use **Markdown** to include multiple links in the script.

```
(function execute() {
    var output = 'Hello\n';
    output += '\n- [Instance 1](http://instance1.com)';
    output += '\n- [Instance 2](http://instance2.com)';
    output += '\n- [Instance 3](http://instance3.com)';
    return output;
})()
```

## Example Text bot response control

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Response properties

</th><th>

Text bot response output

</th></tr></thead><tbody><tr><td>

![Basic properties include the node name and a rich text response message area.](../images/va-rich-text-bot-properties.png "Text bot response control basic properties")

</td><td>

![Text response with emojis that reads, "We could not find any assets currently assigned to you." A phone number, additional steps, and a link are included.](../images/rich-text-example-web-ui.png "Web UI Text bot response output")

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer bot responses](va-bot-responses.md)

