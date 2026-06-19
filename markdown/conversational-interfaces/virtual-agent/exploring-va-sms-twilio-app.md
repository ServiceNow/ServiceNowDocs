---
title: Exploring Conversational SMS Integration with Twilio
description: Conversational SMS Integration with Twilio enables users to initiate conversations with Virtual Agent by messaging your Twilio phone number.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/exploring-va-sms-twilio-app.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Conversational SMS Integration with Twilio, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Exploring Conversational SMS Integration with Twilio

Conversational SMS Integration with Twilio enables users to initiate conversations with Virtual Agent by messaging your Twilio phone number.

**Note:** Do not use the same ServiceNowTwilioDirect or Twilio Notify phone number for Conversational SMS Integration with Twilio. Instead, use separate Twilio numbers for Conversational SMS Integration with Twilio and ServiceNowTwilioDirect.

\[Omitted image "sms-twilio-app.png"\] Alt text: The user texts, "I have an issue." Virtual Agent asks for additional information and offers 4 choices for the user to select: Product issue, Order support, Billing, and Other.

If a bot transfers the conversation to a live agent, the agent can respond to SMS messages in Agent Workspace.

After you set up the Conversational SMS Integration with Twilio, you can create SMS conversation topics in Virtual Agent Designer. For more information about using the tool, see [Getting started with Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md).

## Capturing information from a user in an SMS chat conversation

## Supported controls

The Conversational SMS Integration with Twilio does not support all the available controls in Virtual Agent Designer.

The following user input controls are supported in Twilio SMS conversations:

<table id="table_fq2_gqz_2mb"><thead><tr><th>

User input control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text

</td><td>

User enters a plain text string in the conversation.

 \[Omitted image "sms-text-input.png"\] Alt text: User enters text in a conversation: "I need help!"

</td></tr><tr><td>

Static Choice

</td><td>

User selects an item from a predefined list.

 \[Omitted image "sms-user-static-choice.png"\] Alt text: User enters "CHANGE." The bot displays 3 additional timeslots and an "Other" option. The user enters the number for a new timeslot. Appointment is confirmed.

</td></tr><tr><td>

Dynamic Choice

</td><td>

User selects an item from a list that is created dynamically. For example, the user can select from a list of cases that they opened.

 \[Omitted image "sms-user-ref-choice.png"\] Alt text: The bot displays the user's 7 open cases. The user enters 6, and the bot provides a link to view that case.

</td></tr><tr><td>

Boolean

</td><td>

User enters a Boolean response to the bot. For example, the user can reply "Yes" or "No" in the conversation.

 \[Omitted image "sms-boolean-input.png"\] Alt text: The bot congratulates the user on their purchase and offers to display more information. The user enters "Yes," so the bot provides a link to a KB article.

</td></tr><tr><td>

File picker

</td><td>

User sends a file to the bot.**Note:** Conversational SMS Integration with Twilio doesn't support all file types. Only images can be sent in an SMS conversation.

\[Omitted image "sms-image-input.png"\] Alt text: The bot displays an example image that indicates the serial number location. The user uploads a photo of their product's serial number.

</td></tr></tbody>
</table>For more information on configuring user input controls, see [Virtual Agent Designer user input controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-user-inputs.md).

The following bot responses are supported in Twilio SMS conversations:

<table id="table_mq2_gqz_2mb"><thead><tr><th>

Bot response

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text

</td><td>

Bot sends a plain text string to the user.\[Omitted image "sms-bot-text.png"\] Alt text: Bot sends a text: "Your order is scheduled for install on Dec 25th between 10am and 1pm. Is this ok?" The user enters YES, and the bot confirms their choice.

</td></tr><tr><td>

Image

</td><td>

Bot sends an image to the user.\[Omitted image "sms-bot-image.png"\] Alt text: The bot sends an image that shows the user where to find their product's serial number.

</td></tr><tr><td>

Link

</td><td>

Bot sends a web link to the user.\[Omitted image "sms-bot-link.png"\] Alt text: The bot sends an appointment confirmation to the user, who enters CHANGE. The bot responds with a link where the user can view new appointment options.

</td></tr><tr><td>

Card

</td><td>

Bot sends selected information from a record on your instance. \[Omitted image "sms-bot-card.png"\] Alt text: When the user says their router is on fire, the bot creates a case and sends the card with the number, priority, assigned agent, and a link.

</td></tr></tbody>
</table>For more information on configuring bot responses, see [Virtual Agent Designer bot responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-bot-responses.md).

Live agents can use the Text, Card, and Image response controls to reply to users in SMS conversations.

## User subscriptions for SMS update notifications

Beginning with version 1.1.1, your users with ServiceNow accounts \(sys\_user profiles\) can choose to start or stop receiving SMS updates in their conversations.

**Note:** Notifications in messaging channels can be sent to users with ServiceNow accounts. Other recipients, such as consumer and customer contacts, are considered to be guests and cannot receive notifications on messaging channels.

To comply with privacy regulations, user notifications are turned off by default. Users can opt in or change their settings in the following ways:

-   To check SMS notification settings for the account, send this text: `Notification`
-   To receive SMS notifications, send this text: `START`
-   To stop receiving SMS notifications, send this text: `STOP`

\[Omitted image "sms-notifications-start-stop.png"\] Alt text: The user enters "notifications" to view settings, which are currently on. The user enters STOP, and the bot unsubscribes them. When the user enters START, the bot confirms the re-subscription.

To learn more about Virtual Agent notifications, see [Configuring Virtual Agent notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configuring-va-notifications.md).

For details about creating content for a messaging notification, see [Define Virtual Agent notification contents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/define-va-notif-contents.md).

## What to explore next

To learn more about configuring and using , see:

-   [Configuring Conversational SMS Integration with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-va-sms-twilio-app.md)
-   [Using Conversational SMS Integration with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/using-sms-integ-twilio.md)

**Parent Topic:**[Conversational SMS Integration with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/sms-twilio-store-app.md)

