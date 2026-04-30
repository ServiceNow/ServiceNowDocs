---
title: Preview email notifications
description: You can preview what notifications look like before you actually enable the instance to send them.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Preview email notifications

You can preview what notifications look like before you actually enable the instance to send them.

## Before you begin

Role required: admin

## About this task

You can preview both types of notifications as specified by the **Send when** field on the Notification form:

-   **Record inserted or updated**: A change to record in the instance triggers the notification.
-   **Event is fired**: An event, such as the expiration of a certificate or an inbound email action, triggers the notification.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Open the notification or create one.

    You must save the record before you can view the preview accurately.

3.  Click **Preview Notification** on the form header.

4.  On the Notification Preview window, verify that the notification works as expected.

<table id="table_vw4_dxr_wr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Preview records for this breakdown source

</td><td>

The type of event that triggers the notification. This list appears if you preview an event-triggered notification. Select one of the following:-   **Generated Event**: Preview the notification with a generic event that the previewer creates. This does not actually generate an event record.
-   **Existing Event**: Preview with an existing event record in the instance. If you select this option, select the event in the **Event Record** field.


</td></tr><tr><td>

Event Record

</td><td>

An existing event to preview an event-created notification. This option appears if you select **Existing Event** as the event type \(for event-triggered notifications only\).

</td></tr><tr><td>

Event Creator

</td><td>

The user triggering the notification for the preview. The event creator defaults to the user who clicked **Preview Notification**. You can change the creator as needed. You can change the preview record as needed to see the changes in the notification content.

</td></tr><tr><td>

Preview Record

</td><td>

The record triggering the notification for preview. The preview record defaults to one of the records in the table specified in the **Table** field on the Email Notification form. You can change the preview record as needed to see the changes in the notification content.

</td></tr><tr><td>

Users

</td><td>

The users who will receive the notification, as specified in the **Who will receive** section of the Email Notification form: -   All users that you specify on the form appear, but only the users that will actually receive the notification with the current preview settings appear in black text.
-   Users that are specified but for whatever reason will not receive the notification appear in red, strikethrough text. Place the cursor over any of these names to see the reason the user will not receive the notification. For example, one reason could be that the user's notification settings are turned off.


</td></tr><tr><td>

Subject and Body

</td><td>

The content of the notification as defined by the template. The **Subject** and **Body** sections on the preview display the content in the corresponding **Subject** and **Message** fields on the template. If the template includes a link to the record that triggered the notification, the **Preview Record** link is used. Click the link to go to that record.

</td></tr></tbody>
</table>5.  After you have reviewed the notification, exit the preview window.

6.  Make the necessary changes to the notification or template, if necessary.


**Parent Topic:**[Create an email notification](t_CreateANotification.md)

