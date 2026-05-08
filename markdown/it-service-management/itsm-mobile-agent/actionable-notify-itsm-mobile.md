---
title: Configurable actionable notifications for ITSM Mobile Agent
description: With configurable actionable notifications for ITSM Mobile Agent, you can perform actions based on push notifications without having to open the ITSM Mobile Agent application.Create a push notification for various actions performed on the ITSM Mobile Agent application.Create a push action category if any of the pre-defined push action categories do not meet the business requirements.Create a push action if any of the pre-defined push actions do not meet the business requirements.Create a mobile function for each function in the action category. These actions perform tasks on your instance based on what the user selects in the notification.Associate functions to the actions for an actionable push notification.Create the content of the message to be displayed as a notification.Create a record to determine the information to be displayed for a notification.
locale: en-US
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Configurable actionable notifications for ITSM Mobile Agent

With configurable actionable notifications for ITSM Mobile Agent, you can perform actions based on push notifications without having to open the ITSM Mobile Agent application.

You can associate up to three actions with a push notification. These actions must refer to an existing mobile function. The following function types of actions are supported:

-   Action item
-   Navigation
-   URL
-   Chat launcher

![Actionable push notifications](../image/actionable-notifications.png)

## Process for creating actionable push notifications

Create actionable push notifications using the following process:

1.  Create an actionable push notification for ITSM Mobile Agent.
2.  Create a push action category.
3.  Create function for each push action.
4.  Map functions with push actions on the actionable push notification.
5.  Create push message content.
6.  Create a standard notification.

## Create an actionable push notification for ITSM Mobile Agent

Create a push notification for various actions performed on the ITSM Mobile Agent application.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Notifications**.

2.  Click **New**.

3.  In the push notification form, fill in the fields.

<table id="table_xmw_kzw_smb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your push notification.**Note:** This name does not appear to users viewing the notification.

</td></tr><tr><td>

Application

</td><td>

The scoped application for your notification. This field automatically uses the current application scope.

</td></tr><tr><td>

Actionable

</td><td>

Option for making a notification actionable.

</td></tr><tr><td>

Screen

</td><td>

Optional screen associated with your notification. Displays to a user when they tap on the notification.

</td></tr></tbody>
</table>4.  Click **Save**.


### Result

The notification record is created, and the **Push Action Instances** related list appears on the form.

## Create a push action category

Create a push action category if any of the pre-defined push action categories do not meet the business requirements.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Action Categories**.

    |Action|Description|
    |------|-----------|
    |accept-reject-back|Displays **Accept** and **Reject** buttons. Users can select an option without opening the app.|
    |Accept-Reject-fore|Displays **Accept** and **Reject** buttons. The app opens when the user selects an action.|
    |accept-rejectwcomments-back|Displays **Accept** and **Reject** buttons. When users select the **Reject** option, a confirmation dialog box appears that requires the user to provide a message and click Send.|
    |ack-escalate-ignore-back|Displays **Acknowledge**, **Escalate**, and **Ignore** buttons. Users can select an option without opening the app.|
    |approve-reject-back|Displays **Approve** and **Reject** buttons. Users can select an option without opening the app.|
    |approve-rejectwcomments-back|Displays **Approve** and **Reject** buttons. When users select the **Reject** option, a confirmation dialog box appears that requires the user to provide a message and click Send. Users can select an option without opening the app.|
    |confirm-reschedule-cancel-back|Displays **Confirm**, **Reschedule**, and **Cancel** buttons. Users can select an option without opening the app.|
    |joinbridge-fore|Displays a **Join Meeting** button. Tapping this button opens the app.|
    |PromoteWComments-RejectWComments-fore|Displays **Promote** and **Reject** buttons. When users select either option, a confirmation dialog box appears that requires the user to provide a message and click Send.|
    |queuerejoin-openincident-back|Displays **Online Check-in** and **Open Incident** buttons. Users can select an option without opening the app.|
    |queuestay-queueleave-back|Displays **Stay in Queue** and **Leave Queue** buttons. Users can select an option without opening the app.|
    |yes-no-back|Displays **Yes** and **No** buttons. Users can select an option without opening the app.|

2.  Select **New**.

3.  In the push action category form, enter a name for the category in the **Name** field.

4.  Select the lock icon \(![Lock icon](../image/lock-icon.png)\) next to the **Actions** field.

5.  Select the reference icon \(![Reference icon](../image/reference-lookup-icon.png)\) to display the **Push Actions** list and select the actions for the push action category.

6.  Select **Save**.


## Create a push action

Create a push action if any of the pre-defined push actions do not meet the business requirements.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Actions**.

