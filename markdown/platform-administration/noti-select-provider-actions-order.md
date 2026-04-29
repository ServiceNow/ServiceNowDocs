---
title: Add actions to the notification content
description: Use the Link Actions to Content related list to add actions to the notification content, selection of the provider notification and ordering of actions of an actionable content.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create, Provider notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Add actions to the notification content

Use the Link Actions to Content related list to add actions to the notification content, selection of the provider notification and ordering of actions of an actionable content.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

2.  Select **New** to create a notification, or select an existing notification.

    **Note:** If the notification includes one or more actions, a message appears to remind you to ensure the actions are associated with content.

3.  In the related lists section, select the Link Actions to Content related list.

4.  Select **New** to create an actionable content.

5.  On the form, fill in the fields.

<table id="table_lb2_gbs_lpb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the action set.

</td></tr><tr><td>

Application

</td><td>

Scope of the notification.

</td></tr><tr><td>

Notification

</td><td>

Name of the notification.

</td></tr><tr><td>

Actions

</td><td>

Option to select the actions.**Note:** You can also set the order of actions of an actionable content.

</td></tr><tr><td>

Content

</td><td>

Option to select the content to apply to the selected action.

</td></tr><tr><td>

Active

</td><td>

Option to activate the action set.

</td></tr><tr><td>

Action\(s\) listed in event parm1

</td><td>

Option to link actions from event parm1. Actions must be sys\_ids from the **sys\_notification\_action** table.

</td></tr><tr><td>

Action\(s\) listed in event parm2

</td><td>

Option to link actions from event parm2. Actions must be sys\_ids from the **sys\_notification\_action** table.

</td></tr></tbody>
</table>6.  Select **Submit**.


**Parent Topic:**[Create provider notification](../concept/create-provider-notification-using.md)

