---
title: Create slack channel for an incident
description: Create a private or a public slack channel to collaborate with support teams or send a communication to keep stakeholders informed.
locale: en-US
release: australia
product: Collaboration Services
classification: collaboration-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Slack integration - Incident Management, Collaboration services, IT Service Management]
---

# Create slack channel for an incident

Create a private or a public slack channel to collaborate with support teams or send a communication to keep stakeholders informed.

## Before you begin

-   Role required: sn\_incident\_write, itil, or admin
-   Plugins required:
    -   Collaboration Services plugin \(sn\_tcm\_collab\_hook\) version 2.0.x
    -   Slack Spoke for ServiceNow Integration Hub plugin \(com.sn.slack.ahv2\) version 1.3.x
-   Ensure you have set up interactivity and shortcuts for slack. For more information, refer [configure slack app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/set-up-slack.md).

## About this task

The system property **sn\_tcm\_collab\_hook.slack\_on\_task** enables the slack feature on a task table. By default, the value is incident. If you want to enable the slack feature on other task tables such as problem or change\_request, add the table names in the **Value** field.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

2.  Open an active incident record.

3.  Click the **Create Slack Channel** related link.

4.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Add participants|Individual users or groups whom you want as participants to the channel.|
    |Recommended and Selected|Columns to personalize your list. Select the items in the **Recommended** column and move them to the **Selected** column using the right-arrow icon \(![Right-arrow icon](../image/right-arrow-icon.png)\).|
    |Channel name|Unique name of the channel that differentiates it from the rest of the channels in Slack.|
    |Channel topic|Description about the purpose of the channel.|
    |Include a brief message for participants|Brief message that you want to send to the participants.|
    |Private channel|Option to indicate whether the slack channel is private or public. If you select the check box, the channel is created as a private channel else it is created as a public channel.|

5.  Click **Create channel**.

    A slack channel is created and an invitation is sent to the participants. Any duplicate user is removed from the selected participant list before the notification is sent. The participants can click **Skip** or **Join Channel** to ignore or join a slack channel.