2.  Click **New**.

3.  In the push action form, fill in the fields.

<table id="table_t12_4fm_5mb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Text your users will see in the notification for this action.

</td></tr><tr><td>

Application

</td><td>

Scoped application for this record. This field automatically populates.

</td></tr><tr><td>

Name

</td><td>

Name of the push action.

</td></tr><tr><td>

Foreground

</td><td>

When enabled, the app opens when your users select this action.

</td></tr><tr><td>

Response Type

</td><td>

Options are:-   **Simple**
-   **Text response**


</td></tr><tr><td>

Placeholder Text

</td><td>

Placeholder text to your users when they initiate the actionable push.

</td></tr></tbody>
</table>4.  Click **Save**.


## Create functions for notification push actions

Create a mobile function for each function in the action category. These actions perform tasks on your instance based on what the user selects in the notification.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Functions**.

2.  Click **New** to create a new function record.

3.  Create a function for one of your push actions.

    When selecting a function type in the **Type** field, you must select one of the function types supported for actionable push notifications:

    -   Action item
    -   Navigation
    -   URL
    -   Chat launcher
    For information on function types, and detailed steps for creating functions, see Mobile functions.

4.  Create additional functions for each push action.

    For example, if you have selected `ack-escalate-ignore-back` as your push notification category, your notification displays the **Acknowledge**, **Escalate**, and **Ignore** buttons. Create a function to determine the behavior of each of these buttons.


### What to do next

[Map functions with push actions for actionable push notifications](actionable-notify-itsm-mobile.md#)

## Map functions with push actions for actionable push notifications

Associate functions to the actions for an actionable push notification.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Notifications**.

2.  Open a notification.

3.  In the **Push Action Instances** related list, click **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Push Notification|Push notification associated with this push action instance. This field is automatically filled in with your push notification.|
    |Application|Scoped application associated with this record. This field is automatically filled in with the current application.|
    |Push Action|Push action from your push notification record. Select one of the available actions.|
    |Button|Function to associate with the push action. This action triggers when a user uses the action listed in the **Push Action** field.|

5.  Click **Submit**.


### Example

This example notification uses the accept-rejectwcomments-back in the **Category** field. Clicking the preview icon \(![Preview icon](../image/gac-info-icon.png)\) shows the two actions used by this category: Accept and Reject.

![Push notification displaying a preview of the category record.](../image/action-push-example-1.png)

In the example push action instance, the Approve push action is selected in the **Push Action** field, and the **Approve REQ /w comments** function is selected in the **Button** field. The instance executes this function when a user taps the **Approve** button in the notification.

![Push action instance associating an action with a function.](../image/action-push-example-2.png)

## Create push message content

Create the content of the message to be displayed as a notification.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Notifications**.

2.  Open the notification.

3.  Click **Create Push Message Content** in the Related Links section.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of your push message content record. This name is not visible to your users.|
    |Application|Scoped application associated with this record. This field is automatically filled in with the current application.|
    |Push app|Mobile Agent app on which the push notification is displayed.|
    |Push Message Generation|The script that generates the push notification. When you create message content, this script is automatically generated.|

5.  Click **Submit**.


## Create a standard notification

Create a record to determine the information to be displayed for a notification.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Create Push Notification**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of your notification. This name is not visible to your users.|
    |Active|Option for determining whether the notification is active. The instance does not send inactive notifications to your users.|
    |Table|Table containing the records relating to your notification. For example, notifications about new incidents use the Incident \[incident\] table.|
    |Push Message Only|Indicates the notification is a push message only. This field cannot be changed.|
    |Category|The category for your notification. This field value is **Uncategorized** by default.|

3.  Right-click the form header and select **Save**.

4.  Configure the push message for your standard notification.

    1.  Select to display the **What to Send** tab.

    2.  Select the lock icon \(![Lock icon](../image/lock-icon.png)\) next to the **Push Messages** field.

    3.  Select the reference icon \(![Reference icon](../image/reference-lookup-icon.png)\) to display the **Push Notification Messages** list.

    4.  Select **New**.

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of your push notification message record. This name is not visible to your users.|
        |Application|Scoped application associated with this record. This field defaults to the current application.|
        |Push App|Mobile Agent app on which the push notification is displayed.|
        |Table|Table containing the records relating to your notification. For example, a notification about new incidents would use the Incident \[incident\] table.|
        |Push Message Content|The record for the push message content.|
        |Message|Text the user sees in the push notification, for example, `An incident has been assigned to you`.|

    6.  Select **Submit**.

5.  In the **Notification** form, select **Update**.


