---
title: View or join slack channel from an incident
description: View all slack channels associated with an incident to know if a required slack channel already exists before you create a new one. You can also import messages from a slack channel.
locale: en-US
release: zurich
product: Collaboration Services
classification: collaboration-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Collaboration services, IT Service Management]
---

# View or join slack channel from an incident

View all slack channels associated with an incident to know if a required slack channel already exists before you create a new one. You can also import messages from a slack channel.

## Before you begin

-   Role required: sn\_incident\_write, itil, or admin
-   Plugins required:
    -   Collaboration Services plugin \(sn\_tcm\_collab\_hook\) version 2.0.x
    -   Slack Spoke for ServiceNow Integration Hub plugin \(com.sn.slack.ahv2\) version 1.3.x

## About this task

The system property **sn\_tcm\_collab\_hook.slack\_on\_task** enables the slack feature on a task table. By default, the value is incident. If you want to enable the slack feature on other task tables, such as problem or change\_request, add the table names in the **Value** field.

**Note:** When an incident becomes inactive, the associated slack channels get archived.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

2.  Open an active incident record.

3.  Click the **View Slack Channels** related link.

    All the dedicated slack channels for the incident are displayed.

    **Note:** The **Join channel** option appears only for public channels.

4.  Click **View channel** to open the slack channel.

5.  Click **Join channel** to join any slack channel.

6.  To import messages from any slack channel, click **Import messages**.


-   **[Add form section to view slack channels](add-slack-channels-section.md)**  
View unarchived slack channels associated with an incident in the form section. The form section saves you the effort of opening the available channel list manually from the related list.

**Parent Topic:**[Configuring Collaboration services](../concept/configuring-collab-services.md)

