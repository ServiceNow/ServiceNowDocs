---
title: Image bot response control
description: Use the Image bot response control in a Virtual Agent topic to upload and display an image from a URL link. The image aspect ratio determines how the image is sized in the bot chat bubble.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Assistant Designer bot responses, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Image bot response control

Use the Image bot response control in a Virtual Agent topic to upload and display an image from a URL link. The image aspect ratio determines how the image is sized in the bot chat bubble.

## Image bot response control properties

<table id="table_il2_n2r_sdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this Image bot response control node in the topic flow.

</td></tr><tr><td>

Image URL link

</td><td>

The URL link to an image file you want to include in the conversation. To set a value, do one of the following:-   Specify the image URL by using the text field, data pill, or script.
-   Upload an image by clicking **Upload Image**.

 If you upload an image, then the selected image is uploaded to the server and is stored in the Images \[sys\_db\_image\] table and in the update sets. When the image is stored in the Images table and the update sets, then you can use the image in a production or non-production instance, as needed.

 After the image is uploaded, the URL link is included in the**Response Properties** sheet:

 ![Uploaded link shown in the property sheet.](../images/va-upload-image-with-link-example.png)

 Click the link to view the image.

 The URL is generated dynamically. The name of the instance is inserted at the front of the URL path.

 You can change or delete the link to the image. If you delete the link on this property sheet, only the reference to the URL is deleted. The image remains on the server for future use.

</td></tr><tr><td>

Image alt text

</td><td>

Alternative, screen-readable text included for accessibility. This text is used along with the image. Enter the text using the text field, data pill, or script. For more information about using data pills or scripts, see [Assistant Designer controls](../concept/virtual-agent-controls.md).

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
|Web UI|Supported|The maximum image size is determined by the **com.glide.attachment.max\_size** system property. The default value is 1024 MB.|
|Mobile UI|Supported|The maximum image size is determined by the **com.glide.attachment.max\_size** system property. The default value is 1024 MB.|
|Now Assist panel|Not supported|Not applicable|
|Microsoft Teams|Supported|None|
|Slack|Supported|For details about the maximum image size allowed, check the Slack documentation.|
|Workplace|Supported|For details about the maximum image size allowed, check the Workplace documentation.|
|Facebook Messenger|Supported|For details about the maximum image size allowed, check the Facebook Messenger documentation.|
|SMS Twilio|Supported|File size limits may vary. For Twilio limitations, check their [Accepted Content Types for Media](https://www.twilio.com/docs/sms/accepted-mime-types).|
|LINE|Supported|File size limits may vary. For details, see the LINE documentation.|
|WhatsApp|Supported|File size limits may vary. For details, see the WhatsApp documentation.|
|Apple Messages for Business|Supported|None|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For nonscreen devices, the user receives a message: `We found an image`. For details, see [Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](../concept/va-settings-for-alexa.md).|

## Example Image bot response control

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Response properties

</th><th>

Image bot response output

</th></tr></thead><tbody><tr><td rowspan="2">

![Basic properties include node name, the URL link to the image, and image alt text.](../images/va-image-response-properties.png "Image bot response control basic properties")

</td><td>

![A chat window shows a picture of a computer.](../images/va-image-response-web.png "Web UI Image bot response output")

</td></tr><tr><td>

![A chat window shows a picture of a computer.](../images/va-image-response-mobile.png "ServiceNow mobile Image bot response output")

</td></tr></tbody>
</table>**Parent Topic:**[Assistant Designer bot responses](va-bot-responses.md)

