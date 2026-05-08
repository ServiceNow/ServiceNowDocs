---
title: Create custom notifications in Next Experience
description: Provide better context and information about users' work by creating custom content for in-product notifications in Next Experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Create custom notifications in Next Experience

Provide better context and information about users' work by creating custom content for in-product notifications in Next Experience.

## Before you begin

Role required: admin

## About this task

Create notifications with custom title and message content for your applications and use cases. Next Experience notifications appear as toast banners and in the Notifications menu.

**Note:** Next Experience notifications aren’t supported in the legacy Agent Workspace.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="id_tw3_421_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the notification.

</td></tr><tr><td>

Application

</td><td>

Application scope of the notification.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification. The notification is active by default.

</td></tr><tr><td class="sub-head" colspan="2">

When to send

</td></tr><tr><td>

Trigger

</td><td>

System action that triggers the notification. You can send the notification after a record is changed or after an event is triggered.

</td></tr><tr><td>

Inserted

</td><td>

Option to send the notification after a record is inserted.

 This field appears when you select **Record Change** in the **Trigger** field.

</td></tr><tr><td>

Updated

</td><td>

Option to send the notification after a record is updated.

 This field appears when you select **Record Change** in the **Trigger** field.

</td></tr><tr><td>

Event

</td><td>

Event that triggers the notification. For example, to send a notification after an incident is closed or resolved, you would select the **incident.inactive** event. By default, this event is logged in the system each time a user resolves or closes an incident.

 **Note:** You can select only an event that shares the same table as the notification.

 This field appears when you select **Event** in the **Trigger** field.

</td></tr><tr><td>

Table

</td><td>

Table to receive notifications about.

</td></tr><tr><td>

Conditions

</td><td>

Filter to specify the table records that users receive notifications about. For example, to send notifications about top-priority incidents, you would select **Incident \[incident\]** in the **Table** field and set the conditions to **\[Priority\] \[is\] \[1 - Critical\]**.

</td></tr><tr><td class="sub-head" colspan="2">

Who will receive

</td></tr><tr><td>

Users

</td><td>

Users who receive the notification.**Note:** Notifications in messaging channels are sent only to users with ServiceNow accounts \(sys\_user profiles\). Consumers and customer contacts are considered as guests and can’t receive notifications in messaging channels.

</td></tr><tr><td>

Recipients listed in fields

</td><td>

Record fields that include users who receive the notification. For example, to send the notification to the record assignee, select **Assigned to**.**Note:** This field shows up only if you select a table.

</td></tr><tr><td>

Include the person whose action triggered the notification

</td><td>

Option to include the user who changed the record or triggered the event.

</td></tr><tr><td>

Recipient\(s\) listed in event parm1

</td><td>

Option to select whether Parm 1 contains a list of comma-separated sys\_ids. For more information, see Classic Events.

</td></tr><tr><td>

Recipient\(s\) listed in event parm2

</td><td>

Option to select if Parm 2 contains a list of comma-separated sys\_ids

</td></tr><tr><td>

Table containing recipients from event parm1

</td><td>

Table that is used to resolve the sys\_id of the recipient**Note:** This field appears only when you select Event parm 1.

</td></tr><tr><td>

Table containing recipients from event parm1

</td><td>

Table that is used to resolve the sys\_id of the recipient**Note:** This field appears only when you select Event parm 2.

</td></tr><tr><td>

Advanced event condition

</td><td>

Option to select when the recipients are from more than two tables. These are dynamic conditions.

</td></tr></tbody>
</table>4.  From the form context menu, select **Save**.

5.  Select the **Contents** tab and then select **New Provider Content**.

6.  Select **Next Experience** as the content provider.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|An internal name for the notification content.|
    |Notification|The notification trigger that sends the notification content.|
    |Active|Option for whether the notification is sent when triggered.|
    |Table|Table to receive notifications about.|
    |Route|Next Experience Route|
    |Message Heading|Header text at the top of the message. From the Select variables list, you can select variables to include your message heading.|
    |Message|Secondary text of the message that follows the heading. From the Select variables list, you can select variables to include your message body.|

    The following example shows the values for a notification with custom content that references the number and short description of an incident.

    |Field|Value|
    |-----|-----|
    |Name|Incident record update content|
    |Notification|Incident records|
    |Active|true|
    |Message Heading|$\{number\} changed|
    |Message|Short description: $\{short\_description\}|

8.  Select **Submit**.


## Result

When triggered, users configured to receive the notifications see notifications with custom content as banners and in the Notifications menu in the Next Experience Unified Navigation.

The UI Notification Inbox \[ui\_notification\_inbox\] table lists all sent notifications and their recipients.

If users receive duplicate notifications, verify that the notification trigger has only one content provider. If the notification has both a Next Experience and Workspace content provider, remove the Workspace content provider from the notification trigger to send only the Next Experience notification with custom content.

**Parent Topic:**[Configuring the Next Experience UI](../concept/next-experience-ui-admin.md)

