---
title: Capturing information from a user in a Apple Messages for Business chat conversation
description: Virtual Agent Designer is a diagram tool for creating and managing topics, which are blueprints for conversations between a virtual agent and user.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Conversational Integration with Apple Messages for Business, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Capturing information from a user in a Apple Messages for Business chat conversation

Virtual Agent Designer is a diagram tool for creating and managing topics, which are blueprints for conversations between a virtual agent and user.

Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from a requester in a Apple Messages for Business chat conversation. For more information, see [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).

For more information about displaying images along with external links, see [Using link unfurling in Virtual Agent](va-link-unfurling.md).

Apple Messages for Business has an array of interactive features that are native to the app. For more information about these interactive features, see [Conversational Integration with Apple Messages for Business](integration-apple-mssg.md).

## User notification consent

**Note:**

Notifications are turned off by default for the Apple Messages for Business channel. Make sure to enable notifications at the channel level.

Users must opt in to receive notifications. No notifications can be delivered until the user grants consent.

There are two ways for users to grant consent to receive notifications:

-   The user can enter `Notification` into the Apple Messages for Business chat to get a bot response with the option to subscribe or unsubscribe from receiving notifications for your business on Apple Messages for Business.
-   As the administrator, you can set up the option for users to subscribe or unsubscribe from notifications from your portal. See [Subscription-based notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_SubscriptionBasedNotifications.md) for more information.

## User input controls

The Conversational Integration with Apple Messages for Business application supports the following user input controls in Virtual Agent Designer.

|User input control|Description|
|------------------|-----------|
|Text|User enters a plain text string in the conversation.|
|Static Choice|User selects an item from a predefined list.|
|Dynamic Choice|User selects an item from a list that is created dynamically. For example, the user can select from a list of cases that they opened.|
|Boolean|User enters a Boolean response to the bot. For example, the user can reply `Yes` or `No` in a chat conversation.|
|File Picker|User sends a file to the bot.|
|Date Time|User selects a calendar date, time \(hours and minutes\), or both.|
|Carousel|User selects a single item from the carousel.|

For more information about configuring user input controls, see [Assistant Designer user input controls](../reference/va-user-inputs.md).

The Conversational Integration with Apple Messages for Business application supports the following bot responses in Virtual Agent Designer.

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

Bot sends a web link to the user.

 **Note:** Any URLs must be added to the allowed domain list \(`sys_cs_hostname_allow_list`\) table.

</td></tr><tr><td>

Table

</td><td>

Bot sends information in a table format so that users can see information in a more organized way.

For example, you can organize and display information such as the following:-   Planned service changes
-   Company holidays
-   Contact information
-   Testing sites

</td></tr><tr><td>

Card

</td><td>

Bot uploads and displays selected information from a record on your instance. You can choose a record card, video card, or small or large image card.

</td></tr></tbody>
</table>For more information about configuring bot responses, see [Assistant Designer bot responses](../reference/va-bot-responses.md).

