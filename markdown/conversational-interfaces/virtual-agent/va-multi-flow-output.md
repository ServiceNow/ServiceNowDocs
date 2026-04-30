---
title: Multi-response bot response control
description: Use the Multi-response bot response control in a Virtual Agent topic to sequentially display two or more outputs. Outputs can be text, image, link, or HTML. Users can move from one output to the next through a provided navigation button.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Virtual Agent Designer bot responses, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Multi-response bot response control

Use the Multi-response bot response control in a Virtual Agent topic to sequentially display two or more outputs. Outputs can be text, image, link, or HTML. Users can move from one output to the next through a provided navigation button.

## Multi-response bot response control properties

<table id="table_gzl_msz_hdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

The name that identifies this Multi-response control node in the topic flow.

</td></tr><tr><td>

Add a response

</td><td>

One or more bot responses. For each output type, select **+ Add a Response** to specify the output and define the output properties. 1.  In the Add a Response dialog box, select the **Type**, and specify the associated values:
    -   **Text**: In the **Value** field, enter the text to be displayed in the response.
    -   **HTML**: Enter the **Height** and **Width**, in pixels, to set the dimensions of the HTML block. In the HTML editor, enter the HTML markup to be displayed.
    -   **Image**: Enter a URL in the **Image** field, or select **Upload Image** and choose the image file to upload.
    -   **Link**: Enter the **Header**, **Label** \(label for the link\), and the **Link** \(path or URL for the link\).
2.  Select **Save**.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Navigation button label

</td></tr><tr><td>

Label the button that lets the user continue the conversation

</td><td>

The label for the button displayed below the output. The button enables the user to move to the next output in the flow.

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
|Now Assist panel|Not supported|Not applicable|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Not supported|Not applicable|
|SMS Twilio|Not supported|Not applicable|
|LINE|Not supported|Not applicable|
|WhatsApp|Not supported|Not applicable|
|Apple Messages for Business|Not supported|Not applicable|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For non-screen devices, the user receives a message if unsupported elements are used: `We found a link`. For details, see [Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](../concept/va-settings-for-alexa.md).|

## Example Multi-response control

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Output properties

</th><th>

Multi-response output

</th></tr></thead><tbody><tr><td>

![Basic properties include the node name and the response organized by type: Text, HTML, Image, and Link.](../images/va-multi-flow-properties.png "Multi-response bot response control basic properties")

</td><td>

![A basic response includes text output followed by a hyperlink.](../images/va-multi-flow-web.png "Web UI Multi-response bot response output")

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer bot responses](va-bot-responses.md)

