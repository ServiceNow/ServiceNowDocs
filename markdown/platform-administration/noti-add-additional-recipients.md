---
title: Create and add additional recipients
description: Update the notifications form by adding additional recipients from the Additional Recipients related list to send notifications to.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and update a provider notification for all users, Create provider notification, Provider notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create and add additional recipients

Update the notifications form by adding additional recipients from the Additional Recipients related list to send notifications to.

## Before you begin

Role required: admin and notifications provider admin

## Procedure

1.  Click Additional Recipients related list on the notification form to add new recipients.

    **Note:** An error message about adding content to the notification shows up. See create common content and [create default content](create-default-content.md) to create content for a notification.

2.  Click **New** in the Additional Recipients related list to add additional recipients.

    The Additional Recipients form shows up.

3.  Fill up the fields in the Additional Notification Recipients form.

<table id="table_lb2_gbs_lpb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notification

</td><td>

Name of the notification**Note:** The Notification name auto-populates and the **Recipient Table** field gets User\[sys\_user\] as the default value.

</td></tr><tr><td>

Application

</td><td>

Scope of the recipient record

</td></tr><tr><td>

Recipient Table

</td><td>

Table name of the recipient**Note:** You can also select a non-sys users table.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification

</td></tr><tr><td>

Static Recipients

</td><td>

Names of static recipients of the notification

</td></tr><tr><td>

Dynamic Conditions

</td><td>

Dynamic filter conditions for the users**Note:** Click the refresh button next to the records matching condition link to update the exact number of records matching the latest filter condition. By default, it shows the total number of records in the current table.

Only one active record can be added for a particular recipient table. If you want to add another record for the recipient table, you will have to deactivate the current record.

</td></tr></tbody>
</table>    **Note:** For one recipient table, we can use either static recipients or dynamic conditions.

4.  Click **Submit**.


**Parent Topic:**[Create and update a provider notification for all users](noti-new-update-notification.md)

