---
title: Working with callback requests using the Customer Service Portal
description: As a customer, you can request a callback from a customer service agent using the Customer Service Portal. You can request an immediate callback or schedule a voice or video callback that you can reschedule or cancel.Request an immediate voice callback or schedule a voice or video callback from an agent using the Customer or Consumer Service Portal.Reschedule a callback from an agent using the Customer or Consumer Service Portal.Cancel a callback from an agent using the Customer or Consumer Service Portal.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with callback requests from an agent, Using Omnichannel Callback for Customer Service Management, Customer communication, Using Customer Service Management, Customer Service Management]
---

# Working with callback requests using the Customer Service Portal

As a customer, you can request a callback from a customer service agent using the Customer Service Portal. You can request an immediate callback or schedule a voice or video callback that you can reschedule or cancel.

## Request a callback using the Customer Service or Consumer Service Portal

Request an immediate voice callback or schedule a voice or video callback from an agent using the Customer or Consumer Service Portal.

### Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.consumer

### About this task

You can request an immediate callback only for a voice channel. Use the **Call me later** option to request a video call.

### Procedure

1.  Navigate to the Customer Service Portal or Consumer Service Portal home page by adding the suffix `/csm` or `/csp` to your instance URL.

    For example: `https://yourportalurl.com/csm`

2.  Select **My Lists** in the portal header and then select **My cases**.

3.  Select the case for which you need support.

4.  In the **Actions** section, select **Request callback**.

5.  In the Request a callback pop-up window, enter your name, phone number, issue type, and description.

6.  Select whether to receive an immediate voice callback from an agent or schedule a voice or video callback for later.

<table id="choicetable_dlg_q4r_2wb"><thead><tr><th align="left" id="d91144e160">

Type of callback

</th><th align="left" id="d91144e163">

Action

</th></tr></thead><tbody><tr><td id="d91144e169">

**Immediate voice callback**

</td><td>

Select **Call me now**.

</td></tr><tr><td id="d91144e181">

**Scheduled voice or video callback**

</td><td>

1.  Select **Call me later**.
2.  Select the type of call.
    -   For a phone call, select **Voice**.
    -   For a video call, select **Zoom**.
3.  Select a date and time from the calendar.

The date and time slots indicate the agent's availability.

</td></tr></tbody>
</table>7.  Select **Submit**.


### Result

-   A callback request is created.
-   The details of the callback request are available in the Callback tab.
-   A confirmation email is sent.

## Reschedule a callback using the Customer Service or Consumer Service Portal

Reschedule a callback from an agent using the Customer or Consumer Service Portal.

### Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.consumer

### About this task

You can reschedule a callback request to receive a phone or video call from an agent.

### Procedure

1.  Navigate to the Customer Service Portal or Consumer Service Portal home page by adding the suffix `/csm` or `/csp` to your instance URL.

    For example: `https://yourportalurl.com/csm`

2.  Select **My Lists** in the portal header and then select **My cases**.

3.  Select the case for which you need support.

4.  In the **Callbacks** tab, select the callback request that you want to reschedule.

5.  Select **Reschedule**.

6.  Choose a date and time from the calendar.

    The date and time slots indicate the agent's availability.

7.  Select **Submit**.


### Result

-   The callback request is rescheduled.
-   The pop-up window shows the details of the rescheduled callback.
-   A confirmation email is sent.

## Cancel a callback using the Customer Service or Consumer Service Portal

Cancel a callback from an agent using the Customer or Consumer Service Portal.

### Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.consumer

### Procedure

1.  Navigate to the Customer Service Portal or Consumer Service Portal home page by adding the suffix `/csm` or `/csp` to your instance URL.

    For example: `https://yourportalurl.com/csm`

2.  Select **My Lists** in the portal header and then select **My cases**.

3.  Select the case for which you need support.

4.  In the **Callbacks** tab, select the callback request that you want to cancel.

5.  Select **Cancel**.

6.  Confirm the cancellation in the confirmation message.


### Result

-   The callback request is canceled.
-   The details of the canceled callback request are available in the **Callbacks** tab.
-   A confirmation email is sent.

