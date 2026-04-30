---
title: Link your ServiceNow user account to a messaging application for Virtual Agent conversations
description: Link your ServiceNow account to a third-party messaging application to access non-public Virtual Agent topics that use ServiceNow records.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Account linking in pre-built messaging integrations, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Link your ServiceNow user account to a messaging application for Virtual Agent conversations

Link your ServiceNow account to a third-party messaging application to access non-public Virtual Agent topics that use ServiceNow records.

## Before you begin

Role required: user

## About this task

When you initially engage with the Virtual Agent bot, your messaging account is automatically linked to your ServiceNow account as long as the same email account is defined for both your messaging and ServiceNow accounts. However, if you unlinked your messaging account from your ServiceNow account \(using the **logout** command\), each time that you start a subsequent Virtual Agent session, the bot gives you the option to link to your ServiceNow account or continue as guest. The authentication step \(linking\) occurs in your instance or in a specific Service Portal, if set by your admin.

## Procedure

1.  Open the messaging application.

2.  Find your Virtual Agent bot.

3.  Start a conversation with your Virtual Agent bot.

    The bot then presents a prompt that provides options to authenticate \(**Link to ServiceNow**\), **Continue as Guest**, or use the **Check out Tips**.

4.  Select **Link to ServiceNow** to authenticate.

    ![Link your ServiceNow profile.](../../virtual-agent/images/msteams-custom-bot-response.png)

    Authentication directs you to your instance or a specific Service Portal set by your admin. If you're not already logged in to your instance or a Service Portal, you are prompted to enter your login credentials.

    **Note:** If a user is unlinked or continued as a guest, notifications will be disabled. Also, only the public topics are discoverable.

    ![Check out tips provides you with the commands to get started with the Virtual Agent.](../../virtual-agent/images/checkout-tips.png "Check out Tips")

5.  In the confirmation that appears prompting you to Confirm or Deny linkage between your accounts, select Confirm to allow the account link.

6.  After confirmation, you are directed to your instance user record.

    A confirmation message is displayed at the top of the screen.


**Related topics**  


[Redirect user authentication to a Service Portal](../../virtual-agent/task/set-user-linkage.md)

