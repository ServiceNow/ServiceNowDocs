---
title: Create a chat channel template for Slack
description: Configure Chat Teams and Channel Templates to create chat teams and channels to collaborate, track the chat conversations, and add users and user groups to those Chat Channels. These Channel templates are created in Slack when a major security incident is promoted.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Slack chat connector for major security incidents, Configuring Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a chat channel template for Slack

Configure Chat Teams and Channel Templates to create chat teams and channels to collaborate, track the chat conversations, and add users and user groups to those Chat Channels. These Channel templates are created in Slack when a major security incident is promoted.

## Before you begin

Role required: sn\_msi.workspace\_admin

## About this task

The new channel that you create will be your channel name in Slack as well. You can search for the same channel and add your conversations.

## Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **Chat Channel** &gt; **Channel Templates**.

2.  Select **Slack channel configuration** to view the Slack configuration details.

3.  Select the **Active** check box to activate the Slack Chat Channel configuration.

4.  In the Team Name field, provide the MSI number and code name.

    By default, all Slack channels will be prefixed with the incident number. For example, `MSI000000 - {channel name}`. You can change the prefix to any field of your choice in this format: `{field_name}`.

    **Note:** The team name provided here will be used across all Major Security Incident records. To verify that the actual Slack is displayed in Slack application and has a unique name value for different Major Security Incidents, it’s recommended that you use an incident field value, which is unique such as the `MSI000000 - {channel name}`.

5.  Right-click the configuration, and select **Save**.

6.  Navigate to the Chat Channel Configuration section.

7.  Select **New** to create a new Chat Channel Configuration.

8.  On the form, fill the fields.

<table id="choicetable_t4z_2qt_gbc"><thead><tr><th align="left" id="d195876e166">

Field

</th><th align="left" id="d195876e169">

Description

</th></tr></thead><tbody><tr><td id="d195876e175">

**__Chat Team Configuration__**

</td><td>

Name of the Chat Team configuration. For example, Slack channel configuration.

</td></tr><tr><td id="d195876e185">

**__Channel Name__**

</td><td>

Name of the channel. For example, legal.**Note:**

-   Channel names can only contain lowercase letters, numbers, hyphens, and underscores and must be 50 characters or less. If your channel name contains special characters, they’re removed automatically. If your channel name contains spaces, they are replaced automatically with hyphens \(-\).
-   The new channel that you create here will be your channel name in Slack as well. You can search for the same channel and add your conversations.


</td></tr><tr><td id="d195876e209">

**__Channel Description__**

</td><td>

Unique description for the channel.

</td></tr><tr><td id="d195876e219">

**__Channel Users__**

</td><td>

Select the **Unlock Channel Users** icon, and add the users who can access this channel from the lookup list. Select the **Lock Channel Users** icon to lock the selected list of channel users.

</td></tr><tr><td id="d195876e238">

**__Channel User Groups__**

</td><td>

Select the **Unlock Channel User Groups** icon, and add the user groups who can access this channel from the lookup list. You can also use the **Add me** icon to add yourself.Select the **Lock Channel User Groups** icon to lock the selected list of channel user groups.

</td></tr></tbody>
</table>    ![Slack Chat Channel Configuration](../image/msim-chat-channel-config-slack.png "Slack Chat Channel Configuration")

9.  Select **Submit**.


## Result

The chat channel is now created and the users are assigned to those chat channel groups. You can view the collaboration chat activities both in Slack and in the Collaboration activity stream of the MSIM Workspace with the organized chat channel hierarchy structure as configured in the Chat Channel provider configuration.

**Parent Topic:**[Configure Slack chat connector for major security incidents](../concept/configure-slack-chat-connector-msi.md)

