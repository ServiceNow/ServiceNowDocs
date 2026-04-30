---
title: On-Call Scheduling release notes
description: The ServiceNow On-Call Scheduling application helps you verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# On-Call Scheduling release notes

The ServiceNow® On-Call Scheduling application helps you verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Yokohama release.

## On-Call Scheduling highlights for the Yokohama release

Control whether an on-call schedule or shift record link in all major on-call email notifications redirects you to Service Operations Workspace \(SOW\) or to the classic UI16 interface in On-Call Scheduling.

See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

## Changed in this release

-   **[Email redirection behavior for links in major on-call schedule email notification](https://www.servicenow.com/docs/access?context=create-update-schedule-oncall&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    In all major on-call schedule or shift email notifications, you can now decide where the links to an on-call schedule or shift record are redirected. Instead of an on-call schedule or shift record automatically opening in the classic UI16 interface in On-Call Scheduling, the record can be opened in SOW. The on-call schedule or shift record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`.
    -   The **Redirect SOW Email notification for On-call scheduling** \(**sow\_email\_notification\_redirect.on\_call**\) property is set to `true`.
    -   You have the sn\_sow\_user role.
    The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.


## Activation information

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://www.servicenow.com/docs/access?context=t_ActivateOnCallScheduling&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US). Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

## Related ServiceNow applications and features

-   **[Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    In addition to emails, you can send on-call escalation notifications as SMS alerts and voice calls. Engage on-call escalation in ServiceNow® Notify conference calls.

-   **[ITSM Mobile Agent](https://www.servicenow.com/docs/access?context=itsm-mobile-agent&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Access the upcoming shifts and time-off requests of team members in the ServiceNow® ITSM Mobile Agent app. Send On-Call Scheduling escalation notifications as mobile push notifications.

-   **[Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Identify available On-Call Scheduling members of a support group who can be contacted to resolve an issue in ServiceNow® Service Operations Workspace.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

