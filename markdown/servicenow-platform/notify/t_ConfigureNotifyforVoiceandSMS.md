---
title: Advanced configuration for SMS
description: Use the Twilio co-pilot features to improve SMS delivery with phone number like using multiple numbers to send high-volume messages and content intelligence to automatically format every message without writing custom code. Reach large lists of users with one API request.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Notify with Twilio, Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Advanced configuration for SMS

Use the Twilio co-pilot features to improve SMS delivery with phone number like using multiple numbers to send high-volume messages and content intelligence to automatically format every message without writing custom code. Reach large lists of users with one API request.

## Before you begin

Role required: notify\_admin

## About this task

The Twilio co-pilot features are enabled in your instance once configured. An example of a copilot feature is that you can configure which identity \(phone number, shortcode, or alpha sender ID\) to use to send a message. You can also spread the messaging traffic over several phone numbers or prioritize an alpha sender ID when sending messages to countries where alpha senders are commonly used. To know more about these features, visit [https://www.twilio.com/copilot](https://www.twilio.com/copilot).

**Important:** All the Twilio numbers must be part of the same messaging service for which you have enabled the **Advance SMS Features** feature.

The Twilio Notify bulk SMS feature is used to send SMS in bulk to customers. Use the passthrough sendBulkSMS API to reach large number of users across using a single API request. For more information on these features visit [https://www.twilio.com/notify](https://www.twilio.com/notify)

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Administration** &gt; **Twilio Direct Configuration**.

2.  On the Twilio Account Properties page, enter your **Account SID**.

3.  Enter your **Auth Token**.

4.  Click **Connect**.

5.  On the **Advance SMS Features** tab, check the **Intelligent SMS Handling** box.

    **Note:** To setup Alpha Sender ID, users need to go to Twilio console.

    When you enable **Intelligent SMS Handling**, the "Messaging Service SID" is used to send the SMS even if a Twilio number is used in Notify.sendSMS API.

6.  On the **Advance SMS Features** tab, check the **Twilio Notify Bulk SMS** box.

    **Note:** This feature uses Twilio Notify feature and might have an associated cost. Contact Twilio Support for more details.


**Parent Topic:**[Configure Notify with Twilio](t_ConfigureNotifyWithTwilio.md)

**Related topics**  


[Using Notify with SMS](../concept/c_NotifySMS.md)

