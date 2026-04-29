---
title: Set up Microsoft Teams as a contact method for an on-call escalation
description: Enable users to receive Microsoft Teams notifications for an on-call escalation.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring On-Call Scheduling, On-Call Scheduling, IT Service Management]
---

# Set up Microsoft Teams as a contact method for an on-call escalation

Enable users to receive Microsoft Teams notifications for an on-call escalation.

## Before you begin

User should have Microsoft Teams user credentials.

Role required: admin

## Procedure

1.  Ensure that your ServiceNow instance is configured for Conversational Integration with Microsoft Teams and the IT Service Management integration with Microsoft 365 plugin \(sn\_now\_teams\_it\) is active.

    For information on Virtual Agent permission policies, see [Manage Now Virtual Agent permission policies](https://www.servicenow.com/docs/access?context=disable-now-virtual-agent-ms-teams&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

2.  Select **Microsoft Teams** as your preferred notification channel while defining the escalation settings for a user group.

    For information on escalation settings, see [Escalation and reminder settings for rosters](../reference/escalation-remind-settings-oncall.md).

3.  For the required user group, create a trigger rule that uses the On-Call: Assign by Acknowledgement trigger workflow.

    If a user or shift manager sets the preferred contact channel as Microsoft Teams, a notification is sent to the user in Microsoft Teams along with the actions that a user can perform.

    For information on creating a trigger rule, see [Create an escalation trigger rule](create-trigger-rule-oncall.md).


**Parent Topic:**[Configuring On-Call Scheduling](../../user-administration/concept/configuration.md)

