---
title: Add recipients to usage spike, execution failure, and latency error email notifications
description: Add or change recipients to email notifications triggered by unexpected or undesired behavior in AI agent and agentic workflow executions.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-10-27"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist AI agents, Enable AI experiences]
---

# Add recipients to usage spike, execution failure, and latency error email notifications

Add or change recipients to email notifications triggered by unexpected or undesired behavior in AI agent and agentic workflow executions.

## Before you begin

Set your application scope to Now Assist AI Agents.

Role required: admin

## About this task

There are different email notifications that can be configured: one for Assist usage spikes, one for failed AI agent executions, and two for latency errors. The properties for configuring the thresholds for sending these notifications can be found in the [Now Assist AI Agents Reference](../reference/na-aia-reference.md#agent-properties-table-properties).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  In the **Name** field, search for `AI Agent`, and select the notification you want to edit.

    There are different Notifications records for the different sources of alert. If you want to change the recipients for all types of alerts, you must edit each of the Notification records individually.

3.  Open the **Who will receive** tab.

4.  Select the unlock icon for the type of recipient you want to add or change.

    To quickly add yourself to the list of recipients, select the Add me icon next to the **Users** field.

5.  Select the users and groups you want to receive email alerts.

    If you select **Send to event creator**, the owner of the AI agent or agentic workflow that triggered the alert receives a notification.

    You can select **Exclude delegates** if you don't want delegated users to receive the notification. By default, delegates will receive notifications.

6.  Update or save the record.


## Result

The specified users or groups can now receive notifications for a specific triggered condition of AI agent or agentic workflow executions.

## What to do next

Repeat for any other AI agent alert notifications you want to configure.

