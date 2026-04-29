---
title: Unlink your ServiceNow user account from a messaging application for Virtual Agent conversations
description: If needed, you can unlink your ServiceNow user account from a messaging app used for the Now Virtual Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Account linking in pre-built messaging integrations, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Unlink your ServiceNow user account from a messaging application for Virtual Agent conversations

If needed, you can unlink your ServiceNow user account from a messaging app used for the Now Virtual Agent.

## Before you begin

Role required: user

## About this task

Unlinking your account from a selected Conversational Integration for Slack, Microsoft Teams or Workplace, deactivates the association between your ServiceNow account and the messaging app. After you unlink your account, you can no longer engage in Virtual Agent conversations that query or change records in the ServiceNow database.

## Procedure

1.  From within the messaging app, type `logout`.

2.  From the application navigator, navigate to **Self-Service** &gt; **My Profile**.

3.  Click the **View Linked Accounts** related link.

4.  In the Linked Accounts page, select the check box for the messaging integration to be unlinked.

5.  Select **Actions on selected rows**, then click **Unlink account**.

    The link between your ServiceNow account and the Virtual Agent messaging integration becomes inactive.

    **Note:** Even though you unlinked your account, you can still run public Virtual Agent conversations.

6.  To link your account again, repeat steps 1 through 3 for the associated messaging integration and in the **Actions on selected rows...**, click **Link account**.


**Parent Topic:**[Account linking in pre-built messaging integrations](../concept/va-adapter-autolinking.md)

