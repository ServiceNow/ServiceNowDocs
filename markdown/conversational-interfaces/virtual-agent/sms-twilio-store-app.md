---
title: Integrating Virtual Agent with Twilio
description: Host Virtual Agent conversations on Twilio SMS to chat with virtual agent or live agents. Use the Conversational SMS Integration with Twilio app, available from the ServiceNow Store, to associate your instance with SMS Twilio.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Twilio

Host Virtual Agent conversations on Twilio SMS to chat with virtual agent or live agents. Use the Conversational SMS Integration with Twilio app, available from the ServiceNow Store, to associate your instance with SMS Twilio.

## Capturing information from a user in an SMS chat conversation

Conversational SMS Integration with Twilio enables users to initiate conversations with Virtual Agent by messaging your Twilio phone number.

**Note:** Do not use the same ServiceNowTwilioDirect or Twilio Notify phone number for Conversational SMS Integration with Twilio. Instead, use separate Twilio numbers for Conversational SMS Integration with Twilio and ServiceNowTwilioDirect.

![The user texts, "I have an issue." Virtual Agent asks for additional information and offers 4 choices for the user to select: Product issue, Order support, Billing, and Other.](../images/sms-twilio-app.png "Example SMS conversation with Virtual Agent")

If a bot transfers the conversation to a live agent, the agent can respond to SMS messages in Agent Workspace.

After you set up the Conversational SMS Integration with Twilio, you can create SMS conversation topics in Virtual Agent Designer. For more information on using the tool, see [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

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

 ![User enters text in a conversation: "I need help!"](../images/sms-text-input.png)

</td></tr><tr><td>

Static Choice

</td><td>

User selects an item from a predefined list.

 ![User enters "CHANGE." The bot displays 3 additional timeslots and an "Other" option. The user enters the number for a new timeslot. Appointment is confirmed.](../images/sms-user-static-choice.png)

</td></tr><tr><td>

Dynamic Choice

</td><td>

User selects an item from a list that is created dynamically. For example, the user can select from a list of cases that they opened.

 ![The bot displays the user's 7 open cases. The user enters 6, and the bot provides a link to view that case.](../images/sms-user-ref-choice.png)

</td></tr><tr><td>

Boolean

</td><td>

User enters a Boolean response to the bot. For example, the user can reply "Yes" or "No" in the conversation.

 ![The bot congratulates the user on their purchase and offers to display more information. The user enters "Yes," so the bot provides a link to a KB article.](../images/sms-boolean-input.png)

</td></tr><tr><td>

File picker

</td><td>

User sends a file to the bot.**Note:** Conversational SMS Integration with Twilio doesn't support all file types. Only images can be sent in an SMS conversation.

![The bot displays an example image that indicates the serial number location. The user uploads a photo of their product's serial number.](../images/sms-image-input.png)

</td></tr></tbody>
</table>For more information on configuring user input controls, see [Virtual Agent Designer user input controls](../reference/va-user-inputs.md).

The following bot responses are supported in Twilio SMS conversations:

<table id="table_mq2_gqz_2mb"><thead><tr><th>

Bot response

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text

</td><td>

Bot sends a plain text string to the user.![Bot sends a text: "Your order is scheduled for install on Dec 25th between 10am and 1pm. Is this ok?" The user enters YES, and the bot confirms their choice.](../images/sms-bot-text.png)

</td></tr><tr><td>

Image

</td><td>

Bot sends an image to the user.![The bot sends an image that shows the user where to find their product's serial number.](../images/sms-bot-image.png)

</td></tr><tr><td>

Link

</td><td>

Bot sends a web link to the user.![The bot sends an appointment confirmation to the user, who enters CHANGE. The bot responds with a link where the user can view new appointment options.](../images/sms-bot-link.png)

</td></tr><tr><td>

Card

</td><td>

Bot sends selected information from a record on your instance. ![When the user says their router is on fire, the bot creates a case and sends the card with the number, priority, assigned agent, and a link.](../images/sms-bot-card.png)

</td></tr></tbody>
</table>For more information on configuring bot responses, see [Virtual Agent Designer bot responses](../reference/va-bot-responses.md).

Live agents can use the Text, Card, and Image response controls to reply to users in SMS conversations.

## User subscriptions for SMS update notifications

Beginning with version 1.1.1, your users with ServiceNow accounts \(sys\_user profiles\) can choose to start or stop receiving SMS updates in their conversations.

**Note:** Notifications in messaging channels can be sent to users with ServiceNow accounts. Other recipients, such as consumer and customer contacts, are considered to be guests and cannot receive notifications on messaging channels.

To comply with privacy regulations, user notifications are turned off by default. Users can opt in or change their settings in the following ways:

-   To check SMS notification settings for the account, send this text: `Notification`
-   To receive SMS notifications, send this text: `START`
-   To stop receiving SMS notifications, send this text: `STOP`

![The user enters "notifications" to view settings, which are currently on. The user enters STOP, and the bot unsubscribes them. When the user enters START, the bot confirms the re-subscription.](../images/sms-notifications-start-stop.png "Changing SMS notification settings")

To learn more about Virtual Agent notifications, see [Configuring Virtual Agent notifications](configuring-va-notifications.md).

For details about creating content for a messaging notification, see [Define Virtual Agent notification contents](../task/define-va-notif-contents.md).

-   **[Install Conversational SMS Integration with Twilio](../task/install-sms-twilio.md)**  
You can install the Conversational SMS Integration with Twilio \(sn\_va\_sms\_twilio\) application to host Virtual Agent conversations in the SMS Twilio application.
-   **[Set up the Conversational SMS Integration with Twilio](../task/configure-twilio-adapter.md)**  
Integrate Twilio with Virtual Agent so that you can engage in SMS bot conversations.
-   **[Using Conversational SMS Integration with Twilio](using-sms-integ-twilio.md)**  
Enable a requester to converse with an agent using the SMS conversations.
-   **[Configure SMS authentication](../task/configure-sms-auth.md)**  
Authenticate all users using Conversational SMS Integration with Twilio with Soft PIN \(SN\) and Google authenticators as the 2-factor authentication mechanisms for account linking.

**Parent Topic:**[Integrating Virtual Agent with messaging apps](va-integration-messaging-apps.md)

