---
title: On-Call Scheduling release notes
description: The ServiceNow On-Call Scheduling application enables you to verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Brazil release.The ServiceNow On-Call Scheduling application enables you to verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/on-call-scheduling-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-21"
reading_time_minutes: 1
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# On-Call Scheduling release notes

The ServiceNow® On-Call Scheduling application enables you to verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Brazil release.

## About On-Call Scheduling

-   Respond to incidents faster by ensuring a dedicated support team member always responds. Define on-call schedules, roster rotations, and escalation policies, and automatically escalate to the next responder until someone acknowledges.
-   Give every on-call responder one place to view their schedule, manage shifts, request time off, and track escalation status, from the desktop or the mobile app.
-   Ensure faster response times by reaching responders over the channels they already use and see the delivery status of every notification sent.

See [On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/c_OnCallScheduling.md) for more information.

## Activation and other requirements

-   **Activation information**

    On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/t_ActivateOnCallScheduling.md). Activating this plugin activates the following third-party libraries:

    -   FullCalendar library
    -   DHTMLX scheduler
    **Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-service-management-rn-landing.md)

## Brazil

The ServiceNow® On-Call Scheduling application enables you to verify that dedicated support team members are available to resolve issues when they occur. On-Call Scheduling was enhanced and updated in the Brazil release.

### What's new

-   **[Delivery status tracking for On-Call Scheduling notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/delivery-status-tracking-oncall.md)**

    Track on-call escalation notification delivery status from dispatch through acknowledgment across all supported channels. View failure reasons for each contact mode when notifications fail to reach recipients.


### What's changed

-   **[On-Call read role coverage for on-call read access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/roles-assigning-oncall.md)**

    The On-Call read \[oc\_read\] role grants read-only access to On-Call Scheduling rotations, rosters, schedules, escalations, communication channel configuration, and reports, and dashboards.


-   **[Escalation logging is true by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-properties.md)**

    The `com.snc.on_call_rotation.log_escalations` property, which controls whether on-call escalations are logged, is enabled by default. After upgrade, the existing value on this property remains unaffacted.


