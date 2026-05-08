---
title: Working with callback requests using Virtual Agent
description: As a customer, you can request a callback from a customer service agent through a Virtual Agent conversation. You can request an immediate voice callback or schedule a voice or video callback that you can reschedule or cancel.Request an immediate voice callback or schedule a voice or video callback from a Virtual Agent chat on the ServiceNow portal.Reschedule a callback from a Virtual Agent chat on the ServiceNow portal.Cancel a callback from a Virtual Agent chat on the ServiceNow portal.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Callback requests from customers, Use omnichannel callback, Customer communication, Use, Customer Service Management]
---

# Working with callback requests using Virtual Agent

As a customer, you can request a callback from a customer service agent through a Virtual Agent conversation. You can request an immediate voice callback or schedule a voice or video callback that you can reschedule or cancel.

For more information about setting up Omnichannel Callback, refer to [Configuring Omnichannel Callback](https://www.servicenow.com/docs/access?context=configuring-omnichannel-callback&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

## Request a callback from a Virtual Agent chat

Request an immediate voice callback or schedule a voice or video callback from a Virtual Agent chat on the ServiceNow portal.

### Before you begin

Role required: none

### About this task

You can request an immediate callback only for a voice channel. Use the **Schedule for later** option to request a video call.

### Procedure

1.  Navigate to the Customer Service Portal or Consumer Service Portal home page by adding the suffix `/csm` or `/csp` to your instance URL.

    For example: `https://yourportalurl.com/csm`

2.  Select the Chat icon \(![Chat icon for Customer Service portal.](../image/chat_icon.png)\) to open the chat window and begin a Virtual Agent chat.

3.  Select **Show me everything**.

4.  Select **Request a callback**.

5.  Enter your phone number and a reason for requesting the callback.

6.  Select whether to receive an immediate voice callback from an agent or schedule a voice or video callback for later.

<table id="choicetable_x1h_2hr_2wb"><thead><tr><th align="left" id="d87773e181">

Type of callback

</th><th align="left" id="d87773e184">

Action

</th></tr></thead><tbody><tr><td id="d87773e190">

**Immediate voice callback**

</td><td>

Select **Right now**.

</td></tr><tr><td id="d87773e202">

**Scheduled voice or video callback**

</td><td>

1.  Select **Schedule for later**.
2.  Select the type of call.
    -   For a phone call, select **Voice**.
    -   For a video call, select **Zoom**.
3.  Select a date and time from the calendar and select **Schedule**.

The date and time slots indicate the agent's availability.

</td></tr></tbody>
</table>
### Result

-   A callback request is created.
-   The chat shows the details of the callback time, either the estimated time until the agent phones back or the scheduled date and time set for the phone or video call.
-   A confirmation email is sent.

## Reschedule a callback from a Virtual Agent chat

Reschedule a callback from a Virtual Agent chat on the ServiceNow portal.

### Before you begin

Role required: none

### About this task

Only logged-in users can reschedule callbacks.

### Procedure

1.  Navigate to the Customer Service Portal or Consumer Service Portal home page by adding the suffix `/csm` or `/csp` to your instance URL.

    For example: `https://yourportalurl.com/csm`

2.  Select the chat icon \(![Chat icon for Customer Service Portal.](../image/chat_icon.png)\) to open the chat window and begin a Virtual Agent chat.

3.  Select **Show me everything**.

4.  Select **Reschedule a callback**.

5.  Reschedule the upcoming callback request or a different request.

    -   To reschedule the upcoming callback request, select **Yes**.
    -   To reschedule a different request, select it from the list of requests.
6.  Choose a date and time from the calendar and click **Schedule**.

    The date and time slots indicate the agent's availability.


### Result

The request is rescheduled.

A confirmation message is displayed in the chat.

A confirmation email is sent.

## Cancel a callback from a Virtual Agent chat

Cancel a callback from a Virtual Agent chat on the ServiceNow portal.

### Before you begin

Role required: none

### Procedure

1.  Navigate to the Customer Service Portal or Consumer Service Portal home page by adding the suffix `/csm` or `/csp` to your instance URL.

    For example: `https://yourportalurl.com/csm`

2.  Select the chat icon \(![Chat icon for Customer Service Portal.](../image/chat_icon.png)\) to open the chat window and begin a Virtual Agent chat.

3.  Select **Show me everything**.

4.  Select **Cancel a callback**.

5.  Cancel the upcoming callback request or a different request.

    -   To cancel the upcoming callback request, select **Yes**.
    -   To cancel a different request, select it from the list of requests.
6.  Confirm the cancellation in the confirmation message.


### Result

-   The callback request is canceled.
-   The chat shows the details of the canceled callback request.
-   A confirmation email is sent.

