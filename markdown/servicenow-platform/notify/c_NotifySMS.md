---
title: Using Notify with SMS
description: Send and receive SMS messages using Notify.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using Notify with SMS

Send and receive SMS messages using Notify.

Notify stores inbound and outbound SMS messages in the Notify Messages \[notify\_message\] table.

Notify supports sending concatenated SMS messages. Messages that exceed 160 characters, or 70 unicode characters, are split into multiple messages. This may affect your total telephony cost because each message can incur a cost. Some mobile carriers, such as Sprint, do not support concatenated SMS messages.

To send SMS messages to an individual recipient, use the Notify API sendSMS method. This method takes one recipient as an input parameter. You can also use the **send SMS** workflow activity.

To send SMS messages to one or more recipients, use the Notify API sendBulkSMS method. This method takes a list as an input parameter and uses one API call to send multiple messages. Include the list of phone numbers in an array in the API call. This method improves performance by streamlining platform checks and Notify number validation.

**Note:** When using SNC.Notify.sendBulkSMS API, instead of simply iterating over the numbers, all the given numbers are sent for SMS to Twilio in one API call. This happens only when Twilio Direct driver is active and Twilio Notify bulk SMS is enabled for the number in Advanced SMS features.

The Notify-Twilio integration provides programmable SMS outbound message status tracking with Status Callbacks. These callbacks can be helpful to see if a message has been delivered, failed, or ran into some other delivery issues.

-   **[SMS Statuses](../reference/r_SMSStatus.md)**  
Every Twilio SMS message request has a status value which describes the current state of the message. Use this information for troubleshooting SMS related incidents/ issues. Here are few descriptions of possible statuses of SMS sent from Notify through Twilio REST API.
-   **[Send an SMS with Zoom meeting invite](../task/send-sms-with-zoom-link.md)**  
Send an SMS with Zoom meeting invite to ensure that the meeting participants or any newly added participant is updated with the meeting details when the meeting host starts the conference or adds a participant to the conference.
-   **[Outbound communication requirements](../reference/r_OutboundRequirements.md)**  
Outbound communications initiated through Notify, such as phone calls and SMS messages, must satisfy recipient number requirements.

**Parent Topic:**[Using Notify](using-notify.md)

