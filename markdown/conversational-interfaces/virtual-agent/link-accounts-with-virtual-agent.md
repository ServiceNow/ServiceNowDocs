---
title: Link your ServiceNow user account to a messaging application for Virtual Agent conversations
description: Link your ServiceNow account to a third-party messaging application to access non-public Virtual Agent topics that use ServiceNow records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/link-accounts-with-virtual-agent.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Account linking in pre-built messaging integrations, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Link your ServiceNow user account to a messaging application for Virtual Agent conversations

Link your ServiceNow account to a third-party messaging application to access non-public Virtual Agent topics that use ServiceNow records.

## Before you begin

Role required: user

## About this task

If the same email account is defined for both your messaging and ServiceNow accounts, then when you first use the Virtual Agent, your messaging account is automatically linked to your ServiceNow account.

However, after you unlink your messaging account from your ServiceNow account \(using the **logout** command\), then each time you start a new Virtual Agent session, the bot gives you the option to link to your ServiceNow account or continue as a guest. The authentication step \(linking\) occurs in your instance or in a specific Service Portal, as set by your admin.

## Procedure

1.  Open the messaging application.

2.  Find your Virtual Agent bot.

3.  Start a conversation with your Virtual Agent bot.

    The bot then presents a prompt that provides options to authenticate \(**Link to ServiceNow**\), **Continue as Guest**, or use the **Check out Tips**.

4.  Select **Link to ServiceNow** to authenticate.

    \[Omitted image "msteams-custom-bot-response.png"\] Alt text: Link your ServiceNow profile.

    Authentication directs you to your instance or a specific Service Portal set by your admin. If you're not already logged in to your instance or a Service Portal, you’re prompted to enter your login credentials.

    **Note:** If a user is unlinked or continued as a guest, notifications are disabled. Also, only the public topics are discoverable.

    \[Omitted image "checkout-tips.png"\] Alt text: Check out tips providing you with the commands to get started with the Virtual Agent.

5.  In the confirmation that appears prompting you to Confirm or Deny linkage between your accounts, select Confirm to enable the account link.

6.  After confirmation, you’re directed to your instance user record.

    A confirmation message is displayed at the top of the screen.


**Parent Topic:**[Account linking in pre-built messaging integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-adapter-autolinking.md)

**Related topics**  


[Redirect user authentication to a Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/set-user-linkage.md)

