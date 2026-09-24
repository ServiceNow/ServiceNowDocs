---
title: Embedded breaks and lunches
description: A break or lunch can be embedded directly within a work order task, so a technician doesn't have to leave the task to take scheduled time away.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/embedded-breaks-and-lunches.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Embedded breaks and lunches

A break or lunch can be embedded directly within a work order task, so a technician doesn't have to leave the task to take scheduled time away.

## How embedded breaks and lunches work

Whether a break's status updates automatically depends on the Auto-status breaks setting. When it's on, a break automatically transitions to taken at its scheduled start time and to completed at its scheduled end time, without technician action. When it's off, the technician manually takes the break. Either way, the work order task pauses while the break is in progress and resumes once the break is complete. The task's estimated end time adjusts to account for the time away. Each break is recorded in the Work Notes of the work order task, so managers and technicians have a record of when breaks were taken. Breaks on a work order task can't overlap; each break must have a distinct time window.

Scheduling a work order task over an agent's planned break automatically adjusts the task to accommodate the break, embedding it into the task as long as the break starts at or after the task start time and falls within the task duration. A break that has already started is not embedded. Lunch breaks are indicated on the calendar with a fork and knife icon. If more than one break is scheduled during a task, a fraction on the break indicator shows the number of breaks taken versus scheduled \(for example, 1/2\). Technicians must mark their breaks as taken; if a technician misses a scheduled break, an X shows on the break indicator.

The work order task form shows a **Break Embedded** checkbox that indicates whether the task currently has an embedded break. This field is read-only and updates automatically as breaks are added or removed.

## Embedded break configurations

Administrators have the option to further configure embedded breaks. They can turn off automatic breaks so technicians take breaks manually instead. They can also change how many minutes before a break's start time the reminder notification is sent, instead of the default 15 minutes.

-   `sn_fsm_shift_schdl.enable_embed_break_in_wot` — Enables or disables break embedding within work order tasks globally.
-   `sn_fsm_shift_schdl.wfo.break.auto_status` — When enabled, a break's status updates automatically once its scheduled end time passes, so technicians don't have to manually mark the break as taken.
-   `sn_fsm_shift_schdl.wfo.break.reminder_minutes` — Sets how many minutes before a break's scheduled start time the system sends a reminder.

For details, see [Properties installed with Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/r_PropInstallWFieldServMgmnt.md).

## Schedule-locked tasks

A schedule-locked work order task has a fixed start and end time that can't shift to accommodate a break. As a result, you can't add a break to a task that's schedule locked. You also can't delete a break that's already embedded in a task once it's locked.

## Related tasks

-   [Add a break to a shift](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-manager-workforce/add-break-workforce.md)

    Schedule a break for a technician so their availability reflects real-time off during a shift.

-   [Edit or delete a break](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-manager-workforce/edit-break-workforce.md)

    Adjust a break's timing or remove it entirely when a technician's schedule changes.

-   [Edit or delete a break from the CSP in Workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-manager-workforce/edit-break-csp-workforce.md)

    Make the same update without leaving the calendar, so you can manage a technician's schedule faster.

-   [Check a break in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/check-break-dispatcher.md)

    See whether a technician's break is planned or already taken before you assign or reschedule work.

-   [Check on a break](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/check-break-mobile.md)

    Confirm your own break status from the field so you know when you're expected back on task.

-   [Check a break in Manager Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/check-break-manager-mobile.md)

    Check a technician's break status on the go, without needing to be at a desk.

-   [Take a break manually in the mobile agent app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/take-break-manually-mobile.md)

    Manually record a break when Auto-status breaks is turned off.

-   [Configure event colors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/configure-event-colors-wfo-fsm.md)

    Administrators can set border and background colors so breaks and other events stand out clearly on the calendar.


