---
title: Setting up Notify Zoom connector for Zoom extension for Omnichannel Callback
description: Setting up the Notify Zoom connector in Zoom and then in your ServiceNow instance enables your instance to receive the event information from Zoom. An event is usually any action that is related to a meeting.Configure the Notify Zoom connector in Zoom to receive event information in your ServiceNow instance from Zoom.Configure Notify in your ServiceNow instance to receive event information from Zoom.
locale: en-US
release: yokohama
product: Callback over Zoom
classification: callback-over-zoom
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Zoom extension for Omnichannel Callback, Zoom extension for Omnichannel Callback, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Setting up Notify Zoom connector for Zoom extension for Omnichannel Callback

Setting up the Notify Zoom connector in Zoom and then in your ServiceNow instance enables your instance to receive the event information from Zoom. An event is usually any action that is related to a meeting.

**Note:** Currently, only the Zoom recording URL without passcode is stored in the interaction. You can configure the Zoom account to disable the passcode option.

## Configure the Notify Zoom connector in Zoom

Configure the Notify Zoom connector in Zoom to receive event information in your ServiceNow instance from Zoom.

### Before you begin

-   Ensure that Notify Zoom Connector and Omnichannel Callback are installed on your instance.
-   Ensure that you have the Zoom spoke installed on your instance.
-   Make sure you have the required credentials for and connections to Zoom on your instance.
-   The Notify Zoom connector must have been configured with the same Zoom account with which you created the OAuth app for the Zoom spoke.

Role required: admin, Zoom admin

### Procedure

1.  On your Zoom OAuth app, navigate to **Feature** &gt; **Add Feature** &gt; **Event Subscription**.

2.  Enable the event subscription feature.

3.  Select **Add Event Subscription** to add the first event subscription.

4.  Enter the URL to be used to post information about events in Zoom to your instance:

    `https://<instance name>.com/api/sn_notify_zoom/notify_zoom/ZoomEvent`

5.  Select the **Add Events** button.

6.  Select **Meeting** and then select the following meetings from the list:

    -   Start Meeting
    -   End Meeting
    -   Participant/Host joined meeting
    -   Participant/Host left meeting
7.  Select **Recording** and then select **All Recordings have completed** from the list.

8.  Select **Done**.

9.  On the Add feature screen, select **Save** to save the event subscription configuration.

10. Select **Add Event Subscription** to add a second event subscription.

11. In the form, enter the URL used to post information about events in Zoom to your instance:

    `https://<instance name>.com/api/sn_zoom_spoke/zoom_webhook_endpoint/webhook`

12. Select the **Add Events** button.

13. Select **Recording** and then select **Recording Transcript files have completed** from the list.

14. Select **Done**.

15. In the Add feature section, select **Save** to save the event subscription configuration.

16. In the Token section, select **Copy** to record the verification token to be used during configuration of the Notify Zoom connector.


## Configure the Notify Zoom connector in ServiceNow

Configure Notify in your ServiceNow instance to receive event information from Zoom.

### Before you begin

You must have copied the verification token displayed during the configuration of the Notify Zoom connector in Zoom.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Zoom** &gt; **Configuration**.

2.  Paste the verification token in the **Webhook validation token** field.

3.  Select **Update**.


### What to do next

[Configure a Zoom webhook for Zoom extension for Omnichannel Callback](../Task/configure-zoom-webhook-omni.md)

