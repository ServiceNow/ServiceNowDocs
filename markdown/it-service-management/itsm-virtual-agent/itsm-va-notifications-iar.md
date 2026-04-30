---
title: Actionable notifications for Issue Auto Resolution in ITSM Virtual Agent
description: Notify employees when Virtual Agent finds a topic that matches the end user's intent.
locale: en-US
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Pre-built actionable notifications, ITSM Virtual Agent, IT Service Management]
---

# Actionable notifications for Issue Auto Resolution in ITSM Virtual Agent

Notify employees when Virtual Agent finds a topic that matches the end user's intent.

Issue Auto Resolution sends actionable notifications through Virtual Agent directly to the end user on their preferred chat channel when the machine-learning model finds a topic that matches the end user's intent. Issue Auto Resolution must be enabled, and the end user must be subscribed to notifications.

Actionable notifications contain buttons that the end user can select. Each button is mapped to a topic that is enabled for Issue Auto Resolution. Based on the end user's selections, different aspects of Issue Auto Resolution execute, according to the logic of the matched topic.

For more information about Issue Auto Resolution, see [Using Issue Auto Resolution](https://www.servicenow.com/docs/access?context=auto-resolution-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) and [Issue Auto Resolution for ITSM Virtual Agent](../concept/itsm-va-auto-resolution.md).

**Note:** You must activate notifications in Workflow Studio in order to use them. For details, see [Set up actionable notifications for ITSM Virtual Agent](../task/setup-actionable-notifications.md).

## Issue Auto Resolution

End users receive this notification when an incident is created and the incident short description relates to an existing Issue Auto Resolution topic intent. The end user can choose to accept the Virtual Agent assistance, wait for a human agent, or skip the notification.

![Actionable notification for Issue Auto Resolution printer issues.](../image/IARprinter1.png)

If the end user accepts the Virtual Agent assistance, the matched Issue Auto Resolution topic runs and Virtual Agent provides suggestions to resolve the issue.

After Virtual Agent provides suggestions to resolve the issue, the end user can indicate if these suggestions were successful and can choose to close the ticket or to leave it open. If the end user chooses to leave the ticket open, Virtual Agent assigns the ticket to a live agent.

## Issue Auto Resolution Reminder

End users receive this notification to remind them that virtual assistance has been found to help them. The end user can choose to accept the Virtual Agent assistance, wait for a human agent, or skip the notification.

**Parent Topic:**[ITSM Virtual Agent pre-built actionable notifications](../concept/itsm-actionable-notifications.md)

