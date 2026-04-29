---
title: Configuring On-Call Scheduling
description: Plan and configure On-Call Scheduling properties, templates, trigger rules, escalation policies, rosters, and schedules.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
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

## Redirection of UI16 module links to Service Operations Workspace

If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the On-Call Scheduling module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../../product/service-operations-workspace/task/redirect-ui16-module-links-sow.md).

**Note:** For new instances, this redirection configuration is automatically available in the base system. For upgrade instances, administrators can configure the redirection behavior from the SOW Admin Center.

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
-   **[Setting up custom providers as communication channel](../../on-call-scheduling/concept/custom-on-call-channel-integration.md)**  
You can define and integrate a custom channel to send on-call escalation notifications.

**Parent Topic:**[On-Call Scheduling](../../on-call-scheduling/concept/c_OnCallScheduling.md)

