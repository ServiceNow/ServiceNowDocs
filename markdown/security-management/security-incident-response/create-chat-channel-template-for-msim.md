---
title: Create a chat channel template
description: Configure Chat Teams and Channel Templates to create chat teams and channels to collaborate, track the chat conversations, and add users and user groups to those Chat Channels. These Channel templates are created in the Microsoft Teams when a major security incident is promoted.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Teams, Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a chat channel template

Configure Chat Teams and Channel Templates to create chat teams and channels to collaborate, track the chat conversations, and add users and user groups to those Chat Channels. These Channel templates are created in the Microsoft Teams when a major security incident is promoted.

## Before you begin

Role required: sn\_msi.workspace\_admin

## Procedure

1.  Navigate to **Major Security Incident Management** &gt; **Chat Channel** &gt; **Channel Templates**.

2.  On the Chat Channel Configuration form, select **New** in the form header.

3.  On the form, fill in the fields.

<table id="table_v4k_lbn_drb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the folder.

</td></tr><tr><td>

Provider

</td><td>

Microsoft Teams.

</td></tr><tr><td>

Team Name

</td><td>

Name for the team, for example in the format, \{number\}-\{category\}.**Note:** The team name provided here will be used across all Major Security Incident records. To ensure that the actual Microsoft Team Name is displayed in MS Teams application and has a unique name value for different Major Security Incidents, it is recommended that you use an incident field value which is unique such as the incident number - \{number\}. As shown in the screen shot example, the \{number\} followed by a separator '-' and the \{category\} field variable would provide a unique number and description of the major security incident that Microsoft Teams is created for, for example \{number\} - \{category\}.

</td></tr><tr><td>

Team Description

</td><td>

Optional description of the team.

</td></tr><tr><td>

Table

</td><td>

Major Security Incident \(sn\_msi\_incident\).

</td></tr></tbody>
</table>    ![Chat Team Configuration](../../security-incident-response/image/channel-templates-config.png)

4.  Select **Submit**.

5.  Navigate to Chat Channel Configuration section.

6.  Select **New** to create a new Chat Channel Configuration.

7.  Enter the **Chat Team Configuration** and **Channel Name**.

    **Note:** The new channel that you had created here will be your channel name in Microsoft Teams as well. You can search for the same channel and add your conversations.

8.  Add the **Channel Users** and **Channel User Groups** from the lookup list.

9.  **Submit** the new chat channel configuration record.

    ![Chat Channel Configuration](../../security-incident-response/image/chat-channel-config-new-record.png)


## Result

The chat channel is now created and the users are assigned to those chat channel groups. You can view the collaboration chat activities both in Microsoft Teams and in the Collaboration activity stream of the MSIM Workspace with the organized chat channel hierarchy structure as configured in the Chat Channel provider configuration.

**Parent Topic:**[Configure Microsoft Teams](../../security-incident-response/concept/chat-channel-provider-config.md)

