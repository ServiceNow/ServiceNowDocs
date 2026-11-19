---
title: Create a provider notification
description: Execute the following steps to create a provider notification for Virtual Agent and Workspace providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/virtual-agent/direct-whatsapp-create-a-provider-notification.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Using, Conversational Integration with WhatsApp \(WhatsApp Cloud API\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a provider notification

Execute the following steps to create a provider notification for Virtual Agent and Workspace providers.

## Before you begin

Enable the notifications for the WhatsApp channel. For more information, see [Enable WhatsApp channel notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/enable-direct-whatsapp-channel-notifications.md).

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

Category

</td><td>

Select the category to which this notification belongs. A category identifies and groups related notifications. This notification, if active and listed in the selected Category in the notification preferences for each user \(Notifications tab in the System Settings window\).

</td></tr><tr><td>

Importance

</td><td>

Importance level of the notification.

</td></tr><tr><td>

Application

</td><td>

Application scope of the notification.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification. The notification is active by default.

</td></tr><tr><td>

Urgency

</td><td>

Urgency level of the notification.

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

 **Note:** You can select only an event that shares the table as the notification.

 This field appears when you select **Event** in the **Trigger** field.

</td></tr><tr><td>

Table

</td><td>

Table to receive notifications about.

</td></tr><tr><td>

Conditions

</td><td>

Filter to specify the table records that users receive notifications about. For example, to send notifications about top-priority incidents, you would select **Incident \[incident\]** in the **Table** field and set the conditions to **\[Priority\] \[is\] \[1 - Critical\]**.

</td></tr><tr><td>

Advanced condition

</td><td>

Script that determines whether to send the notification. Set the global *answer* variable to true to send it. The script can use the *current* \(record\) and *event* variables.

</td></tr><tr><td class="sub-head" colspan="2">

Who will receive

</td></tr><tr><td>

Users

</td><td>

Users who receive the notification.**Note:** Notifications in messaging channels are sent only to users with ServiceNow accounts \(sys\_user profiles\). Consumers and customer contacts are considered as guests and can’t receive notifications in messaging channels.

</td></tr><tr><td>

Subscribable

</td><td>

Option to let users subscribe to this notification from their notification preferences.

</td></tr><tr><td>

Recipients in fields

</td><td>

Record fields that include users who receive the notification. For example, to send the notification to the record assignee, select **Assigned to**.**Note:** This field shows up only if you select a table.

</td></tr><tr><td>

Include the person whose action triggered the notification

</td><td>

Option to include the user who changed the record or triggered the event.

</td></tr><tr><td>

Recipient\(s\) listed in event parm1

</td><td>

Option to select if Parm 1 contains a list of comma separated sys\_ids

</td></tr><tr><td>

Recipient\(s\) listed in event parm2

</td><td>

Option to select if Parm 2 contains a list of comma separated sys\_ids

</td></tr><tr><td>

Table containing recipients from event parm1

</td><td>

Table that is used to resolve the sys\_id of the recipient**Note:** This field appears only when you select **Recipient\(s\) listed in event parm1**.

</td></tr><tr><td>

Table containing recipients from event parm2

</td><td>

Table that is used to resolve the sys\_id of the recipient**Note:** This field appears only when you select **Recipient\(s\) listed in event parm2**.

</td></tr><tr><td>

Advanced event condition

</td><td>

Option to select when the recipients are from more than 2 tables. These are dynamic conditions.

</td></tr><tr><td>

Script

</td><td>

Script that defines the recipients of the notification. The script has access to the *parm1* and *parm2* values of the event.**Note:** This field appears only when you select **Advanced event condition**.

</td></tr></tbody>
</table>3.  Select **Submit**.

    **Note:** Use the **Submit** button for Virtual Agent notifications. The **Submit and Add Common Content** button is for other use cases.

    All the validation messages given by different providers are retained. Warning messages of one provider isn’t overridden by warning messages of another provider.


**Parent Topic:**[Using Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/messg-direct-whatsapp-using.md)

**Related topics**  


[Provider notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/provider-notifications-landing.md)

[Create default content in a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-default-content.md)

