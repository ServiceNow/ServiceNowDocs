---
title: Configurable actionable notifications for ITSM Mobile Agent
description: With configurable actionable notifications for ITSM Mobile Agent, you can act on push notifications without opening the application.Create a push notification for various actions performed on the ITSM Mobile Agent application.Create a push action category when none of the predefined push action categories meets your business requirements.Create a push action if none of the predefined push actions meet your business requirements.Create a mobile function for each function in the action category. These actions perform tasks on your instance based on what the user selects in the notification.Associate functions with push actions so that the instance runs the right function when a user selects an action in a push notification.Create the content of the push message that appears as a notification in the ITSM Mobile Agent app.Create a standard notification record that determines the information users see in a push notification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/actionable-notify-itsm-mobile.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
keywords: [Map functions with push actions]
breadcrumb: [Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Configurable actionable notifications for ITSM Mobile Agent

With configurable actionable notifications for ITSM Mobile Agent, you can act on push notifications without opening the application.

You can associate up to three actions with a push notification. These actions must refer to an existing mobile function. Actions support the following function types:

-   Action item
-   Navigation
-   URL
-   Chat launcher

\[Omitted image "actionable-notifications.png"\] Alt text: Actionable push notifications

## Process for creating actionable push notifications

Create actionable push notifications using the following process:

1.  Create an actionable push notification for ITSM Mobile Agent.
2.  Create a push action category.
3.  Create a function for each push action.
4.  Map functions to push actions on the actionable push notification.
5.  Create push message content.
6.  Create a standard notification.

## Create an actionable push notification for ITSM Mobile Agent

Create a push notification for various actions performed on the ITSM Mobile Agent application.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Notifications**.

2.  Select **New**.

3.  On the push notification form, fill in the fields.

<table id="table_xmw_kzw_smb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the push notification.**Note:** This name doesn't appear to users viewing the notification.

</td></tr><tr><td>

Application

</td><td>

Scoped application for the notification. This field automatically uses the current application scope.

</td></tr><tr><td>

Actionable

</td><td>

Option for making a notification actionable.

</td></tr><tr><td>

Screen

</td><td>

Screen associated with the notification. The screen appears when a user taps the notification.

</td></tr></tbody>
</table>4.  Select **Save**.


### Result

The notification record is created, and the Push Action Instances related list appears on the form.

## Create a push action category

Create a push action category when none of the predefined push action categories meets your business requirements.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Action Categories**.

    |Category|Description|
    |--------|-----------|
    |accept-reject-back|Displays **Accept** and **Reject** buttons. Users can select an option without opening the app.|
    |Accept-Reject-fore|Displays **Accept** and **Reject** buttons. The app opens when the user selects an action.|
    |accept-rejectwcomments-back|Displays **Accept** and **Reject** buttons. When users select the **Reject** option, a confirmation dialog box appears that requires the user to provide a message and select **Send**.|
    |ack-escalate-ignore-back|Displays **Acknowledge**, **Escalate**, and **Ignore** buttons. Users can select an option without opening the app.|
    |approve-reject-back|Displays **Approve** and **Reject** buttons. Users can select an option without opening the app.|
    |approve-rejectwcomments-back|Displays **Approve** and **Reject** buttons. When users select the **Reject** option, a confirmation dialog box appears that requires the user to provide a message and select **Send**. Users can select an option without opening the app.|
    |confirm-reschedule-cancel-back|Displays **Confirm**, **Reschedule**, and **Cancel** buttons. Users can select an option without opening the app.|
    |joinbridge-fore|Displays a **Join Meeting** button. Tapping this button opens the app.|
    |PromoteWComments-RejectWComments-fore|Displays **Promote** and **Reject** buttons. When users select either option, a confirmation dialog box appears that requires the user to provide a message and select **Send**.|
    |queuerejoin-openincident-back|Displays **Online Check-in** and **Open Incident** buttons. Users can select an option without opening the app.|
    |queuestay-queueleave-back|Displays **Stay in Queue** and **Leave Queue** buttons. Users can select an option without opening the app.|
    |yes-no-back|Displays **Yes** and **No** buttons. Users can select an option without opening the app.|

2.  Select **New**.

3.  On the form, enter a name for the category in the **Name** field.

4.  Select the lock icon \(\[Omitted image "lock-icon.png"\] Alt text: Lock icon\) next to the **Actions** field.

5.  Select the reference icon \(\[Omitted image "reference-lookup-icon.png"\] Alt text: Reference icon\) to display the **Push Actions** list and select the actions for the push action category.

6.  Select **Save**.


## Create a push action

Create a push action if none of the predefined push actions meet your business requirements.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Actions**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_t12_4fm_5mb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Text that users see in the notification for this action.

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

When selected, the app opens when users select this action.

</td></tr><tr><td>

Response Type

</td><td>

Options are:-   **Simple**
-   **Text response**


</td></tr><tr><td>

Placeholder Text

</td><td>

Placeholder text that users see when they initiate the actionable push.

</td></tr></tbody>
</table>4.  Select **Save**.


## Create functions for notification push actions

Create a mobile function for each function in the action category. These actions perform tasks on your instance based on what the user selects in the notification.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Functions**.

2.  Select **New** to create a function record.

3.  Create a function for one of your push actions.

    When selecting a function type in the **Type** field, you must select one of the function types supported for actionable push notifications:

    -   Action item
    -   Navigation
    -   URL
    -   Chat launcher
    For information on function types, and detailed steps for creating functions, see [Mobile functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/sg-studio-mobile-button-types.md).

4.  Create additional functions for each push action.

    For example, if you selected **ack-escalate-ignore-back** as your push notification category, your notification displays the **Acknowledge**, **Escalate**, and **Ignore** buttons. Create a function to determine the behavior of each of these buttons.


### What to do next

[Map functions with push actions for actionable push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-mobile-agent/actionable-notify-itsm-mobile.md)

## Map functions with push actions for actionable push notifications

Associate functions with push actions so that the instance runs the right function when a user selects an action in a push notification.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Notifications**.

2.  Open a notification.

3.  In the **Push Action Instances** related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Push Notification|Push notification associated with this push action instance. This field is automatically filled in with your push notification.|
    |Application|Scoped application associated with this record. This field is automatically filled in with the current application.|
    |Push Action|Push action from your push notification record. Select one of the available actions.|
    |Button|Function to associate with the push action. This action triggers when a user selects the action listed in the **Push Action** field.|

5.  Select **Submit**.


### Example

This example notification uses the accept-rejectwcomments-back category in the **Category** field. Selecting the preview icon \(\[Omitted image "gac-info-icon.png"\] Alt text: Preview icon\) shows the two actions used by this category: Accept and Reject.

\[Omitted image "action-push-example-1.png"\] Alt text: Push notification displaying a preview of the category record.

In the example push action instance, the Approve push action is selected in the **Push Action** field, and the **Approve REQ /w comments** function is selected in the **Button** field. The instance executes this function when a user taps the **Approve** button in the notification.

\[Omitted image "action-push-example-2.png"\] Alt text: Push action instance associating an action with a function.

## Create push message content

Create the content of the push message that appears as a notification in the ITSM Mobile Agent app.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Notifications**.

2.  Open the notification.

3.  Select **Create Push Message Content** in the Related Links section.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of your push message content record. This name is not visible to your users.|
    |Application|Scoped application associated with this record. This field is automatically filled in with the current application.|
    |Push app|ITSM Mobile Agent app on which the push notification is displayed.|
    |Push Message Generation|Script that generates the push notification. When you create message content, this script is automatically generated.|

5.  Select **Submit**.


## Create a standard notification

Create a standard notification record that determines the information users see in a push notification.

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
    |Push Message Only|Option that indicates whether the notification is a push message only. This field cannot be changed.|
    |Category|Category for your notification. This field value is **Uncategorized** by default.|

3.  Select the **Additional Action** \(\[Omitted image "AdditionalActions.png"\] Alt text: Additional actions icon\) and then select **Save**.

4.  Configure the push message for your standard notification.

    1.  Select the **What to Send** tab.

    2.  Select the lock icon \(\[Omitted image "lock-icon.png"\] Alt text: Lock icon\) next to the **Push Messages** field.

    3.  Select the reference icon \(\[Omitted image "reference-lookup-icon.png"\] Alt text: Reference icon\) to display the **Push Notification Messages** list.

    4.  Select **New**.

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of your push notification message record. This name is not visible to your users.|
        |Application|Scoped application associated with this record. This field defaults to the current application.|
        |Push App|Mobile Agent app on which the push notification is displayed.|
        |Table|Table containing the records relating to your notification. For example, a notification about new incidents uses the Incident \[incident\] table.|
        |Push Message Content|Record for the push message content.|
        |Message|Text the user sees in the push notification, for example, `An incident has been assigned to you`.|

    6.  Select **Submit**.

5.  On the Notification form, select **Update**.


