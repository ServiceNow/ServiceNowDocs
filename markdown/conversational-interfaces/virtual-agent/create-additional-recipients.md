---
title: Create additional recipients for Virtual Agent notifications
description: Create and define additional recipients for a Virtual Agent notification to be delivered on chat channels or messaging channels.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Create, recipients, Virtual Agent, notifications, chat, messaging, channels]
breadcrumb: [Configuring Virtual Agent notifications, Configure, Virtual Agent, Conversational Interfaces]
---

# Create additional recipients for Virtual Agent notifications

Create and define additional recipients for a Virtual Agent notification to be delivered on chat channels or messaging channels.

## Before you begin

Role required: admin

## About this task

-   The admin can define recipients under the Additional Recipients related list for messaging channels.

    **Note:** Selecting the channel \(chat channel or messaging channel\) is a prerequisite to defining the content for the notification.

-   The admin can define recipients under the Additional Recipients related list for chat and messaging channels using a dynamic condition.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications** and select the notification that you want to create additional recipients for.

2.  In the Additional Recipients related list, select **New**.

3.  On the form, fill in the fields.

<table id="table_e2n_vcf_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notification

</td><td>

Identifier of the notification.The notification name is auto-populated.

</td></tr><tr><td>

Recipient Table

</td><td>

The scope of the recipient record for the notification. The **Recipient Table** field is auto-populated with the user \[sys\_user\] as the default value.

</td></tr><tr><td>

Application

</td><td>

The scope of the recipient record.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification for the defined additional recipients.

</td></tr><tr><td>

Static Recipients

</td><td>

Names of the recipients from the scope of the selected recipient table.

</td></tr><tr><td class="sub-head" colspan="2">

Dynamic Recipients

</td></tr><tr><td>

Dynamic Conditions

</td><td>

Dynamic filter conditions for the defined recipients.The dynamic condition is applicable for both messaging and chat channels.

 This dynamic condition enables you to define the recipients list for a group of users to send a notification.

 Click the refresh icon ![Refresh icon.](../images/refresh-icon.png) next to the **records match condition** link to update the exact number of records matching the latest filter condition. By default, it shows the total number of records in the current table.

**Note:** Only one active record can be added for a particular recipient table. If you want to add another record for the recipient table, you must deactivate the current record.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Configuring Virtual Agent notifications](../concept/configuring-va-notifications.md)

