---
title: Capturing information from a user in a WhatsApp chat conversation
description: Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from a requester in a WhatsApp chat conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using, Conversational Integration with WhatsApp \(powered by Twilio\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Capturing information from a user in a WhatsApp chat conversation

Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from a requester in a WhatsApp chat conversation.

Virtual Agent Designer is a diagram tool for creating and managing topics, which are blueprints for conversations between a virtual agent and user. For more information, see [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).

## User notification consent

Users must opt in to receive notifications. No notifications can be delivered until the user grants consent.

There are two ways for users to grant consent to receive notifications:

-   The user can enter `Notification` into the WhatsApp chat with your business. The user gets a bot response with the option to subscribe or unsubscribe from receiving notifications for your business on WhatsApp.
-   As the administrator, you can set up the option for users to subscribe or unsubscribe from notifications from your portal. See Subscription-based notifications for more information.

## User input controls

The Conversational Integration with WhatsApp \(powered by Twilio\) application supports the following user input controls in Virtual Agent Designer.

|User input control|Description|
|------------------|-----------|
|Text|User enters a plain text string in the conversation.|
|Static Choice|User selects an item from a predefined list.|
|Boolean|User enters a Boolean response to the bot. For example, the user can reply `Yes` or `No` in a chat conversation.|
|File Picker|User sends a file to the bot.|
|Date Time|User selects a calendar date, time \(hours and minutes\), or both.|
|Carousel|User selects a single item from the carousel.|

For more information about configuring user input controls, see [Assistant Designer user input controls](../reference/va-user-inputs.md).

The Conversational Integration with WhatsApp \(powered by Twilio\) application supports the following bot responses in Virtual Agent Designer.

|Bot response|Description|
|------------|-----------|
|Text|Bot sends a plain text string to the user.|
|Image|Bot sends an image to the user.|
|Link|Bot sends a web link to the user.|
|Web UI image card output|Bot sends content from a record in a compact format, including an image with text.|
|Table|Bot response is displayed as a table.|

For more information about configuring bot responses, see [Assistant Designer bot responses](../reference/va-bot-responses.md).

**Parent Topic:**[Using Conversational Integration with WhatsApp \(powered by Twilio\)](messg-whatsapp-using.md)

