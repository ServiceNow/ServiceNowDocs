---
title: Create and update a provider notification for all users
description: Create a notification in the notification provider framework to send to both sys and non-sys users.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create, Provider notifications, Notifications, Configure core features, Administer]
---

# Create and update a provider notification for all users

Create a notification in the notification provider framework to send to both sys and non-sys users.

## Before you begin

Role required: notifications provider admin and admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

2.  Select **New** to create a notification.

3.  On the form, fill in the fields.

<table id="table_lb2_gbs_lpb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the notification.

</td></tr><tr><td>

Application

</td><td>

Scope of the notification record.

</td></tr><tr><td>

Category

</td><td>

Select the category to which this notification belongs. A category identifies and groups related notifications. This notification, if active and listed in the selected **Category** in the notification preferences for each user \(Notifications tab in the System Settings window\).

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification.

</td></tr><tr><td>

Triggered By

</td><td>

Trigger used in the notification record.**Note:** The options in this field depend on the selected table. For example, if you select an incident table, the options are Events or Record Change.

</td></tr><tr><td>

Table

</td><td>

The table name on which the notification is triggered.

</td></tr><tr><td>

Inserted

</td><td>

Condition to trigger the notification.

</td></tr><tr><td>

Updated

</td><td>

Condition to trigger the notification.

</td></tr><tr><td>

Event

</td><td>

Event that triggers the notification. For example, to send a notification after an incident is closed or resolved, you would select the **incident.inactive** event. By default, this event is logged in the system each time an incident is resolved or closed.

 **Note:** You can select only an event that shares the same table as the notification.

 This field appears when you select **Event** in the **Triggered By** field.

</td></tr><tr><td>

Conditions

</td><td>

Additional conditions to trigger the notification.

</td></tr><tr><td>

Users

</td><td>

Names of the available sys users.

</td></tr><tr><td>

Recipients in fields

</td><td>

Field in the currently selected table that contains the users or groups who receive a notification.**Note:** The **Recipients in fields** field under Recipients enables you to choose both sys and non-sys users to whom you can send notifications.

</td></tr><tr><td>

Is the originating user included?

</td><td>

Option to include the originating user to be included in the notification.

</td></tr><tr><td>

Event Parm1 contains recipient\(s\)?

</td><td>

Option to select if Parm 1 contains a list of comma-separated sys\_ids.

</td></tr><tr><td>

Event Parm2 contains recipient\(s\)?

</td><td>

Option to select if Parm 2 contains a list of comma-separated sys\_ids.

</td></tr><tr><td>

Resolve Parm1 recipients from table

</td><td>

Table that is used to resolve the sys\_id of a Parm 1 recipient.**Note:** This field appears only when you select Event Parm 1.

</td></tr><tr><td>

Resolve Parm2 recipients from table

</td><td>

Table that is used to resolve the sys\_id of a Parm 2 recipient.**Note:** This field appears only when you select Event Parm 2.

</td></tr><tr><td>

Advanced event condition

</td><td>

Option to select when the recipients are from more than 2 tables. These options are dynamic conditions.

</td></tr><tr><td>

Advanced condition

</td><td>

Create a script to perform certain actions, like sending a notification based on the current email record, changing field values, or changing system properties. [The advanced condition](../concept/c_OptSpecifyingAdvancedCond.md) script must return **true** or set a global answer variable to **true** to send the notification.

The advanced condition script uses the following global variables:

-   **current**: Contains the current record from the table to which the notification is linked.
-   **event**: Contains the event that triggered the notification.
**Note:** The **Advanced condition** field is evaluated in addition to other conditions that you set on the notification. Both the condition and advanced condition must evaluate to true to send the notification.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Open the recently created notification.

6.  Update the form using any of the available related lists.

    See [Create and add additional recipients](noti-add-additional-recipients.md) and [Create and add assignment groups](create-add-assignment-group.md) for more information.

    **Note:** All the validation messages given by different providers are retained. Warning messages of one provider isn’t overridden by warning messages of another provider.


-   **[Create and add additional recipients](noti-add-additional-recipients.md)**  
Update the notifications form by adding additional recipients from the Additional Recipients related list to send notifications to.
-   **[Create and add assignment groups](create-add-assignment-group.md)**  
Create and add assignment groups where you want users that are part of a group to be the recipients of the provider notification.

**Parent Topic:**[Create provider notification](../concept/create-provider-notification-using.md)

