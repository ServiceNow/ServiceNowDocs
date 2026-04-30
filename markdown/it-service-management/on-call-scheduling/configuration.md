---
title: Configuring On-Call Scheduling
description: Plan and configure On-Call Scheduling properties, templates, trigger rules, escalation policies, rosters, and schedules.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [On-Call Scheduling, IT Service Management]
---

# Configuring On-Call Scheduling

Plan and configure On-Call Scheduling properties, templates, trigger rules, escalation policies, rosters, and schedules.

As an administrator, you can configure preferences and application behavior and create tools that improve the effectiveness of roster members and shift managers. These are some of the tasks you can perform as an administrator.

## Activate On-Call Scheduling

You can activate the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin if you have the admin role.

## Set up contact methods

You can configure the following contact methods and enable users to receive notifications for escalations.

-   Slack: You can also configure a template and subflow for user responses to the notifications.
-   Text and voice messages: You can configure phone number and workflows to drive escalation via text and voice message.
-   Microsoft Teams: Ensure that your ServiceNow instance is configured to integrate with Virtual Agent and IT Service Management integration with Microsoft Teams plugin \(sn\_now\_teams\_it\) is active.
-   Mobile push notifications: Configure ServiceNow Agent and enable mobile push notifications

-   **[Activate On-Call Scheduling](../task/t_ActivateOnCallScheduling.md)**  
You can activate the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin if you have the admin role.
-   **[Setting up Slack as a contact method](../../on-call-scheduling/reference/slack-setup-oncall.md)**  
You configure Slack to enable users to receive Slack notifications for escalations. To offer Slack as a contact method for shift members, you install the IntegrationHub spoke for Slack.
-   **[Setting up SMS and voice messaging as contact methods](c_UseNotifyWithOnCallScheduling.md)**  
To send On-call escalation notifications as SMS or voice messages, you must configure Notify.
-   **[Set up Microsoft Teams as a contact method for an on-call escalation](../../on-call-scheduling/task/set-up-msteams-oncall.md)**  
Enable users to receive Microsoft Teams notifications for an on-call escalation.
-   **[Set up mobile push as a contact method for an on-call escalation](../../on-call-scheduling/task/set-up-mobile-push-oncall.md)**  
Enable users to receive mobile push notifications for on-call escalations.

**Parent Topic:**[On-Call Scheduling](../../on-call-scheduling/concept/c_OnCallScheduling.md)

