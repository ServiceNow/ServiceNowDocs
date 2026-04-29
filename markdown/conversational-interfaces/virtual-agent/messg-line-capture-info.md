---
title: Capturing information from a user in a LINE chat conversation
description: Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from the user in a LINE chat conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Conversational Integration with LINE, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Capturing information from a user in a LINE chat conversation

Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from the user in a LINE chat conversation.

Virtual Agent Designer is a diagram tool for creating and managing topics, which are blueprints for conversations between a virtual agent and user. For more information, see [Using Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).

## User notification consent

Users must opt in to receive notifications. No notifications can be delivered until the user grants consent.

There are two ways for users to grant consent to receive notifications:

-   The user can enter `Notification` into the LINE chat with your business. The user gets a bot response with the option to subscribe or unsubscribe from receiving notifications for your business on LINE.
-   As an administrator, you can set up the option for users to subscribe or unsubscribe from notifications from your portal. See [Subscription-based notifications](https://www.servicenow.com/docs/access?context=c_SubscriptionBasedNotifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information.

## User input controls

The Conversational Integration with LINE application supports the following user input controls in Virtual Agent Designer.

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

User selects an item from a predefined list.In a quick reply, the label has the maximum character limit of 20 characters. At a time, a user can view only 13 quick replies. If there are more than 13 quick replies, the pagination format is used to view more options. The default value of the maximum number of replies for a page is set in the **sn\_va\_line.max.picker.choices** system property. The property is located in the System Property \[sys\_properties\] table.

</td></tr><tr><td>

Boolean

</td><td>

User enters a Boolean response to the bot. For example, the user can reply `Yes` or `No` in a chat conversation.

</td></tr><tr><td>

File Picker

</td><td>

User sends a file to the bot.The supported file types are JPG, PNG, BMP, and MP4. Files have a maximum size limit based on file type:

-   For images, the maximum size limit is 10 MB.
-   For videos, the maximum size limit is 200 MB.

</td></tr><tr><td>

Date Time

</td><td>

User selects a calendar date, time \(hours and minutes\), or both.

</td></tr><tr><td>

Carousel

</td><td>

User selects a single item from the carousel.In a carousel, the title for an image has a maximum limit of 40 characters and the text for the image has a maximum character limit of 60 characters. At a time, a user can view only 10 images. If there are more than 10 images, the pagination format is used to view more options. The default value of the maximum number of images in the carousel for a page is set in the **sn\_va\_line.max.carousel.cards** system property. The property is located in the System Property \[sys\_properties\] table.

</td></tr></tbody>
</table>For more information about configuring user input controls, see [Assistant Designer user input controls](../reference/va-user-inputs.md).

The Conversational Integration with LINE application supports the following bot responses in Virtual Agent Designer.

|Bot response|Description|
|------------|-----------|
|Text|Bot sends a plain text string to the user.|
|Image|Bot sends an image to the user.|
|Link|Bot sends a web link to the user.|
|Web UI image card output|Bot sends content from a record in a compact format, including an image with text.|
|Table|Bot response is displayed as a table.|

For more information about configuring bot responses, see [Assistant Designer bot responses](../reference/va-bot-responses.md).

