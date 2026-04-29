---
title: Create or configure a service channel
description: Create or configure a service channel that is used in Advanced Work Assignment \(AWA\).
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create or configure a service channel

Create or configure a service channel that is used in Advanced Work Assignment \(AWA\).

## Before you begin

Role required: awa\_admin or admin

## About this task

You can specify additional conditions to filter the work items that are handled in the channel, change the agent capacity \(workload\) for the channel, set the inbox layouts that your agents use in Workspace, and view associated work item queues.

If you activate the corresponding plugins or install the corresponding store applications, AWA provides base system channels for these services:

-   Cases plugin \(com.snc\_csm.awa\)
-   Chats plugin \(com.glide.interaction.awa\)
-   Chats - Asynchronous plugin \(com.glide.interaction.awa\)
-   Conversational Integration with Facebook Messenger application \(sn\_va\_fb\_messenger\)
-   Incidents plugin \(com.snc.incident.awa\)
-   Conversational Integration with LINE application \(sn\_va\_line\)
-   Walk-up interactions plugin \(com.snc.walkup\)
-   Conversational Integration with WhatsApp \(powered by Twilio\) application \(sn\_va\_whatsapp\_twi\)

For each channel, you can change certain default settings, such as the default capacity \(workload\) for agents. You can also use the related lists to review associated queues, define the associated inbox layouts \(work item cards\) that are displayed in Workspace, and override the agent capacity value.

You can also create a service channel record from the Service Channel module, but you must [create a queue](awa-create-queue.md), [assignment rule](awa-create-assignment-rule.md), and [eligible assignment pool](awa-specify-assignment-eligibility.md) to route work through the service channel. For more information, see [Set up a custom service channel](setup-custom-channel.md).

## Procedure

1.  Navigate to the service channel settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up service channels**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Service Channels**.
2.  Choose a situation.

    -   To create a service channel, select **New**.
    -   To update a service channel, select the service channel record that you want to update.
3.  On the form, fill in the fields.

<table id="table_m12_pyk_t2b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the selected base system service channel to be configured:-   Chat
-   Chat - Asynchronous
-   Case
-   Facebook Messenger
-   Incident
-   Line
-   Walk-up
-   WhatsApp


</td></tr><tr><td>

Inbox order

</td><td>

Order in which channel items appear in the agent inbox.

</td></tr><tr><td>

Application

</td><td>

Name of the application.-   Chat: Global
-   Chat - Asynchronous: Global
-   Case: Advanced Work Assignment for CSM
-   Facebook Messenger: Conversational Integration with Facebook Messenger
-   Incident: Advanced Work Assignment for Incidents
-   Line: Conversational Integration with LINE
-   Walk-up: Walk-up Experience
-   WhatsApp: Conversational Integration with WhatsApp \(powered by Twilio\)


</td></tr><tr><td>

Active

</td><td>

Option for activating the service channel. When you select this option, the associated queues for the service channel can start accepting work items.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the service channel:-   Chat: Live Agent Chat Interactions
-   Chat - Asynchronous: Asynchronous Live Agent Chat Interactions
-   Case: Cases for Agents
-   Facebook Messenger: Live Agent Facebook Messenger Interactions
-   Incident: Incidents for Agents
-   Line: Live Agent LINE Interactions
-   Walk-up: Walk-up interactions for agents to work on
-   WhatsApp: Live Agent WhatsApp Interactions


</td></tr><tr><td>

Table

</td><td>

Table that stores the service channel records.

</td></tr><tr><td>

Advanced condition

</td><td>

If enabled, the advanced conditions that apply to the channel. For example:-   Chat: **\[Type\] \[is\] \[Chat\]**
-   Chat - Asynchronous: **\[Subtype\] \[is\] \[mweb\]**, **\[Type\] \[is\] \[Messaging\]**
-   Facebook Messenger: **\[Subtype\] \[is\] \[Facebook Messenger\]**
-   Line: **\[Subtype\] \[is\] \[Line\]**
-   Walk-up: **\[Type\] \[is\] \[Walk-up\]**
-   WhatsApp: **\[Subtype\] \[is\] \[WhatsApp\]**


