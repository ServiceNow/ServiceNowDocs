---
title: Include cases logged using specified communication channels in Auto-Responder notifications
description: Send Auto-Responder email notifications for customer service cases logged using a communication channel.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Auto-Responder notifications, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Include cases logged using specified communication channels in Auto-Responder notifications

Send Auto-Responder email notifications for customer service cases logged using a communication channel.

## Before you begin

Role required: admin

Perform the following tasks.

-   Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\). For more information, see Activate a plugin and [Predictive Intelligence for CSM solution definitions](../concept/predictive-intelligence-for-csm.md).
-   Set the application scope to Customer Service using the application picker. For more information, see Application picker.
-   Ensure that the required channel is already set up for use. For more information, see .

## About this task

By default, the Case auto-responder recommendations notification is configured to send Auto-Responder email notifications for customer service cases logged using emails. You can configure it to include other communication channels such as web, phone, chat, social, community, alert, and virtual agent.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Notifications**.

2.  Search for `Case auto-responder recommendations`.

3.  In the **Name** column, click the **Case auto-responder recommendations** link.

4.  In the **Conditions** field, click **Add Filter Condition** or **Add "Or" Clause** to set the filter condition for a communication channel.

    **Note:** The default filter condition is **\[Channel\] \[is\] \[Email\] AND \[Active\] \[is\] \[true\]**.

    For example, to send Auto-Responder notifications for customer service cases logged using a mobile phone in addition to email, you would click **Add Filter Condition** and create the condition **\[Channel\] \[is\] \[Phone\] AND \[Active\] \[is\] \[true\]**.


