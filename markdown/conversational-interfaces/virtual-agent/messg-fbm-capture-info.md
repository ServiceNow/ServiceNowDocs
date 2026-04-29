---
title: Capturing information from a user in a Facebook Messenger chat conversation
description: Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from the user in a Facebook Messenger chat conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Conversational Integration with Facebook Messenger, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Capturing information from a user in a Facebook Messenger chat conversation

Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from the user in a Facebook Messenger chat conversation.

Virtual Agent Designer is a diagram tool for creating and managing topics, which are blueprints for conversations between a virtual agent and user. For more information, see [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).

The Conversational Integration with Facebook Messenger application supports the following user input controls in Virtual Agent Designer.

<table id="table_fq2_gqz_2mb"><thead><tr><th>

User input control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text

</td><td>

User enters a plain text string in the conversation.The maximum character limit is 5000 characters.

</td></tr><tr><td>

Static Choice

</td><td>

User selects an item from a predefined choice list.In a quick reply, the label has the maximum character limit of 20 characters. At a time, a user can view only 13 quick replies. If there are more than 13 quick replies, the pagination format is used to view more options. The default value of the maximum number of replies for a page is set in the **sn\_va\_fb\_messenger.max\_quick\_replies** system property \(location: System Property \[sys\_properties\] table\).

</td></tr><tr><td>

Boolean

</td><td>

User enters a Boolean response to the bot. For example, the user can reply `Yes` or `No` in a chat conversation.

</td></tr><tr><td>

File Picker

</td><td>

User sends a file to the bot.The supported file types are JPG, PNG, BMP, and MP4.

 Note the following points about the maximum size limit for a file type:

 -   For images, the maximum size limit is 10 MB.
-   For videos, the maximum size limit is 200 MB.

</td></tr><tr><td>

Date Time

</td><td>

User selects a calendar date, time \(hours and minutes\), or both.**Note:** If your administrator has set the option to request time zone from the customer, the selected date and time reflect customer's time zone. Else, they appear in the UTC time zone. For more information about the time zone setting, see [1.f](../task/messg-fbm-setup.md#time-zone).

</td></tr><tr><td>

Carousel

</td><td>

User selects a single item from the carousel.In a carousel, the title for an image has maximum limit of 40 characters and the text for the image has maximum character limit of 60 characters. At a time, a user can view only 10 images. If there are more than 10 images, the pagination format is used to view more options. The default value of the maximum number of images in a carousel for a page is set in the **sn\_va\_fb\_messenger.max\_carousel\_cards** system property \(location: System Property \[sys\_properties\] table\).

</td></tr></tbody>
</table>For more information about configuring user input controls, see [Assistant Designer user input controls](../reference/va-user-inputs.md).

The Conversational Integration with Facebook Messenger application supports the following bot responses in Virtual Agent Designer.

<table id="table_mq2_gqz_2mb"><thead><tr><th>

Bot response

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text

</td><td>

Bot sends a plain text string to the user.

</td></tr><tr><td>

Image

</td><td>

Bot sends an image to the user.

</td></tr><tr><td>

Link

</td><td>

Bot sends a web link to the user. **Note:** The web link appears as a [URL button](https://developers.facebook.com/docs/messenger-platform/send-messages/buttons#url) in the conversation.

</td></tr><tr><td>

Card

</td><td>

Bot sends selected information from a record on your instance.

</td></tr></tbody>
</table>**Note:** You can also return search results as bot responses in Facebook Messenger chat conversations when there are no relevant topics to display to end users. For more information, see [Improving the user experience with AI Search](va-ai-search.md).

For more information about configuring bot responses, see [Assistant Designer bot responses](../reference/va-bot-responses.md).

**Parent Topic:**[Using Conversational Integration with Facebook Messenger](messg-fbm-using.md)

