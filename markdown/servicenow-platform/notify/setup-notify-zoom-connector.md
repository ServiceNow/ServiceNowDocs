---
title: Set up Notify Zoom connector in Zoom
description: Use the Notify Zoom connector to expand the Notify communication channel by managing and initiating a Zoom meeting directly from any task record such as an incident or a change.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Notify Zoom connector in Notify, Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up Notify Zoom connector in Zoom

Use the Notify Zoom connector to expand the Notify communication channel by managing and initiating a Zoom meeting directly from any task record such as an incident or a change.

## Before you begin

Role required: admin, Zoom admin

1.  Ensure that you have Zoom spoke installed on your instance.
2.  Make sure you have the required credentials and connections to Zoom on your instance.
3.  Configure the Notify Zoom connector with the same Zoom account with which you created the OAuth app for Zoom spoke.

## Procedure

1.  On your Zoom OAuth app, navigate to **Feature** &gt; **Add Feature** &gt; **Event Subscription**.

2.  Use the toggle button to enable the event subscription feature.

3.  In the form that appears, fill in the URL using the following URL format: `[https://yourinstancename.com/api/sn\_notify\_zoom/notify\_zoom/ZoomEvent](https://yourinstancename.com/api/sn_notify_zoom/notify_zoom/ZoomEvent).`

    The URL is used to post information about events in Zoom to your instance.

4.  Use the **Add Events** button to list all the events which Zoom is informing Notify about.

5.  In the categories that appear, select **Meeting** and select all the meeting-related events from the list and click **Done.**

6.  Under **Recording**, select **All Recordings have completed** and **Recording Transcript files have completed** from the list and click **Done**.

7.  Click **Save**on the Add feature screen.

    A **Verification Token** appears on the Add Feature screen.

8.  Record the token by clicking **Copy**.


## What to do next

Configure Notify with the verification token from Zoom.

**Parent Topic:**[Configure Notify Zoom connector in Notify](configure-notify-zoom-connector.md)

**Related topics**  


[Configure Notify Zoom connector in Notify](configure-notify-zoom-connector.md)

