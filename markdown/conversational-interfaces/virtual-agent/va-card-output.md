---
title: Card bot response control
description: Use the Card bot response control in a Virtual Agent topic to upload and display selected information from a record on your instance, along with rich content, such as a video or image.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-07-29"
reading_time_minutes: 8
breadcrumb: [Virtual Agent Designer bot responses, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Card bot response control

Use the Card bot response control in a Virtual Agent topic to upload and display selected information from a record on your instance, along with rich content, such as a video or image.

A card can contain record information, an image, or a YouTube video content in a compact format. The compact format is designed for readability within the chat window.

The Card bot response can show the following types of content:

-   Record: Displays content from a single record on your instance. This record can be referenced from variables in the flow or queried using a script that returns a single Glide record from a selected table. The record content includes the display field for the table at the top of the card, followed by any other fields specified by the properties of the bot response.
-   Image: Displays a large or small image that you provide, along with a title and description. The property sheet provides a pre-configured template for the card layout. Specify the title, description, and the image source.
-   YouTube video: Displays in an inline video player if supported on the channel. The image is displayed along with a title, description, and hyperlink to relevant content.

    In the Xanadu release, only YouTube videos are supported.

    **Tip:** You can also use the [Video bot response control](va-video-bot-response.md) to include YouTube videos in conversations. The Video bot response control includes a navigation button that pauses the conversation. If you want the user to watch the video before continuing with the conversation, use this navigation button. When users have finished watching the video, they can click this navigation button to continue with the conversation.


**Note:** If you previously created conversations that use the [HTML bot response control](va-html-output.md) to generate card layouts, consider updating your conversations to use the Card bot response control. The Card displays information from a record in your instance and contains a link to that related record. Or, it can display images and can include rich content such as a video.

## Card bot response control properties

<table id="table_nff_y1b_3db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this Card bot response control node in the topic flow.

</td></tr><tr><td>

Card type

</td><td>

Type of card to be used. Choose one of the following options:-   **Record**
-   **Large image with text**
-   **Small image with text**
-   **YouTube Video Card**

**Note:** In the Xanadu release, only YouTube video cards are supported.


</td></tr><tr><td class="sub-head" colspan="2">

Type: Record

</td></tr><tr><td>

Record

</td><td>

Reference to a specific record. Data for the card comes from a record referenced in a variable from another node in the flow. For example, the reference could be a Choice List or Glide Action. 1.  Select a variable from the current flow that contains a record object.
2.  Use the **fields** list to determine the fields displayed in the card.

</td></tr><tr><td>

Table

</td><td>

Table that references a single Glide record that contains the data shown in the card.

</td></tr><tr><td>

Filter this table by using

</td><td>

Enter the condition or script to filter data in the table and return the record.-   **Condition**: Condition statement that returns the table record.
-   **Script**: Glide record query that returns the glide record.

</td></tr><tr><td>

fields

</td><td>

Fields from the ServiceNow record to be displayed in the card. Specify each field by clicking **Add Field**.

 **Note:** If you're using Workplace, a maximum of four fields is rendered on the card. If you have more than four fields, the remaining fields are displayed on a subsequent card, with up to four fields per card.

</td></tr><tr><td class="sub-head" colspan="2">

Type: Large image with text or Small image with text

</td></tr><tr><td>

Template

</td><td>

A visual representation that shows the image card layout. Each area of the template is numbered.

</td></tr><tr><td>

Map data to fields on the card

</td><td>

Fields that correspond to the numbers shown on the template. These fields are the following:1.  **Title**: Name or label for the card
2.  **Description**: Explanation of the image
3.  **Image URL link**: Specify the image displayed in the card in one of the following ways:

    -   Specify the image URL, using the text field, data pill, or script.
    -   Upload the image by clicking **Upload Image**.
If you upload an image, the selected image is uploaded to the server and is stored in the Images \[sys\_db\_image\] table and in the update sets. When the image is stored in the Images table and the update sets, you can use the image in a production or non-production instance, as needed.

After the image is uploaded, the URL link is included in the**Response Properties** sheet.

![The link to an uploaded image is shown in the property sheet.](../images/va-upload-image-with-link-example.png)

Click the link to view the image.

The URL is generated dynamically. The name of the instance is inserted at the front of the URL path.

You can change or delete the link to the image. If you delete the link on this property sheet, only the reference to the URL is deleted. The image remains on the server for future use.

4.  **Image alt text**: Alternative, screen-readable text that describes the image for accessibility programs. This text is used along with the image. Enter the text using the text field, data pill, or script.

</td></tr><tr><td class="sub-head" colspan="2">

Type: YouTube Video card

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

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Channel support

<table id="table_yqr_3fp_tsb"><thead><tr><th>

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

Partial support

</td><td>

Record cards and record cards with action only.

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

Conversational Integration with Slack Version 2.0.0 and later.The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

</td></tr><tr><td>

Workplace

</td><td>

Partial support

</td><td>

Image card output not available.Facebook apps no longer support vertical list templates. The card layout uses a horizontal, scrollable carousel template effective August 15, 2019. Cards also feature a button template.

</td></tr><tr><td>

Facebook Messenger

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

SMS Twilio

</td><td>

Supported

</td><td>

Records and image cards only.

</td></tr><tr><td>

LINE

</td><td>

Partial support

</td><td>

Records and image cards only.

</td></tr><tr><td>

WhatsApp

</td><td>

Partial support

</td><td>

Records and image cards only.

</td></tr><tr><td>

Apple Messages for Business

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Alexa \(Voice\)

</td><td>

Partial support

</td><td>

Some types of output are only available on devices with screens. For nonscreen devices, the card title is read. For details, see [Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](../concept/va-settings-for-alexa.md).

</td></tr></tbody>
</table>## Example Glide record query

```
(function execute(table) {
    /* Write a glide record query, and return the glide record.
       For example:
       
       var now_GR = new GlideRecord(table);
       gr.addEncodedQuery('active=true^number=INC0010099');
       gr.query();
       if(gr.next()) {
          return gr;
    }
    */
})(table)

```

In this example, the script creates a GlideRecord object, populates this object using a query that should return a single result, then returns the object. The **Table** property defines the table used in this query.

## Example Card bot response output for records

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Response properties

</th><th>

Card output

</th></tr></thead><tbody><tr><td>

![Basic properties include the node name, card type, how the card should be populated - record or table, and the fields to return.](../images/va-card-properties.png "Card bot response control basic properties")

</td><td>

![An example card that shows the Incident and Incident number in the header. The fields shown are Category, Short description, and State.](../../notification/image/va-card-native.png "Web UI Card output")

 ![Example card from a Microsoft Teams conversation, showing Conversation and creation time in header. The displayed fields include Consumer, SysID, Device type, and creation date and time.](../images/Card-MSteams-01.png "Microsoft Teams Card output")

</td></tr></tbody>
</table>## Example Card bot response for a large image

The Card response layout for images may vary across channels.

<table id="table_f5b_s4v_g4b"><thead><tr><th>

Response properties

</th><th>

Card output

</th></tr></thead><tbody><tr><td>

![Basic properties include the node name, card type, card template, title, description, image link, and image alt text.](../images/va-card-image-props.png)

</td><td>

![Card that reads, "Don't forget we are going back to the office soon!" in the header. It includes the user's schedule return day and an image link to more information.](../images/va-bot-card-web-image.png "Web UI image card output")

 ![Microsoft Teams image card, showing header title Scenery, and a placeholder line Scenery Description.](../images/Card-MSteams-02.png "Microsoft Teams UI image card")

</td></tr></tbody>
</table>## Example Card bot response for a small image

The Card response layout for images may vary across channels.

<table id="table_tjb_mrr_gpb"><thead><tr><th>

Response properties

</th><th>

Card output

</th></tr></thead><tbody><tr><td>

![Basic properties include the node name, card type, template, title, description, image link, and image alt text.](../images/va-card-image-props-small-image.png)

</td><td>

![The user asks, "When do we announce the earnings?" A card is returned with a header that reads, "Save the date - Q1 Earnings Call."](../images/va-card-small-image-example-.png "Web UI image card output")

</td></tr></tbody>
</table>## Example Card bot response with video content

The way the Card bot response displays videos may vary across channels. For example, the display you see in Slack messages may be different from what you see on Microsoft Teams or Workplace from Facebook. Also, if an embedded player is supported on that channel, the player is included in the display. For more information about channels, see the documentation for the channel that you're using.

<table id="id_irz_szc_54b"><thead><tr><th>

Response properties

</th><th>

Card output

</th></tr></thead><tbody><tr><td>

![Basic properties include the node name, card type, template, title, title link, description, and YouTube video ID.](../images/va-card-video-properties-3.png)

</td><td>

![Card that reads, "Check out our new Christmas campaign." The YouTube video is embedded beneath and displays the linked title and description.](../images/youtube-video-card-output-all-opts.png "Card bot response output with video on the chat widget")

 ![Microsoft Teams video card, showing header title Video Example, and placeholder line Video Example Description.](../images/Card-MSteams-03.png "Card bot response output with video on Microsoft Teams")

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer bot responses](va-bot-responses.md)

