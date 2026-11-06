---
title: Setting up the Notify Zoom connector for Zoom extension for Omnichannel Callback
description: Setting up the Notify Zoom connector in Zoom and then in your ServiceNow instance enables your instance to receive event information from Zoom. Events are meeting-related actions, such as a meeting starting or a recording completing.Add event subscriptions to your Zoom OAuth app so that the Notify Zoom connector in your ServiceNow instance receives meeting and recording events from Zoom.Add the Zoom verification token to the Notify Zoom connector configuration in your ServiceNow instance so that your instance can validate and receive event information from Zoom.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/callback-over-zoom/setup-notify-zoom-connector-omni.html
release: australia
product: Callback over Zoom
classification: callback-over-zoom
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Setting up Zoom extension for Omnichannel Callback, Zoom extension for Omnichannel Callback, Manage people and work, Conversational Interfaces]
---

# Setting up the Notify Zoom connector for Zoom extension for Omnichannel Callback

Setting up the Notify Zoom connector in Zoom and then in your ServiceNow instance enables your instance to receive event information from Zoom. Events are meeting-related actions, such as a meeting starting or a recording completing.

**Note:** The interaction stores the Zoom recording URL but not the recording passcode. To make recordings accessible from the interaction, configure the Zoom account so that recordings don't require a passcode.

## Configure the Notify Zoom connector in Zoom

Add event subscriptions to your Zoom OAuth app so that the Notify Zoom connector in your ServiceNow instance receives meeting and recording events from Zoom.

### Before you begin

-   The Notify Zoom Connector and Omnichannel Callback must be installed on your instance.
-   The Zoom spoke must be installed on your instance.
-   A connection and credentials for Zoom must be configured on your instance.
-   The Notify Zoom connector must be configured with the same Zoom account that you used to create the OAuth app for the Zoom spoke.

Role required: admin, Zoom admin

### Procedure

1.  On your Zoom OAuth app, navigate to **Feature** &gt; **Add Feature** &gt; **Event Subscription**.

2.  Enable the event subscription feature.

3.  Select **Add Event Subscription** to add the first event subscription.

4.  Enter the following URL, which Zoom uses to post event information to your instance:

    `https://<instance name>.com/api/sn_notify_zoom/notify_zoom/ZoomEvent`

5.  Select the **Add Events** button.

6.  Select **Meeting** and then select the following events from the list:

    -   **Start Meeting**
    -   **End Meeting**
    -   **Participant/Host joined meeting**
    -   **Participant/Host left meeting**
7.  Select **Recording** and then select **All Recordings have completed** from the list.

8.  Select **Done**.

9.  On the Add feature screen, select **Save** to save the event subscription configuration.

10. Select **Add Event Subscription** to add a second event subscription.

11. Enter the following URL, which Zoom uses to post recording transcript event information to the Zoom spoke on your instance:

    `https://<instance name>.com/api/sn_zoom_spoke/zoom_webhook_endpoint/webhook`

12. Select the **Add Events** button.

13. Select **Recording** and then select **Recording Transcript files have completed** from the list.

14. Select **Done**.

15. In the Add feature section, select **Save** to save the event subscription configuration.

16. In the Token section, select **Copy** and save the verification token for use when you configure the Notify Zoom connector in your ServiceNow instance.


## Configure the Notify Zoom connector in ServiceNow

Add the Zoom verification token to the Notify Zoom connector configuration in your ServiceNow instance so that your instance can validate and receive event information from Zoom.

### Before you begin

You must have the verification token that you copied when you configured the Notify Zoom connector in Zoom.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Zoom** &gt; **Configuration**.

2.  Paste the verification token in the **Webhook validation token** field.

3.  Select **Update**.


### What to do next

For the next step, see [Configure a Zoom webhook for Zoom extension for Omnichannel Callback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/callback-over-zoom/configure-zoom-webhook-omni.md).

