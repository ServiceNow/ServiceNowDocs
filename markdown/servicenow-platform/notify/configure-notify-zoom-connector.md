---
title: Configure Notify Zoom connector in Notify
description: Configure Notify to receive the event information from Zoom. An event is usually any action that is related to a meeting.
locale: en-US
release: yokohama
product: Notify
classification: notify
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Notify Zoom connector in Notify

Configure Notify to receive the event information from Zoom. An event is usually any action that is related to a meeting.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Zoom** &gt; **Configuration**.

2.  Paste the verification token that you recorded on Zoom Event Subscription screen in the **Webhook validation token** field.

3.  Save the record.


## What to do next

Configure and use Zoom as a conference provider from any of the task records.

**Note:** The person creating a conference is the host of the conference and must have their email set in their ServiceNow profile and use the same email for the Zoom account.

You must be signed in to the browser in order to direct to the Zoom client. However, if you are not signed in, you must provide your registration details.

-   **[Set up Notify Zoom connector in Zoom](setup-notify-zoom-connector.md)**  
Use the Notify Zoom connector to expand the Notify communication channel by managing and initiating a Zoom meeting directly from any task record such as an incident or a change.
-   **[Disable Zoom meeting password](disable-zoom-password.md)**  
Disable Zoom meeting password so that you can join a Zoom meeting without any meeting password.

**Parent Topic:**[Configuring Notify](../concept/configuring-notify.md)

**Related topics**  


[Configure a provider in Notify](configure-providers-for-provider-selectors.md)

[Start a conference call](start-a-conference-call.md)

