---
title: Create a messaging notification
description: Notifications define when a message is sent, who it is sent to, and what it contains. To send a notification to Slack or Teams, add a messaging content record to the notification and configure the notification messaging channel. Notifications that require action must be sent to individual users instead of groups.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Notifications in messaging applications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a messaging notification

Notifications define when a message is sent, who it is sent to, and what it contains. To send a notification to Slack or Teams, add a messaging content record to the notification and configure the notification messaging channel. Notifications that require action must be sent to individual users instead of groups.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Messaging** &gt; **Messaging Notifications**.

2.  Click **New**.

3.  Fill in or modify the fields as appropriate.

    ![Identifying the notification](../image/EmailNotifFormTop.png)

<table id="table_tlr_5hd_rdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the notification. Use descriptive names to ensure that your users are able to easily distinguish between notifications.

</td></tr><tr><td>

Table

</td><td>

Select a table to trigger the message. Must be a table or database view within the same application scope.**Note:** Notifications running on the task \[task\] table are not supported. Instead, use a table extended from task.

</td></tr><tr><td>

Category

</td><td>

Select a category for the notification. A category groups related notifications in the system settings.**Note:** Do not leave the category as **Uncategorised**, as users may not be able to find the notification in their list of notifications.

</td></tr><tr><td>

Description

</td><td>

Enter a description for this notification.

</td></tr></tbody>
</table>    **Note:** Notification records are shared between messaging, email, and push notifications. Some fields on the form are not relevant to messaging notification records. Leave fields not described here at their default values.

4.  Click**Advanced view** under **Related links** to switch the advanced view.

    **Note:** Switching to the Advanced view saves the current record.

5.  Open the **When to send** tab and complete the form.

    ![Specifying when to send the notification.](../image/email_notification_when_to_send.png)

    **Note:** If the same trigger generates multiple notifications, the system only sends one notification. The system considers all other notifications, even if they have a different subject and body, as duplicates. The Ignore Duplicates business rule controls this functionality.

<table id="table_ibc_3pb_kr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Send when

</td><td>

Select under what condition the notification is sent: -   When a record is inserted or updated
-   When a particular event is fired
-   When [Notification step](https://www.servicenow.com/docs/access?context=trigger-notification-action-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US) in Flow Designer


</td></tr><tr><td>

Weight

</td><td>

Set a numerical value for the notification priority relative to other notifications with the same target table and recipients. The system only sends the notification with the highest weight. The default value 0 causes the system to always send the notification \(assuming the conditions are met\).

</td></tr><tr><td>

Conditions

</td><td>

Use the condition builder to select the conditions under which this notification is sent. For example, select **Priority** &gt; **greater than** &gt; **3 - Moderate** to send the notification only for High and Critical priority incidents.

</td></tr><tr><td>

Inserted

</td><td>

Select the check box to enable messaging notification when a record is inserted. This field appears when you set the **Send when** field to **Record inserted or updated**.

</td></tr><tr><td>

Updated

</td><td>

Select the check box to enable messaging notification when a record is updated. This field appears when you set the **Send when** field to **Record inserted or updated**.

</td></tr><tr><td>

Event name

</td><td>

Select the event that triggers this notification. This field appears when you set the **Send when** field to **Event is fired**.

</td></tr><tr><td>

Advanced condition

</td><td>

Create a script to define more filter conditions, like sending a notification based on the current messaging record, changing field values, or changing system properties. [The advanced condition](../concept/c_OptSpecifyingAdvancedCond.md) script must return **true** or set a global answer variable to **true** to send the notification.

 The advanced condition script uses the following global variables:

 -   **current**: Contains the current record from the table to which the notification is linked.
-   **event**: Contains the event that triggered the notification.
 **Note:** The **Advanced condition** field is evaluated in addition to other conditions you set on the notification. Both the condition and advanced condition must evaluate to true to send the notification.

</td></tr></tbody>
</table>6.  Open the **Who will receive** tab and fill in or modify the following fields.

<table id="table_oh2_krb_kr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Messaging Channels

</td><td>

Select the messaging channels to receive the messaging notification. Only complete this field if creating a simple notification to send to a channel. Simple notifications use a Messaging Content record of Type **Simple**.

</td></tr><tr><td>

Users

</td><td>

Select the users you want to receive the messaging notification. Only complete this field if creating a notification that requires user action. Notifications that require user action use a Messaging Content record of Type **Buttons**.

</td></tr><tr><td>

Users/groups in fields

</td><td>

Select users or groups from reference fields. For example, if a notification uses the Incident \[incident\] table, you can select users or groups from incident fields like **Opened by** and **Assignment group**. **Note:** You can dot-walk to values in reference fields by clicking the plus sign in the field selector and then selecting the related field.

If you address the notification to a user with an inactive record in the User \[sys\_user\] table, the system does not send the notification to that user.

</td></tr><tr><td>

Groups

</td><td>

Select the groups you want to receive the messaging notification. You can search for groups with the reference lookup icon or by manually entering the group name. This list of groups is static.

</td></tr><tr><td>

Send to event creator

</td><td>

Select this check box to send the notification to the person who performed the action that started the notification process if the person is also a recipient. If the event creator is not specified in one of the recipient fields, the event creator does not receive a notification, regardless of the setting in this field. For new notifications, this option is selected by default.

</td></tr><tr><td>

Event parm 1 contains recipient

</td><td>

Select this check box if the event parameter 1 contains one or more notification recipients \(in a comma separated-list\). This field is visible only when the **Send when** field is set to **Event is fired**.

</td></tr><tr><td>

Event parm 2 contains recipient

</td><td>

Select this check box if the event parameter 2 contains one or more notification recipients \(in a comma-separated list\). This field is visible only when the **Send when** field is set to **Event is fired**.

</td></tr></tbody>
</table>7.  Open the **What it will contain** tab and fill in or modify the following fields.

    |Field|Description|
    |-----|-----------|
    |Messaging content|Select a messaging content record to be used in this notification.|

8.  Click **Update**.


**Parent Topic:**[Notifications in messaging applications](../concept/messaging-integration.md)

