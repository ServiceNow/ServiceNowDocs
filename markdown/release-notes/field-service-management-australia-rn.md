---
title: Australia
description: Field Service Management enhancements and new features in the Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/field-service-management-australia-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Field Service Management release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Australia

Field Service Management enhancements and new features in the Australia release.

## What's new

-   **[Dispatcher Workspace v10.1.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/view-task-calendar.md)**

    View break and lunch details directly within task events on the calendar in Dispatcher Workspace. Dispatchers no longer need to open a separate record to see when an agent is on break. Lunch breaks can be viewed directly within scheduled tasks.

    Dispatchers can [build quick filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/quick-filters-dw.md) for the task panel and calendar using criteria such as skill, parts, and SLA breach. A task filter removes tasks that don't match, while a calendar filter grays them out instead of removing them.

    Avoid ferries when dispatchers view agent routes on the Dispatcher Workspace map. When an administrator enables the [avoid ferry routes property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/r_PropInstallWFieldServMgmnt.md) \(`sn_fsm_disp_wrkspc.dispatcher_workspace.avoid_ferry_routes`\), routes use land roads even if they take longer, and a ferry is used only when no land route is available.

-   **[Shift Scheduling v7.3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/embedded-breaks-and-lunches.md)**

    Embed breaks and lunches directly within a work order task. Breaks can transition automatically at their scheduled start and end time, or require manual action from the technician, based on the new Auto-status breaks setting. Either way, the work order task pauses and resumes with the break, with the change logged to the work notes in a work order task.

-   **[Field Service Mobile v2.1.0 break and recurring event updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/extend-break-mobile.md)**

    Take a break before its scheduled time, extend a break in progress up to your organization's configured limit, or end a break early when your organization allows it. The break updates on your schedule to reflect the actual time. Create recurring personal events directly from the mobile agent app.

-   **[Manager Mobile v1.2 recurring events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/event-manager-mobile.md)**

    Create and manage recurring personal events for agents from Manager Mobile.


**Parent Topic:**[Field Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/field-service-management-rn.md)

