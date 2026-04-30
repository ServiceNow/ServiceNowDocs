---
title: Add a push action category
description: Select a push category to determine what actions your users can take in a notification. This category defines which actions your users can take when viewing a notification.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure actionable push notifications, Push notifications, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add a push action category

Select a push category to determine what actions your users can take in a notification. This category defines which actions your users can take when viewing a notification.

## Before you begin

Role required: admin

## Procedure

1.  In the **Push Notification** record, select a category in the **Category** field.

    There are 12 base system categories to choose from on your instance.

    |Action|Description|
    |------|-----------|
    |accept-reject-back|Displays **Accept** and **Reject** buttons. Users can select an option without opening the app.|
    |Accept-Reject-fore|Displays **Accept** and **Reject** buttons. The app opens when the user selects an action.|
    |accept-rejectwcomments-back|Displays **Accept** and **Reject** buttons. Users see a text field to enter comments when they select the **Reject** option. Users can select an option without opening the app.|
    |ack-escalate-ignore-back|Displays **Acknowledge**, **Escalate** and **Ignore** buttons. Users can select an option without opening the app.|
    |approve-reject-back|Displays **Approve** and **Reject** buttons. Users can select an option without opening the app.|
    |approve-rejectwcomments-back|Displays **Approve** and **Reject** buttons. Users see a text field to enter comments when they select the **Reject** option. Users can select an option without opening the app.|
    |confirm-reschedule-cancel-back|Displays **Confirm**, **Reschedule** and **Cancel** buttons. Users can select an option without opening the app.|
    |joinbridge-fore|Displays a **Join Meeting** button. tapping this button opens the app.|
    |PromoteWComments-RejectWComments-fore|Displays **Promote** and **Reject** buttons. Users see a text field to enter comments when they select either option.|
    |queuerejoin-openincident-back|Displays **Online Check-in** and **Open Incident** buttons. Users can select an option without opening the app.|
    |queuestay-queueleave-back|Displays **Stay in Queue** and **Leave Queue** buttons. Users can select an option without opening the app.|
    |yes-no-back|Displays **Yes** and **No** buttons. Users can select an option without opening the app.|

    If the base system push action categories do not meet your requirements, you can create new action categories for use in your push notifications. See the section below for details on this process.

    Your push notification displays buttons to your user in addition to the message content. In the next steps, you create functions that determine what happens when a users taps these actions.

2.  Right-click the form header and click **Save**.


**Parent Topic:**[Configure actionable push notifications](../concept/actionable-push-notification.md)

