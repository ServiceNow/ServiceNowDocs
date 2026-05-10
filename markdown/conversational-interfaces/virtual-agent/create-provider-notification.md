---
title: Create a provider notification
description: Execute the following steps to create a provider notification for Virtual Agent and Workspace providers.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Using, Conversational Integration with WhatsApp \(powered by Twilio\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a provider notification

Execute the following steps to create a provider notification for Virtual Agent and Workspace providers.

## Before you begin

Role required: admin

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

Application

</td><td>

Application scope of the notification.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification. The notification is active by default.

</td></tr><tr><td class="sub-head" colspan="2">

Trigger

</td></tr><tr><td>

Triggered By

</td><td>

System action that triggers the notification. You can send the notification after a record is changed or after an event is triggered.

</td></tr><tr><td>

Table

</td><td>

Table to receive notifications about.

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

 **Note:** You can select only an event that shares the same table as the notification.

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

Users who receive the notification.**Note:** Notifications in messaging channels are sent only to users with ServiceNow accounts \(sys\_user profiles\). Consumers and customer contacts are considered as guests and cannot receive notifications in messaging channels.

</td></tr><tr><td>

Recipients in fields

</td><td>

Record fields that include users who receive the notification. For example, to send the notification to the record assignee, select **Assigned to**.**Note:** This field shows up only if you select a table.

</td></tr><tr><td>

Is originating user included?

</td><td>

Option to include the user who changed the record or triggered the event.

</td></tr><tr><td>

Event Parm1 contains recipient\(s\)?

</td><td>

Option to select if Parm 1 contains a list of comma separated sys\_ids

</td></tr><tr><td>

Event Parm2 contains recipient\(s\)?

</td><td>

Option to select if Parm 2 contains a list of comma separated sys\_ids

</td></tr><tr><td>

Resolve Parm1 recipients from table

</td><td>

Table that is used to resolve the sys\_id of the recipient**Note:** This field appears only when you select Event parm 1.

</td></tr><tr><td>

Resolve Parm2 recipients from table

</td><td>

Table that is used to resolve the sys\_id of the recipient**Note:** This field appears only when you select Event parm 2.

</td></tr><tr><td>

Advanced event condition

</td><td>

Option to select when the recipients are from more than 2 tables. These are dynamic conditions.

</td></tr></tbody>
</table>3.  Select **Submit**.

    **Note:** Use the **Submit** button for Virtual Agent notifications. The **Submit and Add Common Content** button is for other use cases.

    All the validation messages given by different providers are retained. Warning messages of one provider is not overridden by warning messages of another provider.


**Parent Topic:**[Using Conversational Integration with WhatsApp \(powered by Twilio\)](../../virtual-agent/concept/messg-whatsapp-using.md)

