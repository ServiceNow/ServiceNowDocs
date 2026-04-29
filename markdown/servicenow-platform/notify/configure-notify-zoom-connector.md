---
title: Configure Notify Zoom connector in Notify
description: Configure Notify to receive the event information from Zoom. An event is usually any action that is related to a meeting.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Notify, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Notify Zoom connector in Notify

Configure Notify to receive the event information from Zoom. An event is usually any action that is related to a meeting.

## Before you begin

Role required: notify\_setup\_admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Zoom** &gt; **Configuration**.

2.  On the zoom configuration table, select **Main**.

3.  On the form, fill in the details:

<table id="table_jyz_n2g_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Webhook secret token

</td><td>

Copy the verification token that you recorded on Zoom Event Subscription screen. The Webhook secret token is used to verify event notifications sent by Zoom provider.**Note:** This is a mandatory field.

</td></tr><tr><td>

Run subflow on conference change

</td><td>

Subflow that is run when zoom conference call is started, or participants are added to the call.

</td></tr><tr><td>

Do not set password

</td><td>

Select the check box to not set password for Zoom conferences.

</td></tr><tr><td>

Zoom transcript handling

</td><td>

Select on how you want the Zoom transcript to be handled when you record the meeting in Zoom and after the meeting ends. Available options:-   Do not process or store the transcript - The transcript is not processed and stored in the system.
-   Store only the link to the transcript - The URL link to the transcript that is sent by the Zoom provider is stored in the system. This is the default value.
-   Download and store the transcript as attachment - The transcript is downloaded from the Zoom server and stored in the system. as an attachment in **.vtt** format.
**Note:** By default, this field is set to **Store only the link to the transcript**.

</td></tr><tr><td>

Store zoom summary

</td><td>

Select the check box to store the Zoom summary that is sent by Zoom provider.**Note:** By default, this check box is cleared.

</td></tr></tbody>
</table>4.  Select **Update**.


## What to do next

Configure and use Zoom as a conference provider from any of the task records.

**Note:** The person creating the conference is the host of the conference and must have their email set in their ServiceNow profile and use the same email for the Zoom account.

You must sign in to the browser in order to direct to the Zoom client. However, if you are not signed in, you must provide your registration details.

-   **[Set up Notify Zoom connector in Zoom](setup-notify-zoom-connector.md)**  
Use the Notify Zoom connector to expand the Notify communication channel by managing and initiating a Zoom meeting directly from any task record such as an incident or a change.
-   **[Disable Zoom meeting password](disable-zoom-password.md)**  
Disable Zoom meeting password so that you can join a Zoom meeting without any meeting password.

**Parent Topic:**[Configuring Notify](../concept/configuring-notify.md)

**Related topics**  


[Configure a provider in Notify](configure-providers-for-provider-selectors.md)

[Start a conference call](start-a-conference-call.md)

