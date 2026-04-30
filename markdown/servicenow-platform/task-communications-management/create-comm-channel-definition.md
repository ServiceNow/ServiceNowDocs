---
title: Define a communication channel
description: Define a communication channel for each communication task to determine which mode of communication to use for the task when a plan is attached to a table.
locale: en-US
release: yokohama
product: Task Communications Management
classification: task-communications-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Define a communication plan, Working with Task Communications Management, Task Communications Management, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a communication channel

Define a communication channel for each communication task to determine which mode of communication to use for the task when a plan is attached to a table.

## Before you begin

Role required: sn\_comm\_management.comm\_plan\_admin or admin

You have defined a communication plan and its related tasks.

## About this task

-   The modes of communication available are: email, SMS, conference, and Slack.
-   For the incident table, the functionality for SMS and conference appears only if you activate the Notify plugin \(com.snc.notify\) and the **com.snc.iam.notify\_number** property value is set to the registered notify number. The notify number is registered while configuring the Twilio account.
-   For the incident table, the functionality for Slack appears only if you activate the Collaboration Services for Task Communications Management plugin \(sn\_tcm\_collab\_hook\). To activate the Collaboration Services for Task Communications Management plugin, navigate to [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) and install the Collaboration Services for Task Communications Management application. For more information, refer [Collaboration services for Task Communications Management](https://www.servicenow.com/docs/access?context=collab-services-tcm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

    **Note:** For information on how to configure Slack, refer to [Configure Slack workspace](https://www.servicenow.com/docs/access?context=set-up-slack&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) .

-   **Add Channel – Conference** is mutually exclusive to **Add Channel – SMS** and **Add Channel – Email**. If you select **Add Channel – Conference**, you cannot select **Add Channel – Email** or **Add Channel – SMS**.

## Procedure

1.  Navigate to **All** &gt; **Task Communications Management** &gt; **Plan Definitions**.

2.  Click a communication plan.

3.  Click the Communication Task Definitions related list and then click the task for which you want to define the communication channel.

4.  On the Communication Task Definition form, click any one of the following related links based on your requirement:

    -   **Add channel - DEX Desktop Assistant**
    -   **Add Channel – Conference**
    -   **Add Channel – Email**
    -   **Add Channel – SMS**
    -   **Add Channel – Slack**
5.  On the form, fill in the fields.

<table id="table_ish_5tl_2db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Add Channel – Conference

</td></tr><tr><td>

Communication task definition

</td><td>

Communication task definition that the channel definition is associated with.

</td></tr><tr><td>

Notify provider selector

</td><td>

Lookup icon \(![Lookup icon](../../proactive-triggers/image/look-up-icon.png)\) to select the selector from the Provider Selector \[notify\_group\_selector\] table.**Note:** The selector can be associated with notify number group or conference provider. Each notify number group can have one or more Notify numbers that can be used to make conference calls.

</td></tr><tr><td class="sub-head" colspan="2">

Add Channel – Email

</td></tr><tr><td>

Communication task definition

</td><td>

Communication task definition that this channel definition is associated with.

</td></tr><tr><td>

Email client template

</td><td>

Lookup icon \(![Lookup icon](../../proactive-triggers/image/look-up-icon.png)\) to select the email client template used to send emails to the targeted audience. **Note:** This email template must be defined in the Communication task table.

</td></tr><tr><td>

Recipient field

</td><td>

List to select where you want the recipients list to be populated. Options include **To**, **CC**, and **BCC**. The default value is populated based on what you define in the **Default recipient location of emails for Communication Tasks** property \(**sn\_comm\_management.default\_email\_recipient\_field**\).

</td></tr><tr><td class="sub-head" colspan="2">

Add Channel – SMS

</td></tr><tr><td>

Communication task definition

</td><td>

Communication task definition this channel definition is associated with.

</td></tr><tr><td>

Notify SMS template

</td><td>

Lookup icon ![Lookup icon](../../proactive-triggers/image/look-up-icon.png) to select the notify SMS template used to send an SMS to the targeted audience.**Note:** This SMS template must be defined in the Communication task table.

</td></tr><tr><td>

Notify provider selector

</td><td>

Lookup icon \(![Lookup icon](../../proactive-triggers/image/look-up-icon.png)\) to select the selector from the Provider Selector \[notify\_group\_selector\] table.**Note:** The selector can be associated with notify number group or conference provider. Each notify number group can have one or more Notify numbers that can be used to send SMS.

</td></tr><tr><td class="sub-head" colspan="2">

Add Channel – Slack

</td></tr><tr><td>

Communication task definition

</td><td>

Communication task definition this channel definition is associated with.

</td></tr><tr><td>

Channel Type

</td><td>

Channel type is Slack.

</td></tr><tr><td class="sub-head" colspan="2">

Add Channel – Desktop Assistant

</td></tr><tr><td>

Communication task definition

</td><td>

Communication task definition this channel definition is associated with.

</td></tr><tr><td>

Channel Type

</td><td>

Channel type is Desktop Assistant.

</td></tr><tr><td>

Notification template

</td><td>

Template applied when composing the notification message.

</td></tr></tbody>
</table>6.  Click **Submit**.

    A communication channel is defined for the communication task.


## What to do next

After creating communication tasks and communication channels for those tasks, define contacts for the communication plan.

**Parent Topic:**[Define a communication plan](create-comm-plan-definition.md)

**Related topics**  


[Define a communication task](create-comm-task-definition.md)

[Define a communication contact](create-comm-contact-definition.md)