</td></tr><tr><td>

Assign to field

</td><td>

Field that references the user assigned to the item. In both Case and Interaction \(and most other tables\), this field is the **Assigned to** \(assigned\_to\) field.

</td></tr><tr><td>

Assignment group field

</td><td>

Field that references the assignment group assigned to the item. In most tables, this field is the **Assignment group** field.

</td></tr><tr><td>

Type

</td><td>

Indicator of whether a communication service channel is handled as a synchronous or asynchronous conversation channel. This field appears when you select **Interaction** in the **Table** field.-   Chat
-   Phone
-   Messaging
-   Other


</td></tr><tr><td>

Log level

</td><td>

Amount of information recorded when AWA events are logged.

-   None: No information is logged.
-   Basic: Only basic information is logged.
-   Verbose: Detailed information, including record details and event details, is logged.
 This field appears if **Enable logging** is enabled.

</td></tr><tr><td>

Inbox Alert Audio

</td><td>

Audible alert that sounds when a new item arrives in your inbox for this service channel. If you don’t specify an audio file, the default audio file sounds.

</td></tr><tr><td>

Message Alert Audio

</td><td>

Audible alert that sounds when a new message arrives in your conversation for this service channel. If you don’t specify an audio file, the default audio file sounds.

</td></tr><tr><td class="sub-head" colspan="2">

Capacity and Utilization

</td></tr><tr><td>

Default work item size

</td><td>

Amount of an agent's capacity that is used when this work item is assigned. The default is 1.

</td></tr><tr><td>

Default capacity

</td><td>

Number of items automatically assigned to agents \(pending overrides\). -   Case: The default is 2.
-   Chat: The default is 4.
-   Chat: Asynchronous: The default is 4.
-   Facebook Messenger: The default is 4.
-   Incident: The default is 2.
-   Line: The default is 4.
-   Walk-up: The default is 1.
-   WhatsApp: The default is 4.


</td></tr><tr><td>

Utilization condition

</td><td>

Condition that determines what constitutes an active item that counts toward agent workload/capacity. For example, the record state is New, Open, or Awaiting Info.-   For chat: The state is not Closed Complete or Closed Abandoned
-   For Chat - Asynchronous: The state is Closed Complete or Closed Abandoned
-   For case: The state is New or Open
-   For Facebook Messenger: The state is New or Work in Progress
-   For incident: The state is New, In Progress, or On Hold
-   For Line: The state is New or Work in Progress
-   For walk-up: The state is not On Hold, Closed Complete, or Closed Abandoned
-   For WhatsApp: The state is New or Work in Progress


</td></tr><tr><td class="sub-head" colspan="2">

Logging

</td></tr><tr><td>

Enable logging

</td><td>

Option to record information in the syslog\_awa table when AWA events are logged. Specify the level of detail to be recorded in the **Log level** field on this screen.

</td></tr><tr><td>

Stop logging at

</td><td>

Date and time that logging should stop.This field appears if **Enable logging** is enabled.

</td></tr></tbody>
</table>4.  Select **Submit** or **Update**.

    The channel is added to or updated in the Service Channels \[awa\_service\_channel\] table.


## What to do next

-   [Override the agent capacity](awa-change-agent-capacity.md) for selected agents or groups.
-   [Create or modify an inbox layout](awa-modify-inbox-layout.md) for the service channel.
-   [Configure agent assignment rules](awa-create-assignment-rule.md) for the channel.
-   [Define agent pools eligible for assignment](awa-specify-assignment-eligibility.md).
-   [Create or modify a work item queue](awa-create-queue.md) for the channel.
-   [Create or modify a work item size override](awa-modify-work-item-size.md) for the channel.

