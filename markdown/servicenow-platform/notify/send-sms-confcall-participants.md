---
title: Send a message to conference call participants
description: Send a brief message as a text or voice message to the participants of a conference call to set a context to the call.
locale: en-US
release: yokohama
product: Notify
classification: notify
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Notify for making conference calls, Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Send a message to conference call participants

Send a brief message as a text or voice message to the participants of a conference call to set a context to the call.

## Before you begin

Role required: notify\_view, or major incident manager

## About this task

You must configure a telephony provider like Twilio so that you can use one of the Notify numbers to send SMS to the conference call participants.

## Procedure

1.  Navigate to **All** &gt; **Major Incident Management** &gt; **View Workbench**.

2.  In the **Conference** tab, select the type of the call and click **Start Call**.

3.  In the **Include a brief message for participants** field, type the message that you want to send to the conference call participants and click **Start Call**.

    ![Initiating a conference call.](../image/StartCall.png "Initiate a conference call")

    **Note:** Upon clicking **Start Call** the message text entered will be stored as description on the conference call record. If the OOB workflow is not modified, then the workflow takes care of sending this message text as SMS to the user. This is applicable if you have configured a telephony provider.


**Parent Topic:**[Using Notify for making conference calls](../concept/c_NotifyConferenceCalls.md)

