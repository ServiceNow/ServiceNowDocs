---
title: Capturing information from a user in a WhatsApp chat conversation
description: Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from a requester in a WhatsApp chat conversation.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-01-09"
reading_time_minutes: 3
breadcrumb: [Using, Conversational Integration with WhatsApp \(WhatsApp Cloud API\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Capturing information from a user in a WhatsApp chat conversation

Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from a requester in a WhatsApp chat conversation.

Virtual Agent Designer is a diagram tool for creating and managing topics, which are blueprints for conversations between a virtual agent and user. For more information, see [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).

## User notification consent

Users must opt in to receive notifications. No notifications can be delivered until the user grants consent.

There are two ways for users to grant consent to receive notifications:

-   The user can enter `Notification` into the WhatsApp chat with your business. The user gets a bot response with the option to subscribe or unsubscribe from receiving notifications for your business on WhatsApp.
-   As the administrator, you can set up the option for users to subscribe or unsubscribe from notifications from your portal. See [Subscription-based notifications](https://www.servicenow.com/docs/access?context=c_SubscriptionBasedNotifications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

## User input controls

The Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application supports the following user input controls in Virtual Agent Designer.

|User input control|Description|
|------------------|-----------|
|Text|User enters a plain text string in the conversation.|
|Static Choice|User selects an item from a predefined list.|
|Boolean|User enters a Boolean response to the bot. For example, the user can reply `Yes` or `No` in a chat conversation.|
|File Picker|User sends a file to the bot.|
|Dynamic choice|User selects an item from a dynamic list \(partial support\).|
|Date Time|User selects a calendar date, time \(hours and minutes\), or both.|
|Carousel|User selects a single item from the carousel.|

For more information about configuring user input controls, see [Assistant Designer user input controls](../reference/va-user-inputs.md).

The Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application supports the following bot responses in Virtual Agent Designer.

|Bot response|Description|
|------------|-----------|
|Text|Bot sends a plain text string to the user.|
|Image|Bot sends an image to the user.|
|Link|Bot sends a web link to the user.|
|Card|Bot sends selected information from a record on your instance.|

<table id="table_vpr_j54_mqb"><thead><tr><th>

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

Bot sends a web link to the user.

</td></tr><tr><td>

Card

</td><td>

Record card: Bot sends content from a record in a compact format.Image card: Sends an image along with a caption.

YouTube video card: Bot sends a YouTube video link with a title and description.

</td></tr><tr><td>

HTML

</td><td>

Not supported

</td></tr><tr><td>

Script

</td><td>

Not supported

</td></tr><tr><td>

Multi-response

</td><td>

Bot sends text, image, and link with an interactive button.

</td></tr><tr><td>

Video

</td><td>

Bot sends a video link with title, description, and interactive button.

</td></tr><tr><td>

Web UI image card output

</td><td>

Bot sends content from a record in a compact format, including an image with text.

</td></tr><tr><td>

Table

</td><td>

Bot response is displayed as a table.

</td></tr></tbody>
</table>For more information about configuring bot responses, see [Virtual Agent Designer bot responses](../reference/va-bot-responses.md).

**Parent Topic:**[Using Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](messg-direct-whatsapp-using.md)

