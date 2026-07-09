---
title: On-Call Scheduling release notes
description: The ServiceNow On-Call Scheduling application helps you verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# On-Call Scheduling release notes

The ServiceNow® On-Call Scheduling application helps you verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Zurich release.

## On-Call Scheduling highlights for the Zurich release

-   Build on-call escalation notification configurable flows by using subflows that are available by default in new instances.
-   Add new custom providers as channels for on-call escalation notifications.
-   Configure the on-call notification message and response keywords to send the escalation notifications to the stakeholders.
-   Send the on-call escalations notifications to all the stakeholders when any of the configured record fields are modified.
-   Use Coral, which is the new default theme for Next Experience and Core UI.

See [On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/c_OnCallScheduling.md) for more information.

## Important information for upgrading On-Call Scheduling to Zurich

Starting from the Zurich release, On-Call Scheduling uses subflows, not workflows. You must transition from workflows to subflows, because the workflows are considered as legacy workflows. For existing users in Zurich, your current workflows continue to be supported. However, for new users, the On-Call Scheduling plugin installations on Zurich and later instances only use subflows.

Maintain, build, and modify your own custom on-call scheduling flows in Workflow Studio with subflows for new instances. The following subflows are available for configuration:

-   On-Call: Assign
-   On-Call: Assign and Notify
-   On-Call: Assign by Acknowledgment
-   On-Call: Assign by Acknowledgement per Rota
-   On-Call: Assign by Acknowledgement Voice
-   On-Call: Check Assignment Response
-   On-Call: Conference Call Escalation
-   On-Call: Escalations by Email
-   On-Call: Escalation By Email per Rota
-   On-Call: Time-off approval

## New in the Zurich release

-   **[Add custom on-call notification channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/custom-on-call-channel-integration.md)**

    Increase the flexibility in communication by adding and configuring service providers as on-call notification channels. You must configure the communication channel by using the On-call communication channel configuration \[on\_call\_comunication\_channel\_config\] table. After you configure the channel, you can select the new channel. This feature is applicable only after the subflows are configured and used.

-   **[Customize the on-call notification message and keywords](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/config-oncall-communication-channel.md)**

    Customize an on-call notification message and response keywords that are sent to the user and user groups as per your preferences. You can customize the message and keywords by using the On-call communication channel configuration \[on\_call\_communication\_channel\_config\] tables.

-   **[Send the on-call escalation notifications when the configured record fields are modified](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/create-trigger-rule-oncall.md)**

    Send the on-call escalation notifications when the configured record fields are modified. On-call trigger rules have the following enhancements:

    -   Configure the changes to fields as a triggering condition to run trigger rules. For example, changes to the **Priority** field for an incident can be configured as a trigger condition.
    -   Configure the group or team level trigger rules, or you can configure the global trigger rules that aren’t associated with a user group.
    -   If the assignment group is auto-populated when an incident is created, you can still configure the on-call trigger rules to run and send the escalation notifications.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Performance improvements in subflows for on-call notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/on-call-new-trigger-engine.md)**

    The following performance enhancements are available for on-call notifications when subflows are used:

    -   On-call notifications are sent to multiple channels such as SMS or email simultaneously instead of sending it sequentially.
    -   When the **com.snc.on\_call\_rotation.new\_trigger\_engine** property is set to true, the on-call subflows are processed via the Flow runner queue. The on-call subflows that are marked as High priority are processed faster via a Flow runner queue especially when multiple events are triggered at the same time and are in the process queue.
    -   Reminder notifications are also sent to users when the instance is upgrading.
-   **[Enhanced on-call trigger rules to support subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/on-call-scheduling-subflows-overview.md)**

    The on-call trigger rules form is enhanced to trigger a subflow when the trigger rule is executed. You can enable and select a specific subflow for a trigger rule.


## Activation information

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/t_ActivateOnCallScheduling.md). Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/notify-landing-page.md)**

    In addition to emails, you can send on-call escalation notifications as SMS alerts and voice calls. Engage on-call escalation in ServiceNow® Notify conference calls.

-   **[ITSM Mobile Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/itsm-mobile-agent.md)**

    Access the upcoming shifts and time-off requests of team members in the ServiceNow® ITSM Mobile Agent app. Send On-Call Scheduling escalation notifications as mobile push notifications.

-   **[Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/sow-landing-page.md)**

    Identify available On-Call Scheduling members of a support group who can be contacted to resolve an issue in ServiceNow® Service Operations Workspace.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-service-management-rn-landing.md)

