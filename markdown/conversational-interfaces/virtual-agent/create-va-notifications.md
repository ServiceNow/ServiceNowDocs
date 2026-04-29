---
title: Create Virtual Agent notifications
description: Create a notification that is sent directly to users via the Virtual Agent chatbot. The notification specifies when users receive the notification \(triggers for the notification\) and who receives it \(recipients with and without accounts in the User \[sys\_user\] table\).
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Virtual Agent notifications, Configure, Virtual Agent, Conversational Interfaces]
---

# Create Virtual Agent notifications

Create a notification that is sent directly to users via the Virtual Agent chatbot. The notification specifies when users receive the notification \(triggers for the notification\) and who receives it \(recipients with and without accounts in the User \[sys\_user\] table\).

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications** and select **New**.

2.  On the form, fill in the fields.

<table id="table_k4y_lcw_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the notification.

</td></tr><tr><td>

Table

</td><td>

Table to receive notifications about.

</td></tr><tr><td>

Application

</td><td>

Application scope of the notification.

</td></tr><tr><td>

Type

</td><td>

Type of the notification.

</td></tr><tr><td>

Category

</td><td>

Category of the notification. For Virtual Agent, it's chat.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification. The notification is active by default.

</td></tr><tr><td class="sub-head" colspan="2">

Trigger

</td></tr><tr><td>

Triggered By

</td><td>

System action that triggers the notification. You can choose to send the notification after a record is changed or after an event is triggered.

</td></tr><tr><td>

Inserted

</td><td>

Option to send the notification after a record is inserted.

 This field appears when you select **Record Change** in the **Triggered By** field.

</td></tr><tr><td>

Updated

</td><td>

Option to send the notification after a record is updated.

 This field appears when you select **Record Change** in the **Triggered By** field.

</td></tr><tr><td>

Event

</td><td>

Event that triggers the notification. For example, to send a notification after an incident is closed or resolved, you would select the **incident.inactive** event. By default, this event is logged in the system each time a user resolves or closes an incident.

 This field appears when you select **Event** in the **Triggered By** field.

</td></tr><tr><td>

Conditions

</td><td>

Filter to specify the table records that users receive notifications about. For example, to send notifications about top-priority incidents, you would select **Incident \[incident\]** in the **Table** field and set the conditions to **\[Priority\] \[is\] \[1 - Critical\]**.

</td></tr><tr><td class="sub-head" colspan="2">

Recipients

</td></tr><tr><td>

Users

</td><td>

Users who receive the notification.Add users from the static User \(\[sys\_user\] table or its extension tables\) to define recipients for the notification.

**Note:** You can define the recipients for notifications only for chat channels using this field.

</td></tr><tr><td>

Recipients in fields

</td><td>

Record fields that include recipients who receive the notification. For example, to send the notification to the record assignee, select **Assigned to**.Add recipients from the User \[sys\_user\] table or its extension tables to trigger the notification.

 **Note:** You can define the recipients for notifications for both chat channels and messaging channels using this field.

</td></tr><tr><td>

Is originating user included?

</td><td>

Option to include the user who changed the record or triggered the event.

</td></tr></tbody>
</table>3.  Select **Submit**.

    **Note:** Use the **Submit** button for Virtual Agent notifications. The **Submit and Add Common Content** button is for other use cases.


## What to do next

-   [Create additional recipients for Virtual Agent notifications](create-additional-recipients.md).
-   [Define the notification contents](define-va-notif-contents.md).

**Parent Topic:**[Configuring Virtual Agent notifications](../concept/configuring-va-notifications.md)

