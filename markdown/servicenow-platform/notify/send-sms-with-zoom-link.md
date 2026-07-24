---
title: Send an SMS with Zoom meeting invite
description: Send an SMS with Zoom meeting invite to ensure that the meeting participants or any newly added participant is updated with the meeting details when the meeting host starts the conference or adds a participant to the conference.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/notify/send-sms-with-zoom-link.html
release: australia
product: Notify
classification: notify
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Notify with SMS, Using Notify, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Send an SMS with Zoom meeting invite

Send an SMS with Zoom meeting invite to ensure that the meeting participants or any newly added participant is updated with the meeting details when the meeting host starts the conference or adds a participant to the conference.

## Before you begin

Role required: notify\_view, notify\_admin or notify\_setup\_admin

**Note:** You need a telephony provider like Twilio or Nexmo.

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Zoom** &gt; **Configuration**.

2.  In the **Run Workflow on conference change** field, enter `Notify Zoom: Send SMS on Conference Change`.

    The Notify Zoom: Send SMS on Conference Change workflow is available with the demo data of the Notify Zoom Connector plugin \(sn\_notify\_zoom\).

3.  Click **Update**.


**Parent Topic:**[Using Notify with SMS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/c_NotifySMS.md)

