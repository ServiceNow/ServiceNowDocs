---
title: On-Call Scheduling release notes
description: The ServiceNow On-Call Scheduling application enables you to verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# On-Call Scheduling release notes

The ServiceNow® On-Call Scheduling application enables you to verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Australia release.

## On-Call Scheduling highlights for the Australia release

-   Configure on-call schedule features using granular roles.
-   Configure a monthly roster rotation for an on-call schedule to simplify shift management.

See On-Call Scheduling for more information.

## New in the Australia release

-   **Monthly roster rotation for an on-call schedule**

    Simplify shift management by configuring a monthly roster rotation for an on-call schedule. This option is available only for the 2024 schedule engine.

-   **Granular role for on-call schedule configurations**

    Configure on-call schedule features using the granular and specific role, sn\_on\_call\_admin. It contains sn\_trigger\_table\_cfg\_read and sn\_trigger\_table\_cfg\_write roles.


## Activation information

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see Activate On-Call Scheduling. Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

## Related ServiceNow applications and features

-   **Notify**

    In addition to email notifications, you can send on-call escalation notifications as SMS alerts and voice calls. Engage on-call escalation in ServiceNow® Notify conference calls.

-   **ITSM Mobile Agent**

    Access the upcoming shifts and time-off requests of team members in the ServiceNow® ITSM Mobile Agent app. Send On-Call Scheduling escalation notifications as mobile push notifications.

-   **Service Operations Workspace for ITSM**

    Identify available On-Call Scheduling members of a support group who can be contacted to resolve an issue in ServiceNow® Service Operations Workspace.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

