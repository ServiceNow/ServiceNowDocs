---
title: File Picker user input control
description: Use the File Picker user input control in a Virtual Agent topic to prompt a user to upload an image or any file type. After the user uploads an image file, the image appears immediately in the Virtual Agent client.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-11-05"
reading_time_minutes: 5
keywords: [Virtual Agent, file picker, user input]
breadcrumb: [Virtual Agent Designer user input controls, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# File Picker user input control

Use the File Picker user input control in a Virtual Agent topic to prompt a user to upload an image or any file type. After the user uploads an image file, the image appears immediately in the Virtual Agent client.

## File Picker user input control properties

All file types are supported by the file picker, except the SVG format for image files. Although the image can be high resolution, the image displayed in the Virtual Agent client is scaled based on the aspect ratio. Images scale to fit within the chat window.

In Microsoft Teams, a file can be uploaded through the paper clip \(attachment\) icon, or using drag-and-drop. Copying and pasting only works for image files. Users can share attachments on Microsoft Teams through the Virtual Agent file picker user input control, and by sending attachments while chatting with a live agent.

The live agent picker scenario:

-   Doesn't support the SVG format for image files.
-   Supports a combination of text, files, and emojis. However, orders may show up differently between how a user sends these items versus how an agent views these items.
-   Doesn't support formatted text.

When a file upload is in progress, you can't upload or enter text for the file picker control. The uploaded files go through a virus scan and validation.

You can link an uploaded file to a case you create using the Record Action utility. For more information, see [Record Action utility](va-record-action-util.md).

The following table lists the details about the properties of the File Picker.

<table id="table_nff_y1b_3db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies the File Picker user input control node in the topic flow.

</td></tr><tr><td>

Variable name

</td><td>

Name of the variable that stores the user response to this prompt. The variable name is automatically created from the **Node name** property.

</td></tr><tr><td>

Prompt

</td><td>

Prompt or question asking the user to upload the item. The prompt can be a text string that includes variables or a script that returns text.

</td></tr><tr><td>

Allow user to upload

</td><td>

Type of file to upload. All file types are supported, except the SVG format for image files.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Confirmation messages

</td></tr><tr><td>

Input completion confirmation

</td><td>

Bot response shown to the user when the node interaction is complete. The message can be either a text string or a script that returns text. For example, if you're using dot-walking: `Thanks, (Input Variables > Username)!` Or if you're using a script, the acknowledgement might be: `Thanks, {{vaInputs.username}}!`

</td></tr><tr><td>

Default value confirmation

</td><td>

Message that asks the user to verify that the value in the **Default value** field is correct. This message is used instead of a value in the **Prompt** field. It can contain either a text string or a script that returns text. For example, if you're using dot-walking: `Are you (Input Variables > Username)?` Or if you're using a script, the confirmation message might be: `Are you {{vaScripts.lastUsername}}?`.

</td></tr><tr><td class="sub-head" colspan="2">

Hide or skip this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr><tr><td>

Allow user to skip this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip this node in the conversation. The condition must evaluate to true. You can set this field using either the condition builder or a script.

</td></tr><tr><td>

Skip reprompting if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip reprompting in the conversation. When a preceding node is revisited through a topic loopback or Dialog Act, the Virtual Agent bypasses this node and automatically retain its original value.

</td></tr></tbody>
</table>## Using the File Picker control in different client interfaces

The process to select an image differs based on the Virtual Agent client interface. Use the following steps to select an image in the client interface of your choice.

The following table lists details about the File Picker control in different client interfaces.

<table id="table_zjd_5h2_d2b"><thead><tr><th>

Platform

</th><th>

Steps to select an image or file

</th></tr></thead><tbody><tr><td>

Web UI

</td><td>

1.  Select **Click here to upload an image.** or **Click here to upload a file.**
2.  Select a file from your local computer. All file types are supported.

</td></tr><tr><td>

Slack

</td><td>

1.  Select the Green **+** icon.
2.  Select **Your computer**.
3.  Select an image file from your local computer.

All file types are supported.


</td></tr><tr><td>

Microsoft Teams

</td><td>

1.  On your local computer, copy an image file.
2.  Paste the image file into the text input field in Microsoft Teams.

</td></tr><tr><td>

Workplace

</td><td>

1.  Select the Workplace image icon ![Workplace image icon.](../images/FB-image-icon.png).
2.  Select an image file from your local computer.

All file types are supported.


</td></tr><tr><td>

ServiceNow mobile

</td><td>

1.  Touch **Upload an image**.
2.  Select an image file from the photo library on your mobile device.

 **Note:** The **Upload a file** button is only available when you enable the **All file types** file picker property.

</td></tr></tbody>
</table>## Example of a File Picker user input control

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

File Picker properties

</th><th>

File Picker prompt

</th></tr></thead><tbody><tr><td rowspan="2">

![Basic properties include the node name, prompt, and file type, either Image or All file types.](../images/va-file-picker-properties.png "File Picker user input control basic properties")

</td><td>

![In a chat window, the prompt reads, "Please upload your image." The button reads, "Click here to upload an image."](../images/va-file-picker-image.png "Web UI file picker prompt (image)")

</td></tr><tr><td>

![Prompt that reads, "Please upload a file for the detailed description of the case." There are three options: Upload an Image, Take Photo, or Upload a File.](../../notification/image/va-image-picker-mobile.png "ServiceNow mobile file picker prompt")

</td></tr></tbody>
</table>## Channel support

The following table lists the details about the channel support for the File Picker user input control.

<table id="table_kwp_dyq_rsb"><thead><tr><th>

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

Prompt that users see asking for permission for the app to access a camera or file system if the user has not already given the permission.

 ![Prompt that reads, "Mobile" Would Like to Access the Camera. The choices are "Don't Allow" and "OK."](../../notification/image/camera-access-prompt.png)

</td></tr><tr><td>

Now Assist panel

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Microsoft Teams

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Slack

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Workplace

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Facebook Messenger

</td><td>

Supported

</td><td>

Supported file types are JPG, PNG, BMP, and MP4. The files have a maximum size limit based on the file type:

-   For images, the maximum size limit is 10 MB.
-   For videos, the maximum size limit is 200 MB.

</td></tr><tr><td>

SMS Twilio

</td><td>

Partial support

</td><td>

Image files only

</td></tr><tr><td>

LINE

</td><td>

Supported

</td><td>

Supported file types are JPG, PNG, BMP, and MP4. The files have a maximum size limit based on the file type:

-   For images, the maximum size limit is 10 MB.
-   For videos, the maximum size limit is 200 MB.

</td></tr><tr><td>

WhatsApp

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Apple Messages for Business

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Alexa \(Voice\)

</td><td>

Not supported

</td><td>

Not applicable

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer user input controls](va-user-inputs.md)

