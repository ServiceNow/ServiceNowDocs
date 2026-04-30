---
title: Configure Notify with Twilio
description: Configure Notify to use the Twilio telephony service.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Notify with Twilio

Configure Notify to use the Twilio telephony service.

## Before you begin

You must have an SID and authentication token for an active Twilio account \(https://www.twilio.com/\). You must have a separate contract with Twilio.

You must exclusively use a Twilio account to connect your ServiceNow instance.

**Important:** Ensure that each instance on which you configure Notify uses a different Twilio account. Each account specifies a unique account SID, authentication token, telephone numbers, and endpoint. Using the same account across multiple instances may cause your Twilio service configuration to be overwritten.

Account and sub-account are Twilio categorizations, and both act the same for a ServiceNow instance.

Role required: notify\_admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Administration** &gt; **Twilio Direct Configuration**.

2.  On the Twilio Account Properties page, enter your **Account SID**.

3.  Enter your **Auth Token**.

4.  Click **Connect**.

    If the account is not associated with an instance and the connection is successful, a read-only list of E.164 and short code phone numbers associated with this Twilio account appears. This list displays the phone number, supported capabilities such as voice or SMS, the country for each Twilio number, and the Notify number group to which the number belongs.

    If the account is already associated with an instance, the system displays an error message. To connect to this account,

    -   [Disconnect the account from the instance](t_disconnect-from-Twilio-account.md).
    -   Delete the TwiML apps in the Twilio account.
    **Note:** If you buy or release numbers on the Twilio account, open the configuration page again to refresh the list of numbers. Numbers removed from the Twilio service remain as Notify Number records, but with the **Active** field set to false. Use only active phone numbers for inbound or outbound communication.


## What to do next

Phone numbers and short codes are provided by Twilio once the account is successfully connected and are stored on the Notify Phone Numbers \[notify\_number\] table. Assign each number to a number group. Number groups allow you to control which workflows run when using the phone numbers in each number group.

-   **[Twilio-Direct callback testing](callback-testing.md)**  
Make an outgoing call or send an SMS using Twilio and trigger callbacks to ServiceNow to test whether Twilio can reach the instance. You can also view when the last callback test was run, its status, and the test logs.
-   **[Advanced configuration for SMS](t_ConfigureNotifyforVoiceandSMS.md)**  
Use the Twilio co-pilot features to improve SMS delivery with phone number like using multiple numbers to send high-volume messages and content intelligence to automatically format every message without writing custom code. Reach large lists of users with one API request.
-   **[Advanced configuration for voice](advanced-configure-voice.md)**  
Configure Answering Machine Detection \(AMD\) to determine if a human has picked up the call or not.
-   **[Disconnect from a Twilio account](t_disconnect-from-Twilio-account.md)**  
If a Twilio account is already associated with a different system, disconnect the account from the other system before connecting to the current instance.
-   **[Configure Amazon Polly as default voice tone for text to speech](configure-amazon-polly-voice-tone.md)**  
You can configure Amazon Polly as the default voice by overriding the default voice tone for text to speech.

**Parent Topic:**[Configuring Notify](../concept/configuring-notify.md)

