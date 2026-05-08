---
title: Set up mobile push as a contact method for an on-call escalation
description: Enable users to receive mobile push notifications for on-call escalations.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring On-Call Scheduling, On-Call Scheduling, IT Service Management]
---

# Set up mobile push as a contact method for an on-call escalation

Enable users to receive mobile push notifications for on-call escalations.

## Before you begin

Role required: admin

## Procedure

1.  Install ServiceNow Agent and enable mobile push notifications from the **Notifications** tab.

    For information on this tab, see Base system functionality for ServiceNow mobile.

    The mobile push appears as a communication channel in the ServiceNow instance.

2.  Select **Mobile push** as your preferred notification channel while defining the escalation settings for a user group.

    For information on escalation settings, see [Escalation and reminder settings for rosters](../reference/escalation-remind-settings-oncall.md).

3.  For the required user group, create a trigger rule that uses the On-Call: Assign by Acknowledgement trigger workflow.

    If a user or shift manager sets the preferred contact channel as mobile push, a mobile push notification is sent to the user along with the actions that a user can perform.

    For information on creating a trigger rule, see [Create an escalation trigger rule](create-trigger-rule-oncall.md).


**Parent Topic:**[Configuring On-Call Scheduling](../../user-administration/concept/configuration.md)

