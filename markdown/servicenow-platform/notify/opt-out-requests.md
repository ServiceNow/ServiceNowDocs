---
title: Configure SMS opt-out preferences
description: Allow recipients to opt out of receiving text messages.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Notify, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure SMS opt-out preferences

Allow recipients to opt out of receiving text messages.

## Before you begin

Role required: notify\_setup\_admin, notify\_admin

## About this task

According to regulations in the CTIA Short Code Monitoring Handbook, recipients must be allowed to opt out of receiving text messages. The opt-out functionality is applicable only to Notify. When the user sends an SMS message with an opt-out keyword to any Notify number, the user is opted out of receiving messages from only the Notify number to which the message has been sent, not from all Notify numbers on that instance.

**Important:** The Advanced opt-out feature is automatically enabled for short code and long code numbers associated with a Messaging Service. For more information, refer [Getting Started with Advanced Opt-Out for Messaging Services](https://support.twilio.com/hc/en-us/articles/360034798533-Getting-Started-with-Advanced-Opt-Out-for-Messaging-Services). As this feature is a duplicate of the Twilio's new Advanced Opt-out feature, you should not activate the feature for numbers that are part of Messaging Service. For long code numbers that are not part of a Messaging service, Twilio handles the opt-out for default stop keywords listed at [Twilio support for opt-out keywords](https://support.twilio.com/hc/en-us/articles/223134027-Twilio-support-for-opt-out-keywords-SMS-STOP-filtering-).

This feature is disabled by default and holds significance for short-code and long codes that are not part of Messaging Service. To enable this feature, the Notify admin.

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Administration** &gt; **SMS Preference Configuration**.

2.  Click **New** in the SMS Preference Configuration window.

3.  Fill in the form fields.

<table id="table_otn_32t_shb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Select the provider for which you are configuring the SMS preferences.

</td></tr><tr><td>

Name

</td><td>

A user-friendly name for the configuration.

</td></tr><tr><td>

Order

</td><td>

Order in which the preference configurations apply. If you have multiple configurations, this field indicates which configuration to consider first.

</td></tr><tr><td>

Default preference

</td><td>

The default preference for the configuration. The two options are: -   **Opt-in**: Users by default will receive SMS messages.
-   **Opt-out**: Users by default will not receive SMS messages. They can start receiving SMS messages from a specific Notify number after sending a message with an opt-in keyword like START or BEGIN.


</td></tr><tr><td>

Enable for long code

</td><td>

Option that enables the opt-out feature for long code or toll-free numbers.

</td></tr><tr><td>

Enable for short code

</td><td>

Enables the opt-out feature for short codes only.

</td></tr><tr><td>

Opt-out keywords

</td><td>

Keyword replies that prevent a customer from receiving new messages from the phone number they're responding to. You can configure standard keywords such as STOP, STOPALL, END, CANCEL, QUIT, and UNSUBSCRIBE.

</td></tr><tr><td>

Opt-out confirmation message

</td><td>

Customized confirmation message to send to customers when they opt out of receiving SMS messages.

</td></tr><tr><td>

Opt-in keywords

</td><td>

Customized confirmation responses that enable customers to receive the messages coming from a phone number. You can configure standard keywords such as START, UNSTOP, and YES.

</td></tr><tr><td>

Opt-in confirmation message

</td><td>

A customized confirmation message to send to customers when they opt in to receiving SMS messages.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configuring Notify](../concept/configuring-notify.md)

