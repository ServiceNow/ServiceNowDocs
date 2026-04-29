---
title: Exploring On-Call Scheduling
description: The On-Call Scheduling application helps you ensure that dedicated support team members are available to resolve issues as they arise. Learn more about On-Call Scheduling and the benefits it can provide for the different user roles in your organization.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [On-Call Scheduling, IT Service Management]
---

# Exploring On-Call Scheduling

The On-Call Scheduling application helps you ensure that dedicated support team members are available to resolve issues as they arise. Learn more about On-Call Scheduling and the benefits it can provide for the different user roles in your organization.

## On-Call Scheduling overview

On-Call Scheduling provides a way to determine which member of a user group is available to work on a task.

On-Call Scheduling finds the right person to assign an incident to, by rotation through a hierarchy of duty rosters. The automated process relieves the administrative burden on resource managers and makes it easy for the incident managers to bring the right resources to the table when needed.

On-Call Scheduling can be used by process owners and support managers who want to collaborate more effectively. On-Call Scheduling simplifies the manual shift maintenance and administration efforts while improving the mean time to resolve \(MTTR\) efficiencies.

## On-Call Scheduling workflow

The various members of an organisation use On-Call Scheduling to work together. See a sample end-to-end workflow:![Infographic for on-call scheduling workflow. For the text description, refer to the workflow steps that follow.](../image/Oncall_workflow.png)

1.  Shift admin creates shift and group templates.
2.  Shift admin assigns role and configures escalation trigger rules.
3.  The shift manager creates a shift and add or delete members to the shift.
4.  Shift manager designs the entire escalation process for the new shift.
5.  Roster member views their on-call schedules and find out who the other members on their shift are.
6.  Roster member can specify their availability and preferred contact methods from the methods set up by Shift admin.
7.  Roster members can submit a time-off request and refer another member of the group to cover the shift.
8.  Roster members views the roster and escalation details for a shift.
9.  Roster members view on-call reports and receive reminders.
10. The shift manager approves or rejects the time-off requests.
11. Shift manager reviews the on-call schedules for their groups for any gaps and time-off requests.
12. Shift manager provides, replace, or delete coverage and time-off requests.
13. Roster members receive on-call escalation notifications to acknowledge tasks or conference requests.
14. Shift manager views escalation, group, and performance reports of their on-call teams.

## On-Call Scheduling benefits

<table id="table_zxt_h3r_fyb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Use the calendar to view or select a shift. You can set a day, week, or month view as your preference. The calendar also allows you to set your preferred start day of the week.

</td><td>

[View my On-Call calendar on my calendar app](../task/view-my-schedule-on-my-app-oncall.md)

</td><td>

itil, rota\_manager

</td></tr><tr><td>

Create your own escalation policies and path. On-Call Scheduling allows you to create an escalation trigger rule using the templates available, based on your requirement.

</td><td>

[Designing an escalation process](designing-escalation-process-oncall.md)

</td><td>

itil, rota\_manager, rota\_admin

</td></tr><tr><td>

Use any one of the multiple channels such as Slack, Microsoft Teams, mobile push messages, SMS, and voice messages to set as the preferred contact method for receiving notifications.

</td><td>

[Configure my availability and contact preferences](../task/config-my-contact-prefs-oncall.md)

</td><td>

itil, rota\_manager, rota\_admin, admin

</td></tr><tr><td>

Generate escalation reports, shift reports, and performance reports.

</td><td>

[Viewing On-Call Scheduling reports](../../user-administration/concept/viewing-reports.md)

</td><td>

itil, rota\_manager, rota\_admin

</td></tr><tr><td>

Access the performance reports that are available for premium dashboard users.

</td><td>

[Legacy: Viewing the Performance reports for escalations](viewing-performance-report-oncall.md)

</td><td>

premium dashboard user

</td></tr><tr><td>

Download and use the Mobile agent to perform all these activities on the go.

</td><td>

[Getting started with the On-Call Scheduling mobile app](../task/mobile-getting-started-oncall.md)

</td><td>

itil, rota\_manager

</td></tr></tbody>
</table>## Redirection of UI16 module links to Service Operations Workspace

If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the On-Call Scheduling module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../../product/service-operations-workspace/task/redirect-ui16-module-links-sow.md).

**Note:** For new instances, this redirection configuration is automatically available in the base system. For upgrade instances, administrators can configure the redirection behavior from the SOW Admin Center.

-   **[On-Call Scheduling capabilities](on-call-scheduling-capabilities.md)**  
The key features and capabilities of On-Call Scheduling can be used by the various user roles.
-   **[On-Call Scheduling new schedule engine](oncall-schedule-engine.md)**  
Introducing the new On-call schedule engine with enhanced capabilities and user experience.
-   **[On-Call Scheduling new trigger engine](on-call-new-trigger-engine.md)**  
On-Call Scheduling new trigger engine enables the on-call subflows to get launched via the flow runner queue instead of the event queue. Launching via the flow runner queue improves the on-call performance and helps to alert the on-call members faster than launching via event queue.

**Parent Topic:**[On-Call Scheduling](c_OnCallScheduling.md)

